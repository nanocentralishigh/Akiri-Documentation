# Akiri-Documentation
getthreadidentity() - Prints the thread identity.
setthreadidentity(NUM) - Sets the thread identity.
gethui() - Can be used to retreive a GUI from CoreGUI.
getrawmetatable(obj) - Returns the metatable of the given object without triggering any protections or __metatable fields.
setrawmetatable(obj, mt) - Replaces the metatable of an object without restrictions, even if it was protected with a __metatable lock.
isreadonly(obj) - Returns true if the object is protected (read-only). Used to check if an object's metatable is locked.
setreadonly(obj, bool) - Enables or disables read-only protection for an object.
make_writeable(obj)	- 	Same as setreadonly(obj, bool), used to unlock tables/metatables
getnamecallmethod()	- Retrieves the method name used in a __namecall metamethod.
setnamecallmethod(method)	- 	Manually sets the namecall method.
identifyexecutor() - 	Returns a string identifying the current exploit.
getexecutorname()	- 	Same as above, returns name of the executor.
loadstring(code)	- 	Converts a string into Lua code and executes it.
getgenv()	- 	Returns the global environment.
gettenv(fn)	- Gets the environment of a specific function.
getrenv()	- 	Gets the Roblox environment.
getgc([true/false])	- 	Returns all objects tracked by the garbage collector, including functions, tables, and userdata.
getreg() - Returns the internal Lua registry, holds all references like globals, upvalues, etc.
getsenv(script)	- Gets the environment of a LocalScript.
getcustomasset(path) - Converts a local asset (e.g., image, sound) to a Roblox-compatible asset ID that can be used in-game. Example use: ImageLabel.Image = getcustomasset("image.png")
cloneref(instance)	- 	Creates a reference to a Roblox Instance that is safe from garbage collection or cross-context issues.
compareinstances(a, b)	- Returns true if the two instances are the same object, even if one is a cloned reference.
lz4compress(data)	- Compresses data using the LZ4 algorithm.
lz4decompress(data)	- Decompresses LZ4-compressed data.
messagebox(text, title, type)	- Creates a native Windows-style message box with text, title, and optional type (e.g. OK/Cancel).
# Debug Library
debug.getproto(fn, index) - Gets a specific function prototype from a Lua function.
debug.getprotos(fn) - Gets all protos inside a function.
debug.getstack()	- 	Gets the current function call stack.
debug.getinfo(fn)	- Gets metadata about a function (name, source, line, etc).
debug.getupvalue(fn, i)	- Gets the i-th upvalue of a function.
debug.getupvalues(fn)	- Gets all upvalues of a function.
debug.getconstant(fn, i) - Gets the i-th constant of a function.
debug.getconstants(fn) - Gets all constants of a function.
debug.setconstant(fn, i, val)	- Sets a constant in a function to something else.
debug.setstack() - Allows modifying the stack trace.
debug.setupvalue(fn, i, val) - Sets the i-th upvalue of a function. Allows spoofing locals.
# File System
writefile(path, content) - writefile(path, content)
readfile(path)	- Reads and returns the contents of the file at path.
appendfile(path, content)	- Appends content to the file at path. Creates it if it doesn't exist.
delfile(path)	- Deletes the file at path.
makefolder(path)	- Creates a folder at the given path.
delfolder(path)	- Deletes a folder at the given path and all its contents.
isfolder(path)	- Returns true if the folder exists.
isfile(path)	- Returns true if the file exists.
listfiles(path)	- Returns a list of file/folder names inside the folder at path.
loadfile(path) - Loads and returns a Lua function from the file at path. Like loadstring(readfile(path)).
delfile(path)	
# Fun tingz
saveinstance() - Saves a copy of the game.(MAP ONLY, NO SCRIPTS)
