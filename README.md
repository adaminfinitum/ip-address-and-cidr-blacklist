# IP Address and CIDR Blacklist

There's a [detailed blog post that goes along with this repository](https://www.adaminfinitum.com/security/ip-addresses-blocked-malicious-traffic/) that explains some of my logic in how I added IP addresses and CIDR blocks.

In an nutshell, the server I added these firewall rules to is one that hosts blogs and other personal websites (yes, some are business websites but they are my own businesses, not enterprises so theey don't need to communicate to many remote services). They are all written in English and effectively U.S. based so this list is especially agressive at blocking non-U.S. data center traffic (if it has ever sent malicious/suspicious traffic to my server).

If you're a blogger or business in the U.S., with a website that doesn't have a ton of dependencies on 3rd party services, this will probably work great for you.

I tried not to block and IP addresses that are used by crawlers of major search engines or other service that, while I may not use them, aren't malicious (like Facebook), examples of some of the IP addresses of various services that I either made sure weren't blocked or, in the case of Ahrefs are blocked but you could edit the list to unblock them if so desired.

## Not Blocked:

### DuckDuckGo
23.21.227.69

### WordPress.com 
192.0.64.0 - 192.0.127.255
192.0.64.0/18 
### WP.com feedbot
192.0.85.132

### Google
66.249.64.0 - 66.249.95.255
66.249.64.0/19

### Bing
40.112.0.0/13
40.120.0.0/14
40.124.0.0/16
40.125.0.0/17
40.80.0.0/12
40.96.0.0/12
52.224.0.0/11

### AppleBot
17.58.96.224 
17.58.96.225
NetRange:       17.0.0.0 - 17.255.255.255
CIDR:           17.0.0.0/8

### Facebook Bot
173.252.127.117

## Possibly Blocked 
Check the IP address blacklist if you utilize these services and want them to have access to websites on your server.

### Majestic
144.76.6.230
5.189.159.208

### Moz Open Site Explorer
216.244.66.242

### Ahrefs
54.36.148.0 
54.36.148.164 
54.36.148.179 
54.36.148.35 
54.36.149.1 
54.36.149.89

### Mojeek
5.102.173.71


