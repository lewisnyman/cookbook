# Security

Managing your digital security is all about understanding the risks you face and determining the levels of risk that are tolerable with the data for which you are responsible. The security profile of a personal blog is very different from an e-commerce site, and is different again from a central government portal service.

## Security Essentials

There's some basic steps to take for digital security of your website or application.

#### Secure installation

Open source software usually has comprehensive documentation on securing your installation. As a bare minimum, follow these.

##### Strong passwords

[<img alt="XKCD: Password strength (https://xkcd.com/936/)" src="http://imgs.xkcd.com/comics/password_strength.png" width="500">](https://xkcd.com/936/)

Ensure you have a strong password for the administrative or root user. There is much discussion online about what constitutes a strong password ([Google]( https://support.google.com/accounts/answer/32040?src=soctw); [Wikipedia](https://en.wikipedia.org/wiki/Password_strength); [Correct Horse Battery Staple](http://correcthorsebatterystaple.net/)). We rcommend using a _pass phrase_ rather than a password, ensuring it is at least 16 characters long and preferably longer than 24 characters. 

#### Update all the things

Open source software projects regularly release security updates for the core sofware and for modules within it. Some OSS will include an update status that will specifically identify any available or pending security updates. **_Always_ ensure you install security updates.**

#### SSL encrypt your site

Post-Snowden, for technical and social reasons, encrypt your site with SSL. That's it.

Not just the obvious bits, like logins and checkouts. All of it. With the technical innovations of recent years, there are lots of ways to make a secure site run fast, so there's no need to worry about  

## Data Security

#### Cross-site scripting

We use open-source software that has a thorough understanding of site's vulnerabilities to cross-site scripting attacks and which thoroughly check user input. We're very careful with the extensions we include and custom code we write to keep project sites and applicaitons safe from cross-site scripting attacks. 

#### Encrypted database

Where appropriate, we will encrypt an application's production database to keep vulnerable personal data safe. In this case, encryption keys will be held securely, and that may warrant placing it in a separate location to the application itself.

#### Restricted access 

If the security profile of the system warrants it, we may opt to further restrict the application's access to the data in the database to only the data made available by an API layer in front of the database. That API itself will have strong boundary security and access limitations, via firewalls and other methods, to restrict and control access to it.

We also manage access to the application's hosting platform. If the project's security profile warrants it, we may include a number of elevated access control tools or systems. 

#### Clean database dumps of personal info

It almost goes without saying, but whenever we need to take a dump from a live database – for local development, debugging, support or whatever – we ensure that any personal and identifying data is cleaned out before the data touches any unsanctioned computers (including servers within your hosting platform that have not been specifically accredited or authorised to host that personal data).

