# UNC Environment Check for Roblox Lua Executors

A comprehensive testing script to verify UNC (Unified Naming Convention) environment compatibility for Roblox Lua executors.

## 📋 Overview

This script tests all standard UNC functions that are commonly implemented in Roblox script executors. It provides detailed feedback on which functions are supported, which are missing, and which aliases are unavailable.

## 🚀 Features

- **Comprehensive Testing**: Tests over 100+ UNC functions across 13 categories
- **Alias Detection**: Checks for common function aliases
- **Detailed Reporting**: Clear visual feedback with emojis
- **Success Rate**: Calculates overall compatibility percentage
- **Non-Blocking**: Uses task.spawn for parallel testing
- **Safe Execution**: All tests are wrapped in pcall for error handling

## 📊 Test Categories

### 1. **Cache Functions**

- `cache.invalidate` - Invalidate instance references
- `cache.iscached` - Check if instance is cached
- `cache.replace` - Replace cached instance
- `cloneref` - Clone instance reference
- `compareinstances` - Compare instance references

### 2. **Closure Functions**

- `checkcaller` - Verify executor context
- `clonefunction` - Clone a function
- `getcallingscript` - Get calling script
- `getscriptclosure` - Get module script closure
- `hookfunction` - Hook and replace functions
- `iscclosure` - Check if C closure
- `islclosure` - Check if Lua closure
- `isexecutorclosure` - Check if executor closure
- `loadstring` - Load and execute Lua code
- `newcclosure` - Create new C closure

### 3. **Console Functions**

- `rconsoleclear` / `consoleclear` - Clear console
- `rconsolecreate` / `consolecreate` - Create console window
- `rconsoledestroy` / `consoledestroy` - Destroy console
- `rconsoleinput` / `consoleinput` - Get console input
- `rconsoleprint` / `consoleprint` - Print to console
- `rconsolesettitle` / `consolesettitle` - Set console title

### 4. **Cryptography Functions**

- `crypt.base64encode` - Encode to Base64
- `crypt.base64decode` - Decode from Base64
- `crypt.encrypt` - Encrypt data
- `crypt.decrypt` - Decrypt data
- `crypt.generatebytes` - Generate random bytes
- `crypt.generatekey` - Generate encryption key
- `crypt.hash` - Hash data (supports SHA1, SHA256, SHA384, SHA512, MD5, SHA3-224, SHA3-256, SHA3-512)

### 5. **Debug Functions**

- `debug.getconstant` - Get function constant
- `debug.getconstants` - Get all function constants
- `debug.getinfo` - Get function information
- `debug.getproto` - Get function prototype
- `debug.getprotos` - Get all function prototypes
- `debug.getstack` - Get stack values
- `debug.getupvalue` - Get upvalue
- `debug.getupvalues` - Get all upvalues
- `debug.setconstant` - Set function constant
- `debug.setstack` - Set stack value
- `debug.setupvalue` - Set upvalue

### 6. **Filesystem Functions**

- `readfile` - Read file contents
- `writefile` - Write to file
- `appendfile` - Append to file
- `loadfile` - Load and execute file
- `dofile` - Execute file
- `listfiles` - List directory contents
- `makefolder` - Create folder
- `delfolder` - Delete folder
- `delfile` - Delete file
- `isfile` - Check if path is file
- `isfolder` - Check if path is folder

### 7. **Input Functions**

- `isrbxactive` / `isgameactive` - Check if Roblox window is active
- `mouse1click` - Simulate left mouse click
- `mouse1press` - Press left mouse button
- `mouse1release` - Release left mouse button
- `mouse2click` - Simulate right mouse click
- `mouse2press` - Press right mouse button
- `mouse2release` - Release right mouse button
- `mousemoveabs` - Move mouse to absolute position
- `mousemoverel` - Move mouse relatively
- `mousescroll` - Simulate mouse scroll

### 8. **Instance Functions**

- `fireclickdetector` - Fire click detector
- `getcallbackvalue` - Get callback function value
- `getconnections` - Get signal connections
- `getcustomasset` - Get custom asset URL
- `gethiddenproperty` - Get hidden property
- `sethiddenproperty` - Set hidden property
- `gethui` - Get hidden UI container
- `getinstances` - Get all instances
- `getnilinstances` - Get instances parented to nil
- `isscriptable` - Check if property is scriptable
- `setscriptable` - Set property scriptability
- `setrbxclipboard` - Set Roblox clipboard

### 9. **Metatable Functions**

- `getrawmetatable` - Get raw metatable
- `hookmetamethod` - Hook metamethod
- `getnamecallmethod` - Get namecall method name
- `isreadonly` - Check if table is readonly
- `setrawmetatable` - Set raw metatable
- `setreadonly` - Set table readonly state

### 10. **Miscellaneous Functions**

- `identifyexecutor` / `getexecutorname` - Get executor name and version
- `lz4compress` - Compress data with LZ4
- `lz4decompress` - Decompress LZ4 data
- `messagebox` - Show message box
- `queue_on_teleport` / `queueonteleport` - Queue script on teleport
- `request` / `http.request` - Make HTTP request
- `setclipboard` / `toclipboard` - Set system clipboard
- `setfpscap` - Set FPS cap

### 11. **Script Functions**

- `getgc` - Get garbage collector objects
- `getgenv` - Get global environment
- `getloadedmodules` - Get loaded ModuleScripts
- `getrenv` - Get Roblox environment
- `getrunningscripts` - Get running scripts
- `getscriptbytecode` / `dumpstring` - Get script bytecode
- `getscripthash` - Get script hash
- `getscripts` - Get all scripts
- `getsenv` - Get script environment
- `getthreadidentity` / `getidentity` - Get thread identity level
- `setthreadidentity` / `setidentity` - Set thread identity level

### 12. **Drawing Functions**

- `Drawing` - Drawing library
- `Drawing.new` - Create new drawing object
- `Drawing.Fonts` - Font enumeration
- `isrenderobj` - Check if render object
- `getrenderproperty` - Get drawing property
- `setrenderproperty` - Set drawing property
- `cleardrawcache` - Clear drawing cache

### 13. **WebSocket Functions**

- `WebSocket` - WebSocket library
- `WebSocket.connect` - Connect to WebSocket server

## 📈 Output Format

The script provides clear visual feedback:

- ✅ **Pass** - Function exists and works correctly
- ⛔ **Fail** - Function doesn't exist or failed the test
- ⏺️ **No test** - Function exists but no test implemented
- ⚠️ **Missing aliases** - Alternative function names not found

## 🎯 Usage

1. Copy the script content from `UNC.lua` or copy this `loadstring(game:HttpGet("https://raw.githubusercontent.com/Bomzz1302/Unc-Environment-Roblox-Script/refs/heads/main/UNC.lua"))()`
2. Execute it in your Roblox executor
3. Wait for all tests to complete
4. Review the summary report

## 📊 Summary Report

After all tests complete, you'll see:

```
UNC Summary
✅ Tested with a XX% success rate (X out of X)
⛔ X tests failed
⚠️ X globals are missing aliases
```

## 🔍 Example Output

```
UNC Environment Check
✅ - Pass, ⛔ - Fail, ⏺️ - No test, ⚠️ - Missing aliases

✅ cache.invalidate
✅ cache.iscached
✅ cache.replace
✅ cloneref
✅ compareinstances
✅ checkcaller
✅ clonefunction
⏺️ getcallingscript
✅ getscriptclosure
⚠️ getscriptfunction
...

UNC Summary
✅ Tested with a 95% success rate (76 out of 80)
⛔ 4 tests failed
⚠️ 12 globals are missing aliases
```

## 🛠️ Technical Details

### Test Methodology

Each test:

1. Checks if the function exists in the global environment
2. Executes a specific test case using `pcall`
3. Validates the result against expected behavior
4. Checks for common aliases
5. Reports results asynchronously

### Safe Testing

- All tests run in separate coroutines using `task.spawn`
- Each test is wrapped in `pcall` to prevent crashes
- Tests create temporary files in `.tests` folder (auto-cleaned)
- No permanent changes to the game environment

### Compatibility

This script is designed to work with:

- ✅ All major Roblox executors
- ✅ Both 32-bit and 64-bit executors
- ✅ All Roblox client versions
- ✅ All executor API levels

## ⚠️ Notes

1. **Filesystem Tests**: Creates a `.tests` folder for temporary files
2. **Network Tests**: Requires internet connection for `request` test
3. **Drawing Tests**: Creates temporary drawing objects (auto-cleaned)
4. **Thread Identity**: May temporarily change thread identity level
5. **Performance**: Some tests (like `setfpscap`) may take a few seconds

## 🔒 Safety

This script is **completely safe** to run:

- ✅ No malicious code
- ✅ No data collection
- ✅ No permanent modifications
- ✅ No game bans (testing only)
- ✅ Open source and transparent

## 📝 License

This script is provided as-is for testing executor compatibility. Feel free to modify and distribute.

## 🤝 Contributing

If you find any issues or want to add more tests, feel free to:

1. Report bugs
2. Suggest new tests
3. Submit improvements
4. Share compatibility results

## 📞 Support

For issues or questions:

- Check if your executor is up to date
- Verify you're testing in a Roblox game (not Studio)
- Ensure you have proper permissions
- Review the test output for specific errors

---

**Made for the Roblox scripting community** 🎮

_Last Updated: November 2025_
