# UnseenMail
Polybar Python script for viewing unread email from multi accounts

Cleaned from the original version to work only with IMAP Protocol.

![](./screenshot/UnseenMail.png) 

# Dependencies
- Polybar
- Python 3
- FontAwesome V4 (see your Distribution font configuration)

# Install

1 - Clone this repo

2 - install all dependencies 

3 - Add following to your polybar configuration file


	  [module/unread_mail]
	  type = custom/script
	  
	  label-font = 2
	  format-underline = #f50a4d
	  click-left=  thunderbird & ; you can set your own client
	  format = <label>
	  exec = python path/to/python/script/UnseenMail.py
	  interval = 100

4 - Add accounts to accounts.ini (in script folder)

	#Configuration example for email accounts
	[Example IMAP]
	protocol=IMAP
	host=imap.gmail.com
	port=993
	useSSL = true
	login = email
	password = password
	icon=
	
5 - Run it !
