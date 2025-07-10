# Extra Icon Features Recipe

## Overview

The Extra Icon Features recipe provides a customizable block type that allows you to create icon-based feature sections for your Drupal website. This recipe creates both a block content type and a paragraph type, making it flexible for various layout scenarios.

## Features

- **Icon Features Block Type**: Custom block content type for creating feature sections
- **Icon Features Paragraph Type**: Paragraph type for use within other content types
- **FontAwesome Integration**: Uses the FontAwesome module for professional icons
- **Responsive Design**: Configurable column layouts (4-column, 3-column, etc.)
- **Multiple Display Modes**: Several view modes for different layouts
- **Sample Content**: Includes pre-configured sample content block

## Requirements

- Drupal 10.4+ or Drupal 11+
- Composer package manager
- Paragraphs module (^1.19)
- FontAwesome module (^3.0)

## Installation

To install via Composer, run:

```sh
composer require morethanthemes/extra_block
````

This recipe can be applied using Drupal's recipe system:

```bash
# From your Drupal root directory
drush recipe recipes/extra_icon_features
```

## What's Included

### Content Types

- **Icon Features Block**: Custom block content type with configurable columns and icon feature items
- **Icon Features Paragraph**: Paragraph type for individual icon feature items

### Fields

- **Title** (`field_mt_if_title`): Text field for the feature title
- **Body** (`field_mt_if_body`): Formatted text field for the feature description
- **FontAwesome Icon** (`field_mt_if_fa_icon`): FontAwesome icon selection field
- **Image** (`field_mt_if_image`): Optional image field as alternative to icon
- **Link** (`field_mt_if_link`): Optional link field for feature items
- **Columns** (`field_mt_if_columns`): CSS classes for column layout configuration
- **Items** (`field_mt_if_item`): Entity reference field to icon feature paragraphs

### Display Modes

- **Default**: Standard display mode
- **MT Media After**: Display mode with media positioned after content
- **MT Tile**: Tile-style display mode
- **MT Tile Large**: Large tile display mode

### Sample Content

The recipe includes a sample "Great features at a glance" block with 8 pre-configured icon features:

- Great battery life (battery-full icon)
- Great architecture (network-wired icon)
- Great codebase (code icon)
- Great interactivity (comments icon)
- Notifications (bell icon)
- Lightning speed (lightbulb icon)
- The power of numbers (calculator icon)
- Children-friendly (child icon)

## Usage

### Creating Icon Feature Blocks

1. Navigate to **Structure > Block layout > Custom block library**
2. Click "Add custom block" and select "Icon Features"
3. Configure the column layout using CSS classes (e.g., "col-lg-3 col-md-6 four-columns")
4. Add icon feature items by clicking "Add Icon Features"
5. For each item, configure:
   - Title text
   - Description text
   - FontAwesome icon selection
   - Optional image upload
   - Optional link URL

### Using Icon Features in Layout Builder

The Icon Features block can be placed in any Layout Builder-enabled content using the block placement interface.

### Customizing Column Layouts

The `field_mt_if_columns` field accepts CSS classes for responsive column layouts:

- `col-lg-3 col-md-6 four-columns`: 4 columns on large screens, 2 on medium
- `col-lg-4 col-md-6 three-columns`: 3 columns on large screens, 2 on medium
- `col-lg-6 col-md-12 two-columns`: 2 columns on large screens, 1 on medium

## Customization

### Styling

The recipe provides basic structure but relies on your theme for styling. Common CSS classes to target:

- `.block-mt-icon-features`: Main block wrapper
- `.paragraph--type--mt-icon-features`: Individual feature items
- `.field--name-field-mt-if-fa-icon`: FontAwesome icon wrapper
- `.field--name-field-mt-if-title`: Feature title
- `.field--name-field-mt-if-body`: Feature description

### Additional Fields

You can extend the Icon Features paragraph type with additional fields through the Drupal admin interface:

1. Go to **Structure > Paragraphs types > Icon Features > Manage fields**
2. Add new fields as needed
3. Configure display settings in **Manage display**

### View Modes

Customize the display by creating or modifying view modes:

1. Go to **Structure > Display modes > View modes**
2. Edit existing view modes or create new ones
3. Configure field display settings for each view mode

## Troubleshooting

### FontAwesome Icons Not Displaying

- Ensure the FontAwesome module is properly installed and configured
- Check that your theme includes FontAwesome CSS or the module is configured to include it
- Verify icon names are valid FontAwesome icon identifiers

### Layout Issues

- Review CSS classes in the columns field
- Ensure your theme includes Bootstrap or compatible grid system
- Check view mode configurations for proper field display

## License

Licensed under **GPL-2.0-or-later**.

## Organization

Developed by **[More than Themes](https://morethanthemes.com)** for [Webmaker+](https://webmaker.morethanthemes.com)

## Contributing

Contributions are welcome! Feel free to submit issues or feature requests.

