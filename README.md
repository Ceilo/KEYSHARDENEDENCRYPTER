# KEYSHARDENEDENCRYPTER
Credit goes to @Anonymous and Hardened-Anonymized-DNSCrypt-Proxy



---Skip to content
BL4CKH47H4CK3R
/
Hardened-Anonymized-DNSCrypt-Proxy

Type / to search
Command palette
Create new...
Issues
Pull requests
You have unread notifications
Code
Pull requests
Actions
Projects
Security
Insights
Owner avatar
Hardened-Anonymized-DNSCrypt-Proxy
Public
Fork your own copy of BL4CKH47H4CK3R/Hardened-Anonymized-DNSCrypt-Proxy
BL4CKH47H4CK3R/Hardened-Anonymized-DNSCrypt-Proxy
 1 branch
 0 tags
Latest commit
@BL4CKH47H4CK3R
BL4CKH47H4CK3R ⏰ Mon Jul 3 02:52:16 PM UTC 2023
bb8e6a7
3 hours ago
Git stats
 8 commits
Files
Type
Name
Latest commit message
Commit time
PKGBUILD
⏰ Mon Jul 3 02:52:16 PM UTC 2023
3 hours ago
README.md
⏰ Thu May 18 09:45:25 PM UTC 2023
2 months ago
dnscrypt-proxy.install
⏰ Thu Jun 15 09:21:40 PM UTC 2023
3 weeks ago
dnscrypt-proxy.service
⏰ Sun Apr 9 07:59:55 PM UTC 2023
3 months ago
dnscrypt-proxy.toml
⏰ Mon Jul 3 02:52:16 PM UTC 2023
3 hours ago
README.md
Hardened-Anonymized-DNSCrypt-Proxy
Wipe Snoopers Out Of Your Networks

A flexible DNS proxy, with support for modern encrypted DNS protocols such as DNSCrypt v2, DNS-over-HTTPS, Anonymized DNSCrypt and ODoH (Oblivious DoH).

Features
For all features please refer to the OFFICIAL PAGE
All binary files are downloaded from the OFFICIAL RELEASE PAGE
Why This Project ?
There Are Automated DNSCrypt-Proxy Client For Both Windows & Android (Magisk Module)
But For Linux, People Find It Hard To Configure DNSCrypt-Proxy Manually. But I Wanted To Keep It Simple, So It's Here !

Supported Linux Distributions
Arch / Arch Based Distro With SystemD & NetworkManager

Differences From The Main DNSCrypt-Proxy Project
server_names = altername [RUS], ams-dnscrypt-nl [NLD], d0wn-tz-ns1 [TZA], dct-at1 [AUS], dct-nl1 [NLD], dct-ru1 [RUS], dnscrypt.be [BEL], dnscrypt.ca-1 [CAN], dnscrypt.ca-2 [CAN], dnscrypt.pl [POL], dnscrypt.uk-ipv4 [GBR], dnswarden-uncensor-dc-swiss [CHE], meganerd [NLD], openinternet [USA], plan9dns-fl [USA], plan9dns-mx [MEX], plan9dns-nj [USA], pryv8boi [DEU], sby-limotelu [IDN], scaleway-ams [NLD], scaleway-fr [FRA], serbica [NLD], techsaviours.org-dnscrypt [DEU], v.dnscrypt.uk-ipv4 [GBR] are the resolvers in use.

doh_servers = false (disable servers implementing the DNS-over-HTTPS protocol)

require_dnssec = true (server must support DNSSEC security extension)

force_tcp = true (fix for mobile data intial connection random issues if routes have been set and skip_incompatible = true, see DNSCrypt/dnscrypt-proxy/discussions/2020)

timeout = 1000 (set the max. response time of a single DNS query from 5000 to 1000 ms.)

blocked_query_response = 'refused' (set refused response to blocked queries)

# log_level = 0 (set the log level of the dnscrypt-proxy.log file to very verbose, but keep it disabled by default)

dnscrypt_ephemeral_keys = true (create a new, unique key for every single DNS query)

bootstrap_resolvers = ['45.11.45.11:53'] (use DNS.SB instead CloudFlare)

netprobe_address = '45.11.45.11:53' (use DNS.SB instead CloudFlare)

block_ipv6 = true (immediately respond to IPv6-related queries with an empty response)

blocked-names.txt, blocked-ips.txt, allowed-names.txt and allowed-ips.txt files enabled. (to know more specifics about this, please refer to the Filters (optional) section below)

anonymized_dns feature enabled. (routes are indirect ways to reach DNSCrypt servers, each resolver has 2 relays assigned)

skip_incompatible = true (skip resolvers incompatible with anonymization instead of using them directly)

direct_cert_fallback = false (prevent direct connections through the resolvers for failed certificate retrieved via relay)

Configure [Copy-Paste]
git clone https://github.com/BL4CKH47H4CK3R/Hardened-Anonymized-DNSCrypt-Proxy
cd Hardened-Anonymized-DNSCrypt-Proxy
makepkg -Ccrfs --noconfirm
sudo pacman -U *zst
Deconfigure [Copy-Paste]
sudo pacman -Rcnsu Hardened-Anonymized-DNSCrypt-Proxy
Filters [Optional]
Filters are a powerful set of built-in features, that let you control exactly what domain names and IP addresses your device are allowed to connect to. This can be used to block ads, trackers, malware, or anything you don't want your device to load. To know more about it, you can check the official documentation DNSCrypt-Proxy-Filters

DNS Leak Testing [Websites]
IPLeak
DNSLeakTest
BrowserLeaks
Configuration [Post Installing]
You can edit dnscrypt-proxy.toml as you wish located on /etc/dnscrypt-proxy/dnscrypt-proxy.toml
For more detailed configuration please refer to official documentation
Credits
Frank Denis & All Other Contributors For This Awesome Project
Special Thanks To quindecim For The DNSCrypt-Proxy Configuration
About
Wipe Snoopers Out Of Your Networks

Resources
 Readme
 Activity
Stars
 5 stars
Watchers
 3 watching
Forks
 1 fork
Report repository
Releases
No releases published
Packages
No packages published
Languages
Shell
100.0%
Footer
© 2023 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
