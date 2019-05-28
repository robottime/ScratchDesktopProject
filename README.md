# ScratchDesktopProject
Link scratch blocks, gui, and desktop together.

## Preparations

### Prepare `scratch-blocks`
1. `cd scratch-blocks`
2. run `npm install` with access to Google
3. run `npm link`

### Prepare `scratch-gui`
1. `cd scratch-gui`
2. Switch to the `scratch-desktop` branch with `git checkout scratch-desktop`
3. run `npm install`
4. run `npm link scratch-blocks` to include local `scratch-blocks`

### Prepare `scratch-desktop`
1. `cd scratch-desktop`
2. run `npm install`

## Guide to debug or dist

### Make your own blocks
1. Add or modify blocks' description in file `/scratch-blocks/blocks_vertical/robottime.js`
2. Add or modify blocks' scritp generator in file `/scratch-blocks/generators/arduino/click.js`
3. run `npm run prepublish` with access to Google in folder `/scratch-blocks`
4. Add or modify blocks' xml description in file `/scratch-gui/src/lib/make-toolbox-xml.js`

### Change _Arduino_ or _Python_ button's onClick callback
1.  Edit `onOpenArduinoEditor` or `onOpenPythonEditor` in file `/scratch-gui/src/containers/stage-header.jsx`

### build `scratch-gui`
run `set BUILD_MODE=dist` once and `set STATIC_PATH=static` once, then `npm run build`

### debug or dist `scratch-desktop`
* Run in development mode with `npm start`
* Make a packaged build with `npm run dist` and find executable file from _./dist_
