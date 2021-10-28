---
title: How to Use an iPad as the Only Display of Mac Mini
tags: 
- Tech
- macOS
---

We all know that Apple provided a feature called Sidecar. In the recent macOs Monterey, the the pane 'Sidecar' disappeared from System Preference App. Actually this feature is still availble through the pane "Display". This article is not to instruct you how to open the sidercar step by step, but to provide a new stable way to automatically open it every time when you open your mac, then for mac mini users who only want to display mac on iPads, your dream could come true. 

## Stop buzzling, show me the code!

``` AppleScript
tell application "System Preferences"
	activate
	delay 0.5
	set the current pane to pane id "com.apple.preference.displays"
	beep 1
	delay 2
	tell application "System Events"
		tell process "System Preferences"
			tell first window
				tell first pop up button
					click
					click menu item "name_of_the_iPad" of menu 1
					-- replace "name_of_the_iPad" into your iPad name 
				end tell
			end tell
		end tell
	end tell
	quit
end tell
```