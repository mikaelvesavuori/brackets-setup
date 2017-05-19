# Brackets setup recommendations
This document serves to give some recommendations for how to set up Brackets for frontend development.

## Extensions
Extensions are usually installed through the Extension Manager found in the File menu. Also, make sure to come back to the Extension Manager once in a while to fetch any updates that may have been released.

All descriptions are taken from the extensions' respective Github pages.

- [Brackets File Tree Exclude](https://github.com/DimitrK/exclude-indexing-filetree): Brackets extension for excluding folders and files from the file tree, find in files, and quick open. This means that the files will be completely invisible to Brackets what will greatly improve overall performance of the editor. This is great for cache folders, distribution/build folders and files, and package manager folders like node_modules and bower_components.
- [Brackets-Git](https://github.com/zaggino/brackets-git): Brackets-Git is an extension for Brackets editor - it provides Git integration for Brackets. It's tested and works on any platform supported by Brackets (Windows, Mac OS X, GNU/Linux).
- [hdy.Brackets-Shell](https://github.com/johnhidey/hdy.brackets-shell/): A brackets extension giving you access to the system shell within brackets.
- [Brackets Tree Icons](https://github.com/mskocik/brackets-tree-icons): This extension adds file and folder (open and close state) icons to the brackets file tree. Based on drewbkoch and his Brackets File Icons project, which is based on ivogabe's Brackets-Icons project.
- [brackets-typescript](https://github.com/fdecampredon/brackets-typescript): A Brackets extension that adds TypeScript support.
- [brackets-eslint](https://github.com/zaggino/brackets-eslint): Brackets extension which provides file linting with ESLint..
- [Command Line Shortcuts for Brackets](https://github.com/antivanov/Brackets-Command-Line-Shortcuts): Brackets IDE plugin. Adds support of shortcuts for execution of terminal commands right from the IDE.
- [CSScomb Brackets plugin](https://github.com/hano/csscomb-brackets): Implementation of CSScomp for Brackets.
- [Indent Guides for Brackets](https://github.com/lkcampbell/brackets-indent-guides): An extension for Brackets to show indent guides in the code editor.
- [Indentator](https://github.com/ahuth/brackets-indentator): Re-indent a document according to your current indentation settings. Useful for converting someone else's style to your own. Run by selecting Indent Document under the Edit menu, or using the Ctrl+Alt+I shortcut.
- [Open in terminal](https://github.com/ranjandatta/brackets-open-in-linux-terminal): Open the project folder in terminal.
- [React (.jsx) language mode for Brackets IDE](https://github.com/apla/brackets-jsx): This module removes original xml and javascript modes from brackets and replaces it with latest version from CodeMirror. After, jsx file extension is disassociated from javascript mode and new jsx mode is created.
- [Shizimily Multi-Encoding for Brackets](https://github.com/Hiromi-Ayase/brackets-shizimily-multiencoding): An extension for Brackets to read and write non UTF-8 encoding file.
- [White Space Sanitizer](https://github.com/MiguelCastillo/Brackets-wsSanitizer): Bring sanity to your code by keeping your indentation (spaces and tabs) consistent; the white space sanitizer.

## Handy stuff to know
- You can easily fold/unfold nested code with the left-most arrow icon (should be located right next to the line numbers if you have those activated)
- `CMD+Left Click`: You can use multiple input markers/cursors – useful for when you need to enter the same text into multiple places
- `CMD+C` / `CMD+V` / `CMD+X`: If you don't have anything selected, these operations will apply to the entire line – super handy when you want to copy or erase things really fast

## Useful shortkeys
- `CMD+E`: Quick Edit code which can save a lot of time – for example giving you direct CSS class access when you have the cursor on a class in an HTML document
- `CMD+UPARROW` or `CMD+DOWNARROW`: Go to top or bottom of the current document
- `CMD+PAGEUP` or `CMD+PAGEDOWN`: Go to next or previous Working File
- `CTRL+OPT+I`: Automatically indent document (Requires **Indent Guides for Brackets**)

## Setting recommendations
- Make sure that Highlight Active Line, Line Numbers and Word Wrap are turned on (View menu)
- I find a dark theme to be much easier on the eyes – haven't tried that before? Do it!
- If you are using **Indent Guides for Brackets** you can specify the color and opacity of indent lines under *brackets-indent-guides.guideColor* in the Preferences menu.

## Use a custom font
Set these up either in View > Themes or in the preferences JSON. You will need to specify the actual font name as it's called in your Font Book (on Mac), or in the Fonts folder (at least I guess that's how it would work on Windows). I've found the following (free!) fonts to be very nice to work with:
- [Fira Code](https://github.com/tonsky/FiraCode)
- [Source Code Pro](https://fonts.google.com/specimen/Source+Code+Pro)
- [Inconsolata](https://fonts.google.com/specimen/Inconsolata)

### Settings example for custom font (brackets.json)
- "fonts.fontSize": "16px"
- "fonts.fontFamily": "'Fira Code', 'SourceCodePro-Medium', ＭＳ ゴシック, 'MS Gothic', monospace"

## Setting up linting
JSLint is on by default in Brackets. If you use ESLint you will get, as a default, get both linters activated and running. You need to set these up a bit if you only want one them. See the below example for how to only use ESLint.

### Settings example for linting (brackets.json)
- "linting.prefer": ["ESLint"]
- "linting.usePreferredOnly": true

## Deep-customizing Brackets
You will be able to reach a ton of settings in two of the JSON files that contain (all?) the settings for Brackets. You can open these by going to Preferences (on a Mac this is located under the Brackets menu item).

The file **defaultPreferences.json** is read-only, so the way you will have to input your custom preferences is to copy-paste (or write new) configurations in the right-hand side file, **brackets.json**. That file will "overwrite" the initial global preferences file. Verify any changes by saving your updated **brackets.json** and reloading Brackets with **CMD+R**.
