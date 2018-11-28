# rsa_nw_esa_whatsnew
collection of ESA rules for whats new stuff

set a learning period for the rules
watch for events that match criteria and add to known/seen window
alert when something that has not been seen before happens on the network

currently looking at:
```
whats_new_ja3
- new ja3 hashes after a learning period
  "whatsNewJA3": {
    "ssl_ja3": "a2d9e37641f5ba558913675a08401356",
    "ip_src": "192.168.254.18",
    "ip_dst": "209.132.180.180",
    "direction": "outbound",
    "client": "HTTPS",
    "service": 443,
    "ssl_subject": "*.gnome.org",
    "org_dst": "Red Hat",
    "alias_host": "[extensions.gnome.org]",
    "time": 1543406030,
    "medium": 1
  }
```
whats_new_ssh
- new ssh client connections
```
, {
  "whatsNewSSH1": {
    "client": "OpenSSH_7.4",
    "ip_src": "192.168.254.23",
    "ip_dst": "192.168.254.184",
    "direction": "lateral",
    "org_dst": null,
    "domain_dst": null,
    "alias_host": null,
    "medium": 1,
    "server": "OpenSSH_7.4",
    "time": 1543353801
  }
```
whats_new_client
- new user agents (log and packets)
```
  "whatsNewClient": {
    "client": "RSA NetWitness",
    "ip_src": "192.168.254.140",
    "ip_dst": "192.168.254.148",
    "direction": "lateral",
    "org_dst": null,
    "domain_dst": null,
    "alias_host": "[esa62.domain.ca]",
    "medium": 1,
    "time": 1543407282
  }
```
whats_new_srcmac
- new source mac seen on the network (required eth.src.vendor key and ethernet_oui parser)
 ```
 "whatsNewMACSrc": {
    "eth_src_vendor": "VMware, Inc.",
    "ip_src": "10.15.16.16",
    "ip_dst": "192.168.254.180",
    "eth_src": "00:50:56:99:5f:28",
    "direction": "lateral",
    "time": 1543341264,
    "medium": 1
  }
```
whats_new_ca
- new ssl.ca values seen on packet traffic
 ```
 "whatsNewCA": {
    "ssl_ca": "Palo Alto Networks",
    "ssl_subject": "Palo Alto Networks",
    "ip_src": "10.20.40.4",
    "ip_dst": "192.168.254.23",
    "direction": "lateral",
    "org_dst": null,
    "domain_dst": null,
    "alias_host": "[please]",
    "medium": 1,
    "time": 1543367239,
    "service": 443
  }
```
whats_new_certca
- file certificate ca seen after time for endpoint traffic
```
"whatsNewCertCA": {
    "cert_ca": "C=US, S=CA, L=Santa Clara, O=Intel Corporation, CN=Intel External Basic Issuing CA 3B",
    "cert_subject": "C=US, S=CA, L=Santa Clara, O=Intel Corporation, CN=Intel Corporation - Client Components Group",
    "alias_ip": "[192.168.254.170]",
    "alias_host": "[WIN15]",
    "category": "File",
    "filename": "iaLPSSi_GPIO.sys",
    "medium": 32,
    "time": 1543349842
  }
```
