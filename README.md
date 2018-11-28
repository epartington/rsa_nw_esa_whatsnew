# rsa_nw_esa_whatsnew
collection of ESA rules for whats new stuff

set a learning period for the rules
watch for events that match criteria and add to known/seen window
alert when something that has not been seen before happens on the network

currently looking at:

whats_new_ja3
- new ja3 hashes after a learning period
whats_new_ssh
- new ssh client connections
whats_new_client
- new user agents (log and packets)
whats_new_srcmac
- new source mac seen on the network (required eth.src.vendor key and ethernet_oui parser)
whats_new_ca
- new ssl.ca values seen on packet traffic
whats_new_certca
- file certificate ca seen after time for endpoint traffic
