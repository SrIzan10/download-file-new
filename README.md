# download-file-new

This creates a `d.ts` file so you can use it in your typescript project. Used by [sern CLI](https://github.com/sern-handler/cli.git).

## Install

```shell
npm install download-file-new
```

## Usage

```js
var download = require('dl-file-new')

var url = "http://i.imgur.com/G9bDaPH.jpg"

var options = {
	directory: "./images/cats/",
	filename: "cat.gif"
}

download(url, options, function(err){
	if (err) throw err
	console.log("meow")
}) 
```

## API

### download(url, [options], callback(err))

- __url__ string of the file URL to download 

- __options__ object with options

  - __directory__ string with path to directory where to save files (default: current working directory)
  - __filename__ string for the name of the file to be saved as (default: filename in the url)
  - __timeout__ integer of how long in ms to wait while downloading (default: 20000)

- __callback__ function to run after
