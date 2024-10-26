

# Proxmox notes 

This document lists all changes i've made to any VM or setting within proxmox 


# 10/13/2024 

* Added all private IP's of hosts on local network to truenas allowlist for pool1 & pool2 

* Removed torrentfunk, torlock , and idope.se from Jackett indexers 

* Removed  torlock , and idope.se from sonarr indexers

* Removed broken torrent for Rick And Morty Season 2 

* Changed share settings on pool1 under "Purpose" , changed from 'Default Share Parameters' to 'No Presets'

# 10/23/2024 

* Unblocked protonvpn.com in adguard home 

* Unblocked vpn-api.proton.me in adguard home 

* updated adguard blocklists 

* turned off mouse for tmux on buhfurpc 

* removed ca-22.protonvpn.tcp.conf & ca-49.protonvpn.udp.conf from torrent server openvpn connections

* added new protonvpn openvpn country UDP configs to torrent-server and rebooted 
