## INSTALLATION
```lua
use({"loctvl842/winbar", requires = {"loctvl842/dev-icons})
```

## CONFIGURATION
```lua
local status_ok, winbar = pcall(require, "winbar")
if not status_ok then
	return
end

winbar.setup({
	disable_icons = false,
	disabled_filetype = {},
	separator = ">",
	-- limit for amount of context shown
	-- 0 means no limit
	-- Note: to make use of depth feature properly, make sure your separator isn't something that can appear
	-- in context names (eg: function names, class names, etc)
	depth = 0,
	-- indicator used when context hits depth limit
	depth_limit_indicator = "..",
	highlight = {
		component = "LineNr",
		separator = "LineNr",
	},
})
```
