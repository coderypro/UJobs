# UJobs Changelog

## Version 1.1.0 (February 23, 2026)

### 🎨 New Features
- **Custom Model Data Support** - Add custom_model_data to all GUI items for resource pack integration
- **Hex Color Support** - Full support for hex colors in both formats: `&#RRGGBB` and `&x&R&R&G&G&B&B`
- **Standard Minecraft Color Codes** - Support for `&a`, `&c`, `&e`, etc. color codes
- **GUI Configuration System** - New `gui.yml` file for complete GUI customization
- **Size & Slot Customization** - Configure GUI size and specific slot positions for all items
- **Background Slot Control** - Choose which slots to fill with background items (border-only, checkered, etc.)
- **Navigation Slot Control** - Place navigation buttons in custom positions

### 🛠️ Utilities Added
- **ColorUtil.java** - Utility class for handling hex colors and Minecraft color codes
  - `colorize()` - Convert color codes to colored text
  - `legacyToMiniMessage()` - Convert legacy colors to MiniMessage format
  - `toComponent()` - Create colored components
  - `stripColors()` - Remove all color codes
  
- **GUIItemBuilder.java** - Builder pattern for creating GUI items
  - Support for custom model data
  - Hex color support in names and lore
  - Player head support
  - Item flags and attributes
  - Enchantment glint

### 🔒 GUI Protection Enhanced
- Configurable GUI protection system in config.yml:
  - `gui_protection.enabled` - Master switch
  - `gui_protection.cancel_clicks` - Prevent item taking
  - `gui_protection.cancel_shift_clicks` - Block shift-clicking
  - `gui_protection.cancel_drag` - Prevent dragging items

### 📝 Configuration Updates
- **config.yml** enhancements:
  - Custom model data support for blank items, job items, and navigation buttons
  - Hex color documentation and examples
  - GUI protection settings
  
- **gui.yml** (NEW):
  - Complete GUI configuration for all menus
  - Size and slot customization
  - Background item control
  - Navigation button positioning
  - Detailed examples and documentation
  - Slot numbering reference guide

### 📚 Documentation
- **GUI_CONFIGURATION_GUIDE.md** - Comprehensive guide with examples
- Detailed comments in gui.yml showing all customization options
- Slot numbering visual reference
- Custom GUI templates and examples

### 🐛 Bug Fixes
- Fixed compilation issues with optional UltimateTimber dependency
- Improved GUI event handling and protection

### 🔄 Changes
- Updated all existing GUIs to support new features
- Enhanced InventoryListener with configurable protection
- Maven build configuration improvements
- Commented out UltimateTimber dependency (optional)

### 📦 Build Info
- Java Version: 21
- Paper API: 1.21.10-R0.1-SNAPSHOT
- Built with: Maven Daemon (mvnd) 1.0.3

### 📖 Upgrade Notes
- Fully backward compatible with version 1.0.5
- New gui.yml file will be created on first run
- Existing config.yml will work without changes
- Optional: Configure new features in gui.yml and config.yml

### 🎯 For Server Owners
All new features are optional and backward compatible. Your existing configuration will continue to work. To use new features:

1. Add custom_model_data values in config.yml (if using resource packs)
2. Use gui.yml for advanced GUI customization
3. Configure GUI protection in config.yml if needed
4. Experiment with hex colors in any color field

### 🎨 For Resource Pack Creators
You can now add custom models to:
- Background/blank items
- Job items
- Navigation buttons
- Any GUI item

Use the `custom_model_data` field in config.yml or gui.yml.

---

## Version 1.0.5
- Previous stable release

