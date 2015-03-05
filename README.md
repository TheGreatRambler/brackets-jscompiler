# JSCompiler2 for [Brackets](https://github.com/adobe/brackets)

JSCompiler2 is a tool for [Brackets](https://github.com/adobe/brackets) that allows you to compress and mangle your JavaScript code into one minified file, powered by [UglifyJS2](https://github.com/mishoo/UglifyJS2)

## Features

- Doesn't require previous configurations for quick first use.
- Customize advanced compilation options.
- Compile multiple javascripts into one output.
- Generate multiple outputs at once.
- Works even offline.

## Usage

Simply press the "Compress JavaScript" button on the sidebar, or go to `File > Compress JavaScript`, and your code will be compressed into a `{filename}.min.js` file.

### Advanced options

You can go to `File > Compress JavaScript: Options` to open a JSON file with the compiler options for the currect directory. There you can customize next values:

- **Inputs**: An array of javascript files to be compressed into the minified file.
- **Output**: The name of the resulting minified file.
- **GenerateMap**: A boolean value. If this is false, the source map for the code won't be generated.
- **Mangle**: A boolean value. If this is false, the code won't be mangled.
- **Isolate**: A boolean value. If this is true, the resulting code will be isolated so it won't affect or be affected by other scripts.

If the isolate option is true, the resulting code will be wrapped with the next code:

```javascript
(function(window, undefined){
   // Your compiled code
})(window);
```

You can create multiple outputs by adding more JSON objects to the main **outputs** array.

Also, you can customize the default template for new projects at `File > Compress JavaScript: Options template`. Careful! This is only for advanced users. Updates will restore the template to prevent unexpected crashes.

## Special thanks

Special thanks to Steffen Bruchmann and Peter Flynn, who helped me a lot on my first steps with brackets extension development.

Special thanks also to miladd3, elegos, mrmckeb, kevinmerckx and bbak for their support and ideas through GitHub.

And special thanks too to mrmckeb for the new compiler icon.