# Code for Berkeley Homelessness Project

## Dev Instructions

Open a terminal

Optional: Only if you aren't sure if you have Homebrew installed already

	ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

May ask for a password. This is your 'sudo', or root, password. Usually this is just the password you use to login to your computer, unless you set up a different root password in the past.

Install node:
	
	brew install node

Use nvm:
	
	nvm use

If this doesn't work for some reason, try:

	brew install nvm
	nvm use

Install yarn:

	brew install yarn

Install package dependencies:

	yarn install

Launch the app on localhost:

	npm run serve

This might not work due to your machine's admin security protocols. If it doesn't, run:

	sudo npm run serve

* Note: On my machine, this opens in Safari even though I have my default browser set to Chrome. If you want to be able to use Chrome's DevTools by viewing the app in Chrome, just open up a Chrome window and navigate via address bar to localhost:80

## Troubleshooting

Whenever you open the app, make sure to close it completely from your terminal with ctrl-c. If you don't fully shut down the app and try to reopen it, you may get an EADDRINUSE 127.0.0.1:80 error when trying to execute 'npm run serve' again. In order to fix this issue, do the following:

	lsof -i tcp:80

Find the number listed under 'PID'

	sudo kill -9 INSERT FOUND PID HERE
	sudo npm run serve
