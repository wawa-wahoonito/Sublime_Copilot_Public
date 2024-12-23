# Install Copilot for Sublime Editor:

Date: December 1st, 2024


This file aims to explain how to use copilot in sublime environment. This is suitable for those <ins>who do not wish to use VSCode editor</ins> (default copilot editor). Or stubborn Sublime users who are not into switching editors. The pro is that sublime is much faster than VSCode, also it does not subject to frequent update that makes editing difficult. The con is that sublime is not as user-friendly as VSCode. 


Make sure the following is done: 

1. sublime is installed 
2. copilot is purchased and installed (using education account or personal github account)

The next few steps involve: 
	
1. Installing Node-js runtime
2. Installing two pacakges in sublime (LSP and LSP-copilot) and setting them up

Also, this Readme is written for PC. For MacOS users, replace all "Ctrl" with "⌘" 


## Part 1: Download the latest sublime (needs to be 4 or above)

1. Copilot needs sublime 4 or above 
	
	- You can either download the new version, or click "Help" -> "Check for Updates" to update the sublime 
	
2. Next, make sure other similar AI tools (such as tabnine) are removed: 

	- For example: Shift + Ctrl + P for package control 
	- Remove package "tabnine"
	- Restart sublime to make sure tab9 is probably uninstalled



## Part 2: Install Node js runtime 
	

- Agree with everything and install it in the default location
- No need to check "Auto install necessary tools. Note that... Chocolatey.. etc." Otherwise you will be propmted to install chocolatey in Windows PowerShell environment which may take a long time, and you may still need to cancel the installation 



## Part 3: Install LSP, LSP-copilot, Sign-in Copilot, Change settings for LSP and LSP-copilot 

1. Install LSP (before installing anything)

	- Again, the usual Shift + Ctrl + P for LSP installation
	- Need to close sublime if you forgot to install node-js before this step. Otherwise, LSP-copilot in the next step won't be installed.

2. Install LSP-copilot 

 	- This only works if both Node-js and LSP are installed 
 	- Again, the usual Shift + Ctrl + P for LSP-copilot installation
	- Close sublime before next step 

3. Allow Copliot to Sign in

	- a. Ctrl + N to open an empty file. The next steps won't work if you don't pretend you are working on a file..
	- b. Type Shift + Ctrl + P: Search "Copilot Sign in" or just "Sign in"
	- c. A GitHub website will show up on the browser. A message will show up on the sublime. Click ok.
	- d. Sublime will show an 8-digit number. If not, the 8 digit code is stored on the clipboard. Press "Ctrl V" to show the one-time passcode.
	- e. Enter 8 digits on the pop-up GitHub browser. Click ok.
	
	- *Note*: If you do the following which technically seems to be the same, but you may not update the setting propertly.
		- "Preference -> Package setting -> LSP -> Server -> LSP copilot -> Sign In" 


4. Change LSP user setting

	- Go to "Preference -> Package setting -> LSP -> Setting" 
	- Paste the following to the right-hand-side, aka user setting: 

		 	{
			"hover_highlight_style": "background",
	  		"clients": {},
	  		"default_clients": {},
	  		"show_code_actions_in_hover": false,
	  		"show_symbol_action_links": false,
		   	}
		
5. Go to LSP-copilot setting (LSP-Server-LSPcopilot-setting)

	- Go to "Preference -> Package setting -> LSP -> Setting" 
	- Paste the following to the right-hand-side, aka user setting: 
				
			{ 	
				"enabled": true,
				"settings": {
				"auto_ask_completions": true,
				"debug": false,
				"hook_to_auto_complete_command": false,
				"local_checks": false,
				"telemetry": false,
				"completion_style": "phantom",
				},
		    }

	

## Part 4: Start Using Copilot:
	
- Similar to VSCode, start writing code, or commennt to start generating code. Use "tab" to accept, "space" to regenerate, any key to reject, and more writing to regenerate as well. 

- Always seperate code directory with data directory, otherwise copilot will try to read your data as code.

- Look at the tiny anime on lower-left corner to know if copilot is thinking

- A practical tips tp turn on and off the setting:
	- Use "disable" and "enable" to reset copilot, when needed 
	- Shift + Ctrl + P 
	- Search "Disable LSP global" or 
	- Search "Enable LSP global"



