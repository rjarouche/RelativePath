## Relative path support for Visual Studio Code
Now you can get the relative path to any file in the workspace.

Just press `Ctrl+Shift+q` (Mac: `Cmd+Shift+q`) and select a file. If your workspace has more than 1000 files, you will be prompted to filter that list first.
Alternatively, you can press open command palette `F1` and search for `jRelative Path`.

![GIF](https://media.giphy.com/media/3oEduJ5iRksPxpwoXC/giphy.gif)

## Important
This is a fork from [https://github.com/jakob101/RelativePath](https://github.com/jakob101/RelativePath).
Now when you are on a PHP or HTML file the path will be in this format
<link rel="stylesheet" type="text/css" href="path-to-css-file.css">
<script type="text/javascript" src="path-to-javascript-file.js"></script>
include 'path-to-php.file'
Other files still in the original behavior


## Important 2

### In Multi root workspaces:

Everytime you switch to a file from a different folder the files in that folder are indexed and
cached to improve search performance. If you have multiple large folders part of a workspace
frequent switches between folders might slow you down.

### In Single project workspace:
The caching of the filelist in the project happens only once. If your workspace contains a lot of files
please wait for the initial file list to be created.

## Options
The following Visual Studio Code settings are available for the RelativePath extension. They can be set in user preferences (`ctrl+,` or `cmd+,`) or workspace settings (.vscode/settings.json).
```javascript
	// An array of glob keys to ignore when searching.
	"relativePath.ignore": [
		"**/node_modules/**",
		"**/*.dll",
		"**/obj/**",
		"**/objd/**"
	],

	// Excludes the extension from the relative path url (Useful for systemjs imports).
	"relativePath.removeExtension": false,

	// An array of extensions to exclude from the relative path url (Useful for used with Webpack or when importing files of mixed types)
	"relativePath.excludedExtensions": [
		".js"
	],
```
## Special thanks to jakob101

## Licence
[MIT](https://github.com/Microsoft/vscode-go/blob/master/LICENSE)
