Note: All these instructions are for Mac machines. If anyone has a Windows machine and this doesn't work, feel free to message me and I'll help you figure it out. :)

1. Open a terminal
2. Optional: Only if you aren't sure if you have Homebrew installed already
	- In your terminal, run the following: ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	- May ask for a password. This is your 'sudo', or root, password. Usually this is just the password you use to login to your computer, unless you set up a different root password in the past.
3. Install node
	- In your terminal, run the following: brew install node
4. Use nvm
	- Run: nvm use
	- If this doesn't work for some reason, try running the following: brew install nvm
		- Then, retry nvm use
5. Install yarn
	- In your terminal, run: brew install yarn
6. Install package dependencies
	- Run: yarn install
7. Launch the app on localhost!
	- Run: npm run serve
		* This might not work due to your machine's admin security protocols. If it doesn't, run: sudo npm run serve
		* Note: On my machine, this opens in Safari even though I have my default browser set to Chrome. If you want to be able to use Chrome's DevTools by viewing the app in Chrome, just open up a Chrome window and navigate via address bar to localhost:80

*. IMPORTANT
	- Whenever you open the app, make sure to close it completely from your terminal with ctrl-c. If you don't fully shut down the app and try to reopen it, you may get an EADDRINUSE 127.0.0.1:80 error when trying to execute 'npm run serve' again. In order to fix this issue, do the following:
		1. Run: lsof -i tcp:80
		2. Find the number listed under 'PID'
		3. Run: sudo kill -9 INSERT FOUND PID HERE
		4. Try (sudo) npm run serve again
