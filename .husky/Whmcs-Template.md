
 
But it didn't do anything. So I tried editing random things in the header.tpl and footer.tpl files, for example, changing $companyname from $companyname to 'Random title', or in footer.tpl, editing the links in the right-side menu. I even went so far as to upload a blank header.tpl file with the text 'blah blah blah'. Nothing changed, all I see is the default 'portal' template, no matter what I do. I have my template files uploaded in the template directory (in a folder called 'vs\_aqua'), and the url I'm using is 'www.mydomain.com/whmcs/?systpl=vs\_aqua'. I tried changing that to 'systpl=default' and that changed the template, but any changes I make to my template don't appear, even in other browsers with the cache cleared.
 
Yes, I tried that. I did it again now though, and my edit to the 'company title' field came through this time. According to the wiki, though: 'You can then preview your new template by specifying it "on the fly" using an url such as =xxxxx where xxxxx is the name of your new template.' But that doesn't work for my template for whatever reason.
 
**DOWNLOAD --->>> [https://zoohogonka.blogspot.com/?file=2A0SLs](https://zoohogonka.blogspot.com/?file=2A0SLs)**


 
It's definitely using the files in the vs\_aqua template folder, I renamed it and when I refreshed I just got a blank page. Changes made manually to the template work, but my included header.php stuff isn't appearing at all.
 
I had the same problem you describe, I just deleted all content of template\_c folder and my changes are now taken into account, I guess you have to empty this folder every time you make changes to your templates files...
 
its either a path error or a coding error(php or smarty). Have you turned errors on in configuration.php? Have you looked at the error logs on the server. Your pretty much flying blind here. Also check out this on smarty.net
 
i know this has been brought up before (probably numerous times i expect), however, as there is an **old** whmcs tutorial "WHMCS Creating a Custom Template" on youtube, i need to ask this again.

Like others before me, if i wanted to pay money for integrations, i would not be here asking this question...this is a community community where people share their expertise and experiences. In the past i have purchased whmcs themes, however, i have been very disspointed in what i have ended up with. In looking at some of the recent ones, i am still very unsure if they are worth the money (in some cases i am convinced absolutely not...even for some whmcs themes costing $129). As an example, a number of "advertised as whmcs themes", in fact are Wordpress themes which then require the use of a paid for wordpress integration plugin in order to function correctly with whmcs. This is not particularly desirable or honest in my opinion...so that brings me here posting this question.
 
I am an real fan of Wordpress, and use the Avada Wordpress framework to build websites quite often. I am not a coder, but do understand html and css basics. It s just that the source code for my wordpress website built using avada appears to contain a lot of coding that i believe may be unneeded for whmcs custom template.
 
I know that using Wordpress & WHMCS seems the right choice and the easiest approach but in the long run it's not. You have two systems to maintain, two separate admin interfaces, you double the risk of something going wrong and most important you'll be afraid to update both softwares. In my experience integrations are not so reliable and like you said there's a lot of unnecessary code involved. Keeping integrations and templates functional is not impossible but frustrating.
 
Personally I took a different approach. I need WHMCS but I also need to publish contents. Since the majority of features I need are in WHMCS, I decided to focus on this system adding the missing pieces like news, blog posts etc. Before you ask no, I'm not talking about the standard announcements section. I will no longer invest my time an money in having unhandy and unreliable integrations.
 
The disavantage of the above approach you talk of is, in order for one to extend their webpage in whmcs, it seems to me that a lot of work is required. In Wordpress, this is but a small almost effortless task (especially with the Avada Wordpress theme/framework i use which is 90% "drag and drop" and shortcodes for everything else), and this is where i am at a crossroads...the much shorter long-sighted road is the Wordpress one because of the ease with which Wordpress websites can be upgraded and modernised. Playing around with the smarty templating system in whmcs editing layouts and creating addtional pages and functionality, is nothing short of a time consuming pain in the ass!
 
What about the option to use both on parent domain + subdomain arrangement in a non-integrated arrangement. Wordpress for the main website, then url link to the whmcs interface on the sudomain for ecommerce stuff (such as hosting, domains, renewals etc)? In using this method i am essentially keeping both separated. It would mean that clients cannot log into wordpress and that login be used to access whmcs (which i would not want anyway).
 
So if i were to take my above mentioned approach, reskinning whmcs is my next hurdle. As i said in first post, there seems to be an awful amount of source code when i "inspect" my wordpress page in google chrome.
 
I do also understand if you want to achieve this on your own. You can fairly easily integrate your Wordpress header and footer into your whims template by using the following method. ( This is what I did )
 
Of course my approach takes longer and is way more complicated. The question here is that after more than 10 years of WHMCS, I had enough of repeating myself with every client of mine asking for integration that sooner or later breaks with updates.
 
That's why for me it was worth investing time in the opposite direction. This way I no longer have to create two copies of the same template full of unnecessary code and deal with limitations (2 admin interfaces is a big no).
 
if you're going to do that, you might as well use a hook to add the code in the header/footer - because it will be interesting to see what happens in v8 if the temporary enablement of php finally gets removed (it's already been removed from Smarty)... when that happens, your current solution won't work.
 
Though with that said, I would advise not to integrate wordpress with WHMCS beyond using the WHMCS data feeds available or custom ones. Reason being if wordpress is hacked, which is possible, then they can get access to WHMCS also and thus all your client info. Applications should really be separated by server users also but I digress.
 
Using the domain and sub domain for WHMCS is what I would recommend. I do that personally, though use a site builder and not wordpress for the site. Just get WHMCS to look similar to the wordpress theme or do a completely different look to make it stand out more. Then on the regular site, have links to WHMCS login pages and toss the wordpress login links away. Would users really need to access wordpress?
 
Themes, or System Themes, in WHMCS control the client-facing user interface. WHMCS allows you to provide a seamless experience for your website visitors by using system themes to customise the Client Area to match the rest of your website.
 
You can set a **Default Order Form Template** at **Configuration > System Settings > General Settings** in the **Ordering** tab. You can also select an order form template for individual product groups at **Configuration > System Settings > Products/Services**.
 
Redefine Web hosting excellence and **save 90% of the time** you spend on your website management. Leave a lasting mark in the digital landscape with our **Best WHMCS Web Hosting Themes and Templates**.
 
HostX, CloudX , ClientX, TwentyX, etc.) are crafted with a user-friendly interface, modern design elements, and customizable features, allowing you to create a professional and visually appealing website for your web hosting business.
 
WHMCS Global Services (WGS) understands the importance of a well-designed website in attracting and retaining customers. Our premium web hosting templates are aesthetically pleasing and optimized for performance and SEO, helping your website rank higher in search engine results.
 
**1. Multipurpose Theme:**All our advanced themes are meticulously designed to cater to various business aspects, whether it be IPTV, VPN, internet sales, VOIP services, or any other industry. We strive to deliver a highly professional and tailored experience for your specific business needs.
 
**2. Compatible with all the third-party WHMCS modules:**All our hosting website templates are designed to be fully compatible with all third-party platforms and WHMCS modules. This means that you can seamlessly integrate your preferred third-party tools and utilize the functionalities provided by the WHMCS module without any compatibility issues.
 a2f82b0cb4
 
