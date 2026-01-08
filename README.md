# Saksham's Custom WordPress Plugin

A custom WordPress plugin that demonstrates advanced WordPress development concepts including custom admin settings, URL rewriting, and dynamic content display.

## Features

- **Custom Admin Interface**: Complete settings page with various field types (text, password, number, textarea, select, multiselect, radio, checkboxes, and image upload)
- **Custom URL Rewrites**: Creates custom routes at `/custom-plugin/` with pagination support
- **Dynamic Content Display**: Shows mock vehicle data with detail pages accessible via VIN
- **Pagination System**: Implements WordPress-style pagination for data listings
- **Settings Framework**: Comprehensive admin settings with multiple sections and field types
- **Internationalization Ready**: Built with i18n support for translations

## Installation

1. Upload the entire `wordpress-custom-plugin` folder to your `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. After activation, visit the new 'Custom Plugin' menu in your admin panel
4. Go to Settings → Permalinks and click 'Save Changes' to enable URL rewrites

## Usage

### Admin Panel
- Navigate to the 'Custom Plugin' menu in your WordPress admin
- Access the 'Settings' page to configure various options
- Use the 'Secondary Page' for additional plugin information

### Frontend Routes
- **Main Page**: Visit `yoursite.com/custom-plugin/` to see the vehicle listings
- **Paginated Pages**: Navigate through pages at `yoursite.com/custom-plugin/page/2/`, etc.
- **Detail Pages**: View individual vehicles at `yoursite.com/custom-plugin/[VIN-number]/`

## Technical Architecture

### Core Components
- **Main Plugin File**: `wordpress-custom-plugin.php` - Entry point with activation/deactivation hooks
- **Core Class**: `class-wordpress-custom-plugin.php` - Orchestrates the plugin
- **Loader**: `class-wordpress-custom-plugin-loader.php` - Manages WordPress hooks
- **Admin Component**: `class-wordpress-custom-plugin-admin.php` - Admin interface and settings
- **Public Component**: `class-wordpress-custom-plugin-public.php` - Frontend functionality
- **Internationalization**: `class-wordpress-custom-plugin-i18n.php` - Translation support

### Key Functions
- URL rewriting using `add_rewrite_rule`
- Custom query variable registration
- Template redirection using `template_include` filter
- Settings API integration with multiple field types
- Dynamic pagination system

## Development Notes

This plugin was built using the WordPress Plugin Boilerplate as a foundation and extends it with custom functionality for demonstrating advanced WordPress concepts. The plugin includes mock vehicle data for demonstration purposes.

## Contributing

Feel free to fork this repository and submit pull requests for improvements. All contributions are welcome!

## License

This plugin is licensed under the GPL v2 or later license.