just click 
www.ananthuunnip.ml

to reach the site

Buy a domain (e.g., richpauloo.com). I used godaddy.com, but you can use any number of domain name registries.
Step 1
go to github 

In your github.io repository Settings, add the domain you purchased in Step 1 to the “Custom domain box”:


Step 3
In your DNS Management console, add a CNAME record with the following parameters:

    type = CNAME
    name = www
    value = username.github.io.


Step 3
Meaning: This tells your DNS to point www.username.com requests towards the site hosted at username.github.io. Set the TTL (time to live) to an hour or less.
Step 3
Next, in your DNS Management console, add 4 separate A records with the following information:

    type = A
    name = @
    points to (value) = IP

IP
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153


However the values might have changed since the time of writing. See the offical docs for the most up-to-date values.

Meaning: “A” records connect your domain name (hosted by your DNS) to the actual IP addresses where your site lives on a server (at Github).
