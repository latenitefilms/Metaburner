# Lua Scripting

An incredible powerful feature of Metaburner is the ability to code your own Lua scripts.

Simply use the **Lua** Content Source, then use the **Custom Field** to type your code.

Anything you write to the `result` global variable will be displayed in Metaburner.

For example, to display the current date and time you could do:

```lua
result = os.date("%Y-%m-%d %H:%M", os.time())
```

You can also do maths:

![](/static/lua-scripting.png)

Metaburner isn't sandboxed, so you can also read files from your system:

```lua
local function readFile(path)
    local file = io.open(path, "r") -- Open the file for reading
    if not file then
        return nil, "File not found or cannot be opened"
    end

    local content = file:read("*a") -- Read the entire contents of the file
    file:close() -- Close the file
    return content
end

local path = "/Users/chrishocking/Desktop/Test.txt"
local content, err = readFile(path)

if content then
    result = content
else
    result ="Error reading file: " .. err
end
```

Each instance of Metaburner has it's own `uniqueIdentifier`. You can find this by using this Lua code:

```lua
result = uniqueIdentifier
```

You can also see the Unique Identifier in the **Controls** section in the Inspector.

You can use this `uniqueIdentifier` to access the FCPXML and Processed Data.

You have access to the full FCPXML via the `fcpxmlData_uniqueIdentifier` global variable, which is stored as a `string`.

For example:

```lua
result= _G["fcpxmlData_" ..uniqueIdentifier]
```

You have access to Metaburner's processed data via the `processedData_uniqueIdentifier` global variable, which is stored as a `table`.

For example:

```lua
result= _G["processedData_" ..uniqueIdentifier]
```

You can manipulate this data any way you want.

The Lua environment is shared between all instances of the Metaburner plugin, so you can even pass information between different Metaburner Titles!

You can learn more about Lua Scripting on the [CommandPost website](https://commandpost.io/developer/lua-overview/).

[ChatGPT](https://chat.openai.com) is also great at generating Lua scripts.