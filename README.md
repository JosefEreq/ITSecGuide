# Cyber Security Hardening Guide


#### <em> Last updated 2022-08-01 </em>

<br></br>

## Introduction

This document provides guidelines and recommendation for hardening the cyber security posture in the following areas:

* #### 		Online Security and Privacy
* #### 		Email
* ####	 	Windows 10 / 11
* ####		iOS
* ####		Firefox, Tor Browser and Thunderbird
* #### 		Network and Router

 ##### 		<em>(Coming soon) MacOS</em>
<br></br>

Each section and recommendation is categorized by area and security level, to make it easier for readers to find those that are relevant to them.
See the following 3 security level definitions:
* ##### 	Standard - Basic security. Little impact on usage and convenience. For basic users.
* ##### 	Advanced - Good security. Mild impact on usage and convenience. Requires knowledge in configuring computers, operating systems and applications.
* #####	Expert - Great security. Big impact on usage and convenience. Requires system administration knowledge.

<br></br>
The provided guidelines and actions are intended for <em>private cyber security</em>. No consideration have neccesarly been taken for enterprise environments.
<br></br>
<br></br>
<em>All recommended software are non-commercial open source projects.</em>

<br></br>
<br></br>
<br></br>
<br></br>
## Table of contents
1. [Internet, VPN and Email providers](#Providers)
2. [Accounts and Passwords](#AccsPWs)
3. [Windows 10 / 11](#WinCli)
4. [Web Browsing](#Browse)
5. [Email & Chat](#mail)
6. [iOS](#soi)
7. [Network and Router](#Network)
8. [Firefox & Tor Browser](#FirefoxTor)
9. [Firefox (Specific)](#Firefox)
10. [Tor Browser (Specific)](#Tor)
11. [Thunderbird Email](#Thunderbird)

<br></br>
<br></br>
<br></br>
<br></br>
<a name="Providers"></a>
# 	Internet, VPN and Email provider
Consider the following when choosing a Internet, VPN or Email provider;

*       What policy do they have regarding protecting sensitive customer data?
*       Have they handed out sensitive data to a government agency or a third party previously?
*       What customer data do they store?
        Your VPN provider should never store customer authentication or connection logs!
*       Do they have the neccesary resources to build a secure network infrastructure? 


<br></br>
<br></br>
<a name="AccsPws"></a>
# 	Accounts and Passwords
| Level | Title | Description | Note |
| :---        |   :----:   |    :----:   |         ---: |
| Standard | Use MFA! | Use multi-factor authentication for your online accounts and avoid SMS. Your SIM/phone number can be taken over by a scammer. Use a mobile app for verification instead. |  |
| Standard | Keep your accounts in your control. | Never log in with your online account on somebody elses device! |  |  |
| <b>Advanced</b> | Avoid online password managers that manages your key! | I recommend: <br></br><a href="https://keepass.info/"><b>Keepass</b> <img width="30" height="30" src="https://upload.wikimedia.org/wikipedia/commons/0/04/KeePass_icon.svg"></img></a>  Windows  <br></br> <a href="https://keepassxc.org/"><b>KeepassXC</b> <img width="30" height="30" src="http://keepassxc.org/images/keepassxc-logo.svg"></img></a>  MacOS <br></br>  <a href="https://apps.apple.com/us/app/authpass-password-manager/id1479297675"><b>AuthPass</b> <img width="30" height="30" src="https://static.crozdesk.com/web_app_library/providers/logos/000/008/475/box/authpass---password-manager-1570718935-logo.png?1570718935"></img></a> iOS | Online password managers that handle your key might be breached and leak your credentials. |


<br></br>
<br></br>
<a name="WinCli"></a>
# 	Windows 10 / 11
| Level | Title | Description | Note | 
| :---         |   :----:   |   :----:   |         ---: |
| Standard | Avoid signing in with or connecting a online Microsoft account. | Your identity might leak through local services communicating online if they can be tied to a online account. | |
| Standard | Set a secure password on your local computer user. | Set a long and complex password that's hard to guess.
| Standard | Configure in-app security and privacy settings. | Go trough each applications privacy and security settings first thing you do after installing it. | There's often a lot of of privacy settings. |
| Standard | Auto-lock on inactivity. | Set your computer to lock automatically after being inactive. |  |
| Standard | Enable auto-update. | Enable auto-update for both the operating system and applications, to make sure you always have the latest security patches. | Hackers countinesly scan the internet for vulnerable devices and services. |
| Standard | Completely disable crash reporting, to prevent data being sent to Microsoft. | <b>Powershell:</b> Run <em>"Disable-WindowsErrorReporting"</em>. | This feature might leak information about your device. |
| Standard | Restart your PC! | Regularly restart your PC to clean up running background processes and free up the memory from sensitive data.
| Standard | Disable network during setup! | Disable your network interfaces while installing and configuring your operating system. | Make sure the operating system and all applications are securely configured before connectiong to the internet |
| Standard | Encrypt your drives. | For encrypting drives/volumes I recommend <a href="https://www.veracrypt.fr/code/VeraCrypt/"><b>Veracrypt</b>  <img width="30" height="30" src="https://avatars.githubusercontent.com/u/7925881?s=200&v=4"></img></a> | | |
| Standard | Take backups! | Take regular file backups of the operating system drive and other important drives, a system image backup and store them in a safe location. | <b>NOTE:</b> Make sure every kind of backup containing sensitive data or system files is encrypted, no matter where you store it. | 
| Standard | Uninstall applications you don't need. | Uninstall applications in both <em>Control Panel/Programs and Features</em> and the Settings app. | <b>NOTE:</b> Some apps are only visible in the Settings app. |
| Standard | Disable all local accounts not being used, including the guest account.
| Standard | Fully activate Windows User Account Control(UAC). | Enable UAC in <em>Control Panel/User Accounts/Change User Account Control settings</em> Drag the slider to the higest level and click OK. | UAC will prompt for verification before an application elevates itself to admin.
| Standard | Install a endpoint protection solution on Windows <b>if neccesary</b>. | You may want to install a EDR solution, depending on how securely the computer is configured and used, since Windows is full of security vulnerabilities. Choose a modern EDR solution that looks for unusual executions and behaviors | <b>NOTE:</b> Select a EDR provider you trust. But remember that the they could potentially read all files on your PC. Avoid installing an EDR solution, for privacy concerns, if your Windows operating system is locked down with all the recommendations in this guide applied and you rarely open externally sourced documents/files. |
| Advanced | Don't use sleep mode. | Don't put your computer to sleep. Use hibernation instead. | Your memory is not cleared in sleep mode, keeping your disk decrypted, making it much easier for a malicious actor to access your data if your laptop gets lost or stolen.
| Standard | Disable logging in your torrent and VPN clients! | Don't leave traces of downloads in case you're subject to a legal investigation.
| Standard | Disable all autoplay features via the Windows Setttings app. | Disable AutoPlay and in <em>Windows Settings/Bluetooth & Devices/AutoPlay</em>. | This will prevent plugged in devices from auto-starting its local media.
| Standard | BIOS password | Set a BIOS password | |
| Standard | Secure boot | Enable UEFI secure boot | |
| Standard-<b>Advanced</b> | Disable RDP or restrict its connections! | Disable Remote Desktop on Windows unless you need it in <em>"Windows Settings/System/Advanced Sytem Settings/Remote/"</em> select <em>"Don't allow remote connections to this computer"</em> <b>AND</b> uncheck <em>"Allow Remote Assistance connections to this computer"</em>. <b>Advanced:</b> If RDP is needed, create a firewall rule to only allow connections from your own devices (IP-adresses) | There has been a lot of vulnerabilities discovered in RPD throughout the years. But more importantly, you should disable all network protocols you don't need. |
| <b>Advanced</b> | Enable LSA protection | <b>Registry:</b> Set/Create DWORD key <em>HKLM/SYSTEM/CurrentControlSet/Control/Lsa/RunAsPPL</em> with value of <em>"1"</em>. |  | 
| <b>Advanced</b> | Disable driver/software download from Windows Error reporting servers. | <b>Group Policy:</b> Enable <em>"Prevent Windows from sending an error report when a device driver request additional software during installation"</em> in <em>Computer Configuration/Administratrive templates/System/Device installation</em>. | This feature might leak information about your device. |
| <b>Advanced</b> | Disable automatic driver and related software installations. | <b>Group policy:</b> Enable <em>"Prevent device metadata retrieval from the Internet"</em> in Computer Configuration/Administratrive templates/System/Device installation. | This feature might leak information about your device and might lead to unexpected software being installed. | 
| <b>Advanced</b> | Disable background error reports from being sent when installing a driver. | <b>Group policy:</b> Enable <em>"Do not send a Windows error report when a generic driver is installed on a device"</em> in <em>Computer Configuration/Administrative templates/System/Device installation</em>. | This feature might leak information about your device. |
| <b>Advanced</b> | Disable IP source routing, for both IPv4 and IPv6! | <b>Registry:</b> Set/Create DWORD key <em>"HKLM/SYSTEM/CurrentControlSet/Services/Tcpip/Parameters/IPEnableRouter"</em> with value <em>"0"</em> <b>AND</b> <em>"HKLM/SYSTEM/CurrentControlSet/Services/Tcpip/Parameters/disableipsourcerouting"</em> with value <em>"2"</em> | IP source routing allows the information in network packages to dictate the routing of its traffic. This is might result in traffic avoiding network gateways.
| <b>Advanced</b> | Disable automatic elevated(Admin privileges) installations. | <b>Group policy:</b> Disable <em>"Always install with elevated privileges"</em> in <em>Computer Configuration/Policies/Administrative Templates/Windows Components/Windows Installer</em>. | |
| <b>Advanced</b> | Remove Windows Features you don't need. | Uninstall features in <em>Control Panel/Programs and Features/Turn Windows features on or off</em>. | |
| <b>Advanced</b> | Enable remote restrictions for UAC. | <b>Registry:</b> Set/Create DWORD key <em>HKLM/SOFTWARE/Microsoft/Windows/CurrentVersion/Policies/System/LocalAccountTokenFilterPolicy</em> with value <em>"0"</em>
| <b>Advanced</b> | Disable all unncesseary scheduled tasks. | Go trough your scheduled tasks, including all sub-libraries, and disable unneccesary tasks. | A lot of 3rd party applications creates infringing and unneccesary scheduled tasks.
| <b>Advanced</b> | Use a software firewall. | Use one that can allow/block both incoming and outgoing traffic.
| <b>Expert</b> | Disable insecure protocols. | Disable SMB, SSL, PCT 1.0 and TLS 1.0/1.1/1.2. | <b>See</b> guide https://docs.microsoft.com/en-us/windows-server/securty/tls/tls-registry-settings#tls-dtls-and-ssl-protocol-version-settings <b>AND</B> https://docs.microsoft.com/en-us/windows-server/storage/file-server/troubleshoot/detect-enable-and-disable-smbv1-v2-v3 <br></br> <b>NOTE:</b> Use <b>SFTP</b> instead of SMB, or if you really have to use it, disable 1.0 and leave 2.0/3.0 enabled. |
| <b>Expert</b> | Clean up your certificate trust store. | Run <b>certmgr.msc</b> as an administrator and look in <em>"Trusted Root Certification Authorities/Certificates"</em> and <em>"Intermediate Certification Authorities/Certificates"</em>. | <b>NOTE:</b> Delete certificates from CAs run by governments and affiliates and organisations you don't trust. 
| <b>Expert</b> | Disable automatic driver installation for plugged in devices. | <b>Group policy:</b> Enable <em>"Prevent installation of devices not described by other policy settings"</em> <b>AND</b> enable <em>"Allow installation of devices that match any of these device instance IDs"<em> and specify already installed device instances IDs. Both policies can be found in <em>Computer Configuration/Administratrive templates/System/Device installation/Device installation restrictions.</em>
| Standard | Adjust Windows privacy settings. | Set the features in Windows settings listed below  ↓ |  | |
<pre>
<code>
<b>Windows Settings:</b>
	System \ Clipboard
		Clipboard history = Off
	Time & Language \ Typing \ Typing insights
		Typing insights = Off
      	Privacy & Security \ General
                Let apps show me personalised ads by using my advertisting ID = Off
                Let websites show me locally relevant content by accessing my language list = Off
                Let Windows improve Start and search results by tracking app launches = Off
                Show me suggested content in the Settings app = Off
        Privacy & Security \ Speech
                Online speech recognition = Off
        Privacy & Security \ Inking & Typing personalisation
                Personal Inking and typing dictionary = Off
        Privacy & Security \ Diagnostics & feedback
                Send optional diagnostic data = Off
                Tailored expierences = Off
        Privacy & Security \ Activity history
                Store my activity history on this device = Off
                Send my activity history to Microsoft = Off
        Privacy & Security \ Safe permissions
                SafeSearch = Off
                Microsoft account = Off
                Work or School account = Off
                Search history on this device = Off
                Show search highlights = Off
</code>
</pre>

<table>
    <tr>
        <td><b>Advanced</b></td>
        <td>Disable unneccesary services.</td>
        <td>Run <b>services.msc</b> as an administrator and disable the services listed below ↓</td>
	    <td><b>NOTE:</b> Some <b>features and functions may stop working</b>, and no garantue can be given against that. I've been testing it for about 1 year on my Windows installation, but that's limited to my scenario of Windows usage.

Functions you use could be depedent on some of these services (Not seen in the Dependencies tab or neccesarly intepretable by the service name or its documented purpose). Therefore you should be observant in case that some feature or function stops working.</td>
    </tr>
</table>
<pre>
<code>
	ActiveX Installer
	AllJoyn Router Service
	Auto Time Zone Updater
	BranchCache
	Cellular Time
	Clipboard User Service
	Connected Devices Platform Service
	Connected Devices Platform User Service
	Connected User Experiences and Telemetry
	Function Discovery Resource Publication
	(If you don't use Windows recording or streaming.) GameDVR and Broadcast User Service.
	Geolocation Service
	Retail Demo Service
	User Experience Virtualization Service
	Windows Error Reporting Service
	(Unless a NPS/Radius server) Routing and Remote Access
	(Unless in SharedPC mode) Shared PC Account Manager
</code>
</pre>

<table>
    <tr>
        <td><b>Advanced</b></td>
        <td>Enable the Virtualization Based Security (VBS) features listed below ↓</td>
	<td></td>
	<td></td>
    </tr>
</table>
<pre>
<code>
	<b>Group Policy: Computer Configuration\Administrative templates\System\Device Guard</b>
	Enable "Turn On Virtualization Based Security" 	
	Set options:
        	Secure Boot and DMA protection
        	Enable Virtualization Based Protection of Code Integrity(HVCI) with UEFI Lock.
        	Enable the option "Require UEFI memory attribute tables" to make sure HVCI is only enabled for compatible devices.
        	Enable secure Launch.
</code>
</pre>

<br></br>
<br></br>
<a name="Browse"></a>
# 	Web Browsing
| Level | Title | Description | Note |
| :---        |    :----:   |    :----:   |         ---: |
| Standard | Use a VPN! | Use a VPN when you want to keep your internet connection private, and when you connect to a public Wifi. | <b>NOTE:</b> Use the VPN providers DNS server to make sure the traffic and logs are contained at one provider. <b>OpenVPN:</b> Add the parameter <em>"block-outside-dns"</em> to your config file to block lookups to the ISPs DNS server and prevent that kind of leak. |
| <b>Advanced</b> | Encrypt your DNS lookups | Encrypt your DNS lookups when not connected to a VPN tunnel. I recommend using the DnscryptV2 protocol and <a href="https://github.com/DNSCrypt/dnscrypt-proxy"><b>dnscrypt-proxy</b> <img width="30" height="30" src="https://b.thumbs.redditmedia.com/xLIzuCm3dBa7aboYMPFE8YEk96OB17qk4BXo9x6HzVY.png"></img></a> client for Windows, MacOS and routers(Linux based) and <a href="https://apps.apple.com/us/app/dnscloak-secure-dns-client/id1452162351"><b>DNSCloak</b> <img width="30" height="30" src="https://is3-ssl.mzstatic.com/image/thumb/Purple116/v4/0f/8c/91/0f8c9109-4ae6-baf6-4527-009c700dac0c/source/512x512bb.jpg"></img></a> for iOS. | <b>NOTE:</b> Use a DNS server that don't log client lookups and have DNSSEC support enabled. 
| <b>Advanced</b> | Use a privacy focused search engine. | I recommend  <a href="https://html.duckduckgo.com"><b>DuckDuckGo</b>  <img width="30" height="30" src="https://e7.pngegg.com/pngimages/124/307/png-clipart-duckduckgo-web-search-engine-google-search-anonymity-eyebrows-miscellaneous-logo.png"></img></a> | <b>NOTE:</b> Don't trust all sites in your search results, don't click on random links. |
| Standard | Use <a href="https://brave.com/"><b>Brave browser</b>  <img width="30" height="30" src="https://cdn.search.brave.com/serp/v1/static/brand/0afc6092b0fe05d8a9414d0b27ee3749523d824099384649a75b6a4c22d1cf54-ogImg.png"></img></a>  for <b>easy</b> security and privacy. | Brave is easy to setup and provides good built-in security and tracking protection. | |
| <b>Advanced</b> | Use <a href="https://www.mozilla.org/en-US/firefox/"><b>Firefox</b>  <img width="30" height="30" src="https://design.firefox.com/product-identity/firefox/firefox/firefox-logo.png"></img></a>  browser for <b>best</b> security and privacy. | Firefox is generally the most secured and private browser if you spend some time configuring it properly, and with extensions you can select what kind of scripts and content are allowed. | <b>NOTE:</b> See the Firefox sections further below for a guide on how to configure it for best security and privacy. |
| <b>Advanced</b> | Use <a href="https://www.torproject.org/"><b>Tor</b>  <img width="30" height="30" src="https://upload.wikimedia.org/wikipedia/commons/c/c9/Tor_Browser_icon.svg"></img></a>  browser as a <b>complement</b> for really sensitive or private browsing. | The Tor browser should be used for the most private browsing sessions, and it's based on Firefox and has the same security and privacy capabilities. | <b>NOTE:</b> See the Tor browser sections further below for a guide on how to configure it for best security and privacy. |

<br></br>
<br></br>
<a name="mail"></a>
# 	Email & Chat
| Level | Title | Description | Note | 
| :---        |    :----:   |    :----:   |        ---: |
| <b>Advanced</b> | Block remote content! | Set email app default behavior to block remote content | Disable remote content and only enable it selectively for emails you trust. | Otherwise you're essentially browsing to a bunch of sites emailed to you, usually without any good protection from the email client. |
| Standard | Don't click unsubscribe. Block instead. | Avoid clicking on unsubscribe links in subsription email. It will give away more information about you. Also, the email could potentially be spoofed and contain a malicious unsubscribe link. |
| <b>Advanced</b> | Email is bad for security, <b>talk on encrypted chats!</b> | I recommend <a href="https://www.signail.org"><b>Signal</b> <img width="30" height="30" src="https://upload.wikimedia.org/wikipedia/commons/5/56/Logo_Signal..png"></img></a> for encrypted chat. Email communication usually includes a hosting provider that can read it. | | Standard | Don't open random files! | Don't open any attached files you don't expect to receive! |
| Standard | Email sender/domain can easily be spoofed! | Don't trust that email comes from the sender/domain you see displayed. <b>Expert:</b> Look in the SMTP headers and see if the SPF,DKIM,DMARC checks passed. Not all use DKIM/DMARC yet. But if the SPF check fails, then the sender is spoofed or they have really bad email security. 
| <b>Advanced</b> | Use a private and secure provider for sensitive Email. | You should use a secure and private provider for sensitive communication that has to be emailed. |
| Standard | Encrypt your mail storage! | Make sure your email application stores its data on a encrypted drive. |  |

<br></br>
<br></br>
<a name="soi"></a>
# 	iOS
| Level | Title | Description | Note | 
| :---        |    :----:   |    :----:   |         ---: |
| Standard | Set a passcode! | Set a passcode, 6 digit PIN minimum, that's hard to guess. | <b>Note:</b> It should be hard to guess even if the maliciour actor knows information about you, such as social security number.
| Standard | Don't jailbreak! | Don't jailbreak your device, to reduce the risk of malicious device takeover. Also, you won't receive automatic iOS updates. |
| <b>Advanced</b> | Use <a href="https://apps.apple.com/us/app/firefox-private-safe-browser/id989804926"><b>Firefox Focus</b>  <img width="30" height="30" src="https://upload.wikimedia.org/wikipedia/commons/7/70/Firefox_Focus_2021_Icon.png"></img></a>  as a <b>first option.</b> | Use Firefox Focus as a first option and standard Firefox for sites not working in it. Firefox Focus has better security and clears cookies between each session. | <b>Note:</b> Enable <em>"Block web fonts"</em>, <em>"Enhanced Tracking Protection"</em> + All block options <b>AND</b> disable <em>"Send usage data"</em>, <em>"Studies"</em>, <em>"URL Autocomplete"</em> and <em>"Get Search Suggestions"</em> |
| Standard | Use  <a href="https://apps.apple.com/us/app/firefox-private-safe-browser/id989804926"><b>Firefox</b>  <img width="30" height="30" src="https://design.firefox.com/product-identity/firefox/firefox/firefox-logo.png"></img></a> | Firefox has very good security and privacy features on iOS. | <b>Note:</b> Enable <em>"Block Pop-up Windows"</em>, <em>"Close Private Tabs"</em>, <em>"Enhanced Tracking Protection"</em> + <em>"Strict (Mode)"</em> <b>AND</b> disable <em>"Show Link Previews"</em>, <em>"Offer to Open Copied Links"</em>, <em>"Send Usage data"</em> and <em>"Studies"</em>. 
| Standard | Uninstall apps you don't need! | Uninstall all apps you don't need, including native ones.
| Standard | Enable automatic updates. | Enable automatic updates for iOS and apps. | |
| Standard | Enable On-Device Mode for the Translate app. | <b>Enable</b> On-Device Mode in Translate system settings.
| Standard | Disable iCloud sync of data you don't need. | Disable syncronization of data to iCloud in system settings, for each app and feature you don't need synced to iCloud. |
| Standard | Avoid side-loading apps! | Only side-load apps from sources you really trust. |  |
| Standard | Disable Siri scanning for apps. | <b>Disable</b> <em>"Learn from this app"</em> in the app system settings and Siri section for all installed apps. | |
| <b>Advanced</b> | Don't use Find My Iphone unless you really need it! | <b>Disable</b> Find My Iphone in iCloud system settings. | Minimize the amount of tracking in your phone including location tracking. | 
| Standard | Don't auto-join hotposts | <b>Disable</b> Auto-Join Hotspot in Wifi system settings.
| Standard | Set a SIM PIN. | Make sure a PIN code is set on your SIM card.
| Standard | Disable notification previews when locked. | <b>Set</b> Show Previews to <em>"When Unlocked"</em>. | You don't want others to see your notification content if your phone gets stolen. |
| Standard | Disable Siri if you don't need it. | <b>Settings:</b> Disable Siri from the Siri system settings. | Siri might leak sensitive data, even if it's a fairly secure voice control infrastructure design.
| Standard | Disable or limit Airdrop. | <b>Disable</b> Airdrop if not used or limit it to <em>"Contacts only"</em> in system settings. |
| Standard | Disable CarPlay while locked. | <b>Disable</b> <em>"Allow CarPlay While Locked"</em> in CarPlay system settings. |
| Standard | Require "eye contact" to use FaceID. | <b>Enable</b> <em>"Require Attention for Face ID"</em> in Accessibility system settings. |
| Standard | Disallow access to features when locked. | <b>Disable</b> everything in <em>"Allow Access when locked"</em> in Face ID & Passcode system settings. |
| Standard | Configure your in-app settings security and privacy settings. | Go trough each applications privacy and security settings first thing you do after installing it. | There's often a lot of of privacy settings. |
| Standard | Erase data on multiple failed passcode attempts. | <b>Enable</b> <em>"Erase data"</em> | <b>NOTE: </b>Your iPhone will be reset and all data will be erased after 10 failed passcode attempts.
| Standard | Disable Location Services or only allow it while using the app. | <b>Disable</b> Location Service for apps, <B>OR</B> only allow it while using the app. This is can be set per app in <em>Privacy/Location Service</em> system settings. |
| Standard | Disable telemetry | <b>Disable</b> <em>"Share iPhone & Watch Analytics"</em> in <em>Privacy/Analytics & Improvements</em> system settings.
| Standard | Disable personalised Ads | <b>Disable</b> <em>"Personalised Ads"</em> in <em>Privacy/Apple Advertising</em> system settings. |
| Standard | Disable Personalised Recommendations in App Store. | <B>Disable</b> <em>"Personalised Recommendations"</em> in App Store account settings. |

<br></br>
<br></br>
<a name="Network"></a>
# 	Network and Router
| Level | Title | Description | Note | 
| :---        |    :----:   |    :----:   |         ---: |
| Standard | Secure password for your Wifi! | Set a long and complex password for connecting to the Wifi.  |  |
| Standard | WPA2/WPA3 support! | Enable WPA3 security on your router, or as minimum WPA2, if not supported.  | <b>NOTE:</b> WPA3 should be a requirement for new routers you buy!
| Standard | Secure password for router managentment. | Set a long and complex password on the account used to access your router management interfaces.
| <b>Advanced</b> | Block ping on router. | There's no reason to allow clients on the internet to ping and discover your router. | <b>NOTE:</b> Not all routers have the option to block ping (ICMP Echo).  |
| Standard | Use a VPN! | Use a VPN when you want to keep your internet connection private, and when you connect to a public Wifi. | <b>NOTE:</b> Use the VPN providers DNS server to make sure the traffic and logs are contained at one provider. <b>OpenVPN:</b> Add the parameter <em>"block-outside-dns"</em> to your config file to block lookups to the ISPs DNS server and prevent that kind of leak. | 
| <b>Advanced</b> | Encrypt your DNS lookups | Encrypt your DNS lookups when not connected to a VPN tunnel. I recommend using the DnscryptV2 protocol and <a href="https://github.com/DNSCrypt/dnscrypt-proxy"><b>dnscrypt-proxy</b> <img width="30" height="30" src="https://b.thumbs.redditmedia.com/xLIzuCm3dBa7aboYMPFE8YEk96OB17qk4BXo9x6HzVY.png"></img></a> client for Windows, MacOS and routers(Linux based) and <a href="https://apps.apple.com/us/app/dnscloak-secure-dns-client/id1452162351"><b>DNSCloak</b> <img width="30" height="30" src="https://is3-ssl.mzstatic.com/image/thumb/Purple116/v4/0f/8c/91/0f8c9109-4ae6-baf6-4527-009c700dac0c/source/512x512bb.jpg"></img></a> for iOS. | <b>NOTE:</b> Use a DNS server that don't log client lookups and have DNSSEC support enabled. 
| Standard | Enable the router firewall! | Enable the firewall on your router so to only allow incoming traffic that you need. |  |
| Standard | Update your routers and APs! | Enable auto-update or regulary update the firmware on your routers and access points. | These devices are exposed by nature and need to stay updated from new vulnerabilities. <b>NOTE:</b> Don't use any unsupported routers or access points that don't receive security patches from the vendor!
| <b>Advanced</b> | Create a guest wifi zone. | Set up a separate guest wifi SSID (With password) for devices you dont own and less secure devices such as mobile phones. The guest wifi zone must be isloated from the internal wifi. |  |
| <b>Advanced</b> | Don't broadcast your SSID. | It makes it somewhat harder for evil neighbours to hack your network. |  |
| Standard | Disable WPS PIN on your router! | WPS is a protocol for easy Wifi setup, and WPS PIN is one of its method that has a serious security vulnerability where the PIN can be extracted by a malicious actor. |  |
| Standard | Don't expose any devices! | Don't put any computers or other devices in front of the router/firewall. Unless it's intended for the public. | Hackers countinesly scan the internet for exposed services and target them.
| Standard | Don't expose your router management interfaces! | Keep the router management interfaces, no matter what network protocol, accessible from the internal LAN only. | |
| Standard | Disable unnecessary features on your router! | Disable all your router and access point features you don't need, since they just increase the attack vector. | Extra important on a router since it's exposed on the internet and many typical routers come with bloatware. <b>NOTE #1:</b> This also applies to security features that risk leaking information to its provider, such as HTTP protections that scan all URLs and uploads them to a 3rd party. <br></br> <b>NOTE #2:</b> Don't use built-in file sharing features on your router. File sharing should be setup on a secure server or NAS, and I recommend <b>SFTP</b> for this. |
| Standard | Disable logging of sensitive data on your router! | Some routers log sensitive data, such as web/http traffic and DNS lookups. Disable all these.
| <b>Expert</b> | Install a secure and customizable open source firmware! | For secure and customizable firmware I recommend:<br></br> <a href="https://openwrt.org/"><b>Open-WRT</b>  <img width="30" height="30" src="https://avatars.githubusercontent.com/u/2528830?s=200&v=4"></img></a>  or<br></br><a href="https://dd-wrt.com/"><b>DD-WRT</b>  <img width="156" height="30" src="https://dd-wrt.com/wp-content/themes/dd-wrt/assets/images/logo.png"></img></a> |
| <b>Advanced</b> | Disable the CTF/NAT acceleration feature. | Disable Cut-Through Forwarding/NAT acceleration on your router. | These features allows for traffic to bypass internal firewall scanning and other potential security features. |
| <b>Advanced</b> | Disable UPNP on your router. | | UPNP could allow a potentially infected device on your network to open up network ports allowing malicious traffic from the internet.|

<br></br>
<br></br>
<a name="FirefoxTor"></a>
# 	Firefox & Tor Browser
### The configuration below applies to both the Firefox and Tor browser. See sections further below for configurations specific to each browser.
##### Some security measures require you to install an extension while other require changes in the settings or config editor. The config editor can be accessed by entering <em>about:config</em> into the URL/search bar.

| Level | Title | Description | Note | 
| :---        |  :----:   |    :----:   |         ---: |
| <b>Expert</b> | Remove untrusted CA certificates in root store. | <b>Settings:</b> Uncheck certificates in Privacy & Security/View Certificates. | <b>NOTE:</b> Remove certificates from CAs run by governments and affiliates and organisations you don't trust. Firefox has its own certificate root store (Outside the operating system root store). |
| <b>Advanced</b> | Enforce HTTPS by rejecting sites not supporting TLS encryption. | <b>Settings:</b> Enable HTTPS-only mode |
| Standard | Block fingerprinting from web sites | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/canvasblocker/"><b>CanvasBlocker</b></a> <b>AND</b> <b>Config editor:</b> privacy.resistFingerprinting = <em>"true"</em>, privacy.trackingprotection.fingerprinting.enabled = <em>"true"</em> |
| Standard | Block trackers | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search"><b>uBlock Origin</b></a> <b>AND</b> <b>Config editor:</b> privacy.trackingprotection.enabled = <em>"true"</em>
| Standard | Block cryptominers embeeded in sites. | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search"><b>uBlock Origin</b></a> <b>AND</b> <b>Config editor:</b> privacy.trackingprotection.cryptomining.enabled = <em>"true"</em> |
| <b>Advanced</b> | Only run the content you need from sources you trust! | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/noscript/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search"><b>NoScript</b></a> | Selectively permitt neccesary content types, for example scripts and CSS, only on domains you trust.
| <b>Advanced</b> | Disable WebGL. | <b>Config editor:</b> webgl.disabled = <em>"true"</em>, webgl.disable-wgl = <em>"true"</em>, webgl.enable-webgl2 = <em>"false"</em> | There are vulnerabilities in the API thare are unpatchable.
| <b>Advanced</b> | Use containers for domains/sites with sensitive data/cookies. | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/multi-account-containers/"><b>Multi Account Containers</b></a> | This will minimize the risk of cookies from one domain, eg. sign-in cookies, leaking to another, even if Firefox has built-in protection for that(Cookie isolation).
| <b>Advanced</b> | Auto-delete cookies, with option to whitelist domains | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/cookie-autodelete/"><b>Cookie AutoDelete</b></a> | You will must probably browse many sites in a mixed un-contained browsing session. That's why it's good to keep those browsing cookies temporarly only. |
| <b>Advanced</b> | Prevent Etag tracking | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/chameleon-ext/"><b>Chameleon</b></a> |
| <b>Advanced</b> | Spoof/fake your user agent to prevent tracking. | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/chameleon-ext/"><b>Chameleon</b></a> | Chameleon lets you randomize a user agent within a specified internval. |
| <b>Advanced</b> | Protect yourself from CSS based exfiltration. | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/css-exfil-protection/"><b>CSS exfil protection</b></a> |  |
| Standard | Prevent tracking from URL properties. | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/clearurls/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search"><b>ClearURLs</b></a> <b>AND</b> <b>Config editor:</b> network.http.referer.XOriginPolicy = <em>"2"</em>, network.http.referer.XOriginTrimmingPolicy = <em>"2"</em>, network.http.sendRefererHeader = <em>"0"</em>, network.http.sendSecureXSiteReferrer = <em>"false"</em> | This prevents tracking from things like cross-domain referall links, by cleaning up URLs and HTTP headers from these properties.
| <b>Advanced</b> | Disable WebRTC to prevent IP leaks. | <b>Config editor:</b> disable/media.peerconnection.enabled = <em>"false"</em>
| <b>Advanced</b> | Prevent tracking through requests done to centralized content delviery networks(CDN) such as Google or Cloudflare. | <b>Extension:</b> <a href="https://addons.mozilla.org/en-US/firefox/addon/decentraleyes/"><b>Decentraleyes</b></a> | Decentraleyes will serve local files to keep sites working. |
| <b>Advanced</b> | Prevent URL/search bar tracking. | <b>Config editor:</b> browser.urlbar.speculativeConnect.enabled = <em>"false"</em> | The setting will disable pre-emptive DNS lookups for domains you enter in the URL/search bar. |
| <b>Advanced</b> | Disable snippets on the home/start page. | <b>Config editor:</b> browser.aboutHomeSnippets.updateUrl = <em>BLANK</em> | These snippets will generate HTTP traffic from your browser when you open the home/start page.
| <b>Advanced</b> | Disable network captive portal redirect | <b>Config editor:</b> network.captive-portal-service.enabled = <em>"false"</em> | This should be disabled since you can't be sure what site the public Wifi redirects you to upon connecting. |
| <b>Advanced</b> | Disable network state probing. | <b>Config editor:</b> network.connectivity-service.enabled = <em>"false"</em> | This feature will generate HTTP traffic to test network connectivity from your browser when the network state changes. | 
| <b>Advanced</b> | Disable speculative pre-connection. | <b>Config editor:</b> network.http.speculative-parallel-limit = <em>"0"</em>, network.prefetch-next = <em>"false"</em>, network.dns.disablePrefetch = <em>"true"</em>, network.dns.disablePrefetchFromHTTPS = <em>"true"</em>, network.predictor.enabled = <em>"false"</em>, network.predictor.enable-prefetch = <em>"false"</em> | This feature will fetch links preemptively on link previews/mouse hover. | 
| <b>Advanced</b> | Disable built-in regional detection feature. | <b>Config editor:</b> browser.region.update.enabled = <em>false</em>, browser.region.local-geocoding = <em>false</em>, browser.region.network.url = <em>BLANK</em> | This feature might leak information about you/your device. |
| <b>Advanced</b> | Disable IP-based geolocation when browsing. | <b>Config editor:</b> browser.search.geoip.url = <em>BLANK</em> | |
| Standard | Disable experimental feature. | <b>Config editor:</b> messaging-system.rsexperimentloader.enabled = <em>"false"</em> | You should avoid experimental/beta features since they're not neccesarily secure enough until they become generally available. |	
| <b>Advanced</b> | Disable Activity Stream in Firefox. | <b>Config editor:</b> browser.newtabpage.activity-stream.feeds.asrouterfeed = <em>"false"</em> | Activity Stream might leak information about your page visists. |
| <b>Advanced</b> | Block DRM content. | <b>Settings:</b> Disable playback of DRM content <b>AND</b> <b>Config editor:</b> media.eme.enabled = <em>"false"</em>, media.gmp-widevinecdm.enabled = <em>"false"</em>, media.gmp-widevinecdm.visible = <em>"false"</em> | Playing DRM content also means your running code on in your browser you can't review (Closed source). |
| <b>Advanced</b> | Block the browser from enumerating hardware devices. | <b>Config editor:</b> media.navigator.enabled = <em>"false"</em> | This function leak information about your device. |
| <b>Advanced</b> | Block storing of extra information in Firefox Session Restore feature. | <b>Config editor:</b> browser.sessionstore.privacy_level = <em>"2"</em> | This function stores information such as cookies, form values and HTTP POST data.
| <b>Advanced</b> | Prevent IDN exploits by displaying raw Punnycode. | <b>Config editor</b>: network.IDN_show_punycode = <em>"true"</em> | See more information about the vulnerability and workaround here https://www.mozilla.org/en-US/security/advisories/mfsa2005-29/ |
| <b>Advanced</b> | Disable cached browsing. | <b>Config editor:</b> browser.cache.memory.enable = <em>"false"</em>, browser.cache.disk.enable = <em>"false"</em> | This feature might lead to information about your browsing being saved without your knowledge, even if temporarly. |
| Standard | Send "Do not track". | <b>Settings:</b> Enable <em>"Do not track"</em>. | Not all sites follows this request/header. But it should still be enabled.
| <b>Advanced</b> | Prevent native data collection and leaking. | <b>Set config editor</b> properties listed below ↓</td> | Disable Firefox built-in data collection and potential data leaking features, such as telemetry. |
<pre>
<code>
app.normandy.optoutstudies.enabled = <em>"false"</em>
app.shield.optoutstudies.enabled = <em>"false"</em>
extensions.getAddons.cache.enabled = <em>"false"</em>
browser.send_pings = <em>"false"</em>
dom.event.clipboardevents.enabled = <em>"false"</em>
beacon.enabled = <em>"false"</em>
app.normandy.enabled = <em>"false"</em>
browser.ping-centre.telemetry = <em>"false"</em>
toolkit.telemetry.bhrPing.enabled = <em>"false"</em>
toolkit.telemetry.firstShutdownPing.enabled = <em>"false"</em>
toolkit.telemetry.healthping.enabled = <em>"false"</em>
toolkit.telemetry.newProfilePing.enabled = <em>"false"</em>
toolkit.telemetry.shutdownPingSender.enabled = <em>"false"</em>
toolkit.telemetry.updatePing.enabled = <em>"false"</em>
toolkit.telemetry.archive.enabled = <em>"false"</em>
toolkit.telemetry.enabled = <em>"false"</em>
toolkit.telemetry.rejected = <em>"true"</em>
toolkit.telemetry.unified = <em>"false"</em>
toolkit.telemetry.unifiedIsOptIn = <em>"false"</em>
toolkit.telemetry.prompted = <em>"2"</em>
toolkit.telemetry.rejected = <em>"true"</em>
datareporting.healthreport.uploadEnabled = <em>"false"</em>
browser.crashReports.unsubmittedCheck.autoSubmit2 = <em>"false"</em>
browser.crashReports.unsubmittedCheck.autoSubmit = <em>"false"</em>
browser.crashReports.unsubmittedCheck.enabled = <em>"false"</em>
browser.tabs.crashReporting.includeURL = <em>"false"</em>
browser.tabs.crashReporting.sendReport = <em>"false"</em> 
dom.ipc.plugins.flash.subprocess.crashreporter.enabled = <em>"false"</em>
dom.ipc.tabs.createKillHardCrashReports = <em>"false"</em>
</code>
</pre>

<br></br>
<br></br>
<a name="Firefox"></a>
# 	Firefox (Specific)
##### Some security measures require you to install an extension while other require changes in the settings or config editor. The config editor can be accessed by entering <em>about:config</em> into the URL/search bar.
| Level | Title | Description | Note | 
| :---        |  :----:   |    :----:   |         ---: |
| <b>Advanced</b> | Disable 3rd party cookies. | <b>Config editor:</b> network.cookie.cookieBehavior = <em>"1"</em> | To prevent sites on different domains from reading share each others cookies. |

<br></br>
<br></br>
<a name="Tor"></a>
# 	Tor Browser (Specific)
##### Some security measures require you to install an extension while other require changes in the settings or config editor. The config editor can be accessed by entering <em>about:config</em> into the URL/search bar.

| Level | Title | Description | Note | 
| :---        |  :----:   |    :----:   |         ---: |
| <b>Advanced</b> | Disable all cookies. | <b>Config editor:</b> network.cookie.cookieBehavior = <em>"2"</em> | Don't keep any persistent cookies in the Tor browser sessions. |

<br></br>
<br></br>
<a name="Thunderbird"></a>
# 	Thunderbird Email
##### Some security measures require you to install an extension while other require changes in the settings or config editor. The config editor can be accessed by entering <em>about:config</em> into the URL/search bar.
| Level | Title | Description | Note | 
| :---        |  :----:   |    :----:   |         ---: |
| <b>Advanced</b> | Disable remote content. | <b>Settings:</b> Disable remote content. | <b>NOTE:</b> This will prevent Thunderbird from loading any content not directly attached to the email, thus preventing leaks when you read an email. |
| <b>Advanced</b> | Disable speculative pre-connection. | <b>Config editor:</b> network.http.speculative-parallel-limit = <em>"0"</em>, network.prefetch-next = <em>"false"</em>, network.dns.disablePrefetch = <em>"true"</em>, network.dns.disablePrefetchFromHTTPS = <em>"true"</em>, network.predictor.enabled = <em>"false"</em>, network.predictor.enable-prefetch = <em>"false"</em> | This feature will fetch links preemptively on link previews/mouse hover. | 
| <b>Advanced</b> | Prevent native data collection and leaking. | <b>Set config editor</b> properties listed below ↓</td> | Disable Thunderbirds built-in data collection and potential data leaking features, such as telemetry. |
<pre>
<code>
app.normandy.optoutstudies.enabled = <em>"false"</em>
app.shield.optoutstudies.enabled = <em>"false"</em>
extensions.getAddons.cache.enabled = <em>"false"</em>
browser.send_pings = <em>"false"</em>
dom.event.clipboardevents.enabled = <em>"false"</em>
beacon.enabled = <em>"false"</em>
app.normandy.enabled = <em>"false"</em>
browser.ping-centre.telemetry = <em>"false"</em>
toolkit.telemetry.bhrPing.enabled = <em>"false"</em>
toolkit.telemetry.firstShutdownPing.enabled = <em>"false"</em>
toolkit.telemetry.healthping.enabled = <em>"false"</em>
toolkit.telemetry.newProfilePing.enabled = <em>"false"</em>
toolkit.telemetry.shutdownPingSender.enabled = <em>"false"</em>
toolkit.telemetry.updatePing.enabled = <em>"false"</em>
toolkit.telemetry.archive.enabled = <em>"false"</em>
toolkit.telemetry.enabled = <em>"false"</em>
toolkit.telemetry.rejected = <em>"true"</em>
toolkit.telemetry.unified = <em>"false"</em>
toolkit.telemetry.unifiedIsOptIn = <em>"false"</em>
toolkit.telemetry.prompted = <em>"2"</em>
toolkit.telemetry.rejected = <em>"true"</em>
datareporting.healthreport.uploadEnabled = <em>"false"</em>
browser.crashReports.unsubmittedCheck.autoSubmit2 = <em>"false"</em>
browser.crashReports.unsubmittedCheck.autoSubmit = <em>"false"</em>
browser.crashReports.unsubmittedCheck.enabled = <em>"false"</em>
browser.tabs.crashReporting.includeURL = <em>"false"</em>
browser.tabs.crashReporting.sendReport = <em>"false"</em> 
dom.ipc.plugins.flash.subprocess.crashreporter.enabled = <em>"false"</em>
dom.ipc.tabs.createKillHardCrashReports = <em>"false"</em>
</code>
</pre>

<br></br>
<br></br>
<br></br>




