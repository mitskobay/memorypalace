## How to Create QR Codes on a Mac

# Level 1: Create and Run Shortcut
We will use the Shortcuts app ([1]) that comes with MacOS. This will avoid including trackers that third party applications may embed in their QR codes. ([2])
- Open the Shortcuts app (`Finder > Applications > Shortcuts.app`)
- Click `+` button to create a new shortcut
- In search bar, enter "qr"
- Drag `Generate QR Code` into the main panel (or double click)
- Replace `Text` with `Clipboard`
- Clear search bar, locate and drag `Save to Photo Album`
- Notice that the name of the shortcut in the header has also changed to "Save to Photo Album". Click the name and change it to "Create QR Code"
- Done! To test it, copy a web address into the clipboard. Then click the play button (the triangle) on the right side of the header. The QR code appears in the shortcut panel. It should also be in your Photo Album.
- Once you have checked that it works, close the window. This reveals the main Shortcuts window, which contains the new shortcut.
- In practice, you can copy a web address, then open the Shortcuts app and push the play button on your QR code shortcut. Look for the QR code in the Photos app, in the `recents` folder

# Level 2: Make It Convenient

- To automatically open the Photos app after creating the QR code, we can add a new line to our shortcut. Search for "open" and drag `Open App` at the end of our shortcut. Click on `App` and search for `Photos`. Now the Photos app will open each time a QR code is created
- If we anticipate creating QR codes often, we may want to add the shortcut to the dock. To do this, control-click the "Create QR Code" shortcut and select `Add to Dock`
- The dock icon defaults to the shortcut icon, but it would be helpful to replace it with a QR code icon. There is a way to select an icon in the shortcuts app, but for me it only appeared in the app, not in the dock. But do this first. Control-click the shortcut in the Shortcuts app, and select `Change Icon...`. Search "qr". There are, conveniently, two QR code icons to choose from.
- Here's how I finally got the icon visible in Shortcuts to appear in the dock. First, control-click the shortcut in the dock. Select `Options > Show in Finder`. In Finder, control-click the QR code app and select `Get Info`. Next, still in Finder, control-click the QR code app and select `Show Package Contents`. Navigate to `Contents > Resources`. Drag ShortcutIcon.icns to the top of the info panel until the green + icon shows up. Drop the icon there.
- Finally, restart the dock. Open the Terminal app (`Applications > Utilities`), and type `killall Dock` in Terminal. Press `Return`. Quit Terminal and wait for the Dock to restart. The new icon should now appear!

[1]: https://support.apple.com/guide/shortcuts-mac/intro-to-shortcuts-apdf22b0444c/mac
[2]: https://education.apple.com/resource/250011714