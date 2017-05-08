# digitalocean-serverpilot-letsencrypt
Install Let's Encrypt SSL on ServerPilot (Free Plan) / Digital Ocean Hosted Droplet

Let's Encrypt on Your ServerPilot Free Plan
Automate the installation of Let's Encrypt SSL on the free plan of ServerPilot

About the script

ServerPilot's paid plan costs only $10 per month that unlocks auto installation of Let's Encrypt SSL along with some other premium features. But if you don't want to spend that $10 then this script can automate the installation of the SSL on your ServerPilot servers. When you activate the SSL for an app, this script adds a cron job as well that takes care of the renewal of your Let's Encrypt SSL.

<code>Getting started</code>

Step 1: Clone the repo

If git isn't installed on your system, then install it first by typing this in terminal

<pre>sudo apt-get -y install git</pre>
and then run this command to clone the reposity

<pre>sudo git clone https://github.com/quickfever/digitalocean-serverpilot-letsencrypt.git && cd digitalocean-serverpilot-letsencrypt && sudo mv sple.sh /usr/local/bin/rwssl && sudo chmod +x /usr/local/bin/rwssl</pre>


When you will run the above command, the repo will be cloned to your system and the script will be copied to /usr/local/bin and will be made executable. After that, you can execute it easily.

## Install SSL

Here are the simple steps to install SSL on your apps

For main domains (Don't include www with your domain)

rwssl install example.com app_name main
In above example, you can see that I've passed four arguments to rwssl command. The first argument tells the script to install the SSL. Second argument is the domain name. Third argument is the app name of your domain and fourth argument tells either this is a sub domain or the main domain.

### For sub domains

<pre>rwssl install sub.example.com app_name sub</pre>

## Uninstall SSL

rwssl uninstall example.com app_name
rwssl uninstall sub.example.com app_name
Any questions? Ask me in my blog post here.


[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.example.com or <http://www.example.com> and sometimes 
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com
