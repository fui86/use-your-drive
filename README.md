# Use Your Drive - Plugin Analysis

## Overview

This is a **WordPress plugin** for integrating **Google Drive** with WordPress websites. The plugin allows users to display, play, and manage Google Drive files directly from their WordPress site.

## Repository Structure

This repository contains a **partial export** of the plugin, specifically the frontend assets and media player skins.

```
use-your-drive/
├── css/                          # Main stylesheet assets
│   ├── admin-bar.css             # Admin bar styles
│   ├── admin.min.css             # Admin panel styles (minified)
│   ├── main.min.css              # Main plugin styles (minified)
│   ├── modal.min.css             # Modal/popup styles
│   ├── tinymce.min-rtl.css       # TinyMCE editor RTL styles
│   ├── fonts/                    # Web fonts (Inter Variable)
│   ├── icons/                    # File type icons (128px)
│   └── images/                   # UI images and logos
│
└── skins/                        # Media player skins
    ├── Default_Skin/             # Default media player (MediaElement.js)
    │   ├── Player.php            # Player class definition
    │   ├── Template.php          # HTML template for player
    │   ├── js/Player.js          # JavaScript player logic
    │   ├── css/style.css         # Player styling
    │   └── assets/               # Placeholder images
    │
    ├── Legacy_jPlayer/           # Legacy player (jPlayer library)
    │   ├── Player.php            # Player class definition
    │   ├── Template.php          # HTML template
    │   ├── js/                   # jPlayer library files
    │   └── css/                  # Player styling
    │
    └── Basic_Playlist_2020/      # Alternative modern player
        ├── Template.php          # HTML template
        ├── js/                   # MediaElement.js based
        └── css/                  # Player styling
```

## Technical Details

### Namespace
The plugin uses the PHP namespace: `TheLion\UseyourDrive\MediaPlayers`

### Key Classes

1. **Default_Skin** - Extends `MediaplayerSkin`
   - Uses MediaElement.js library
   - Supports video ads (VAST/VMAP)
   - Localized strings for 40+ languages

2. **Legacy_jPlayer** - Extends `MediaplayerSkin`
   - Uses jQuery jPlayer library
   - Supports audio/video playlists
   - Compatible with older browsers

### Features (based on code analysis)

- **Audio/Video Playback**: Full-featured media players
- **Playlist Support**: Create playlists from Google Drive folders
- **Thumbnails**: Display file thumbnails
- **RTL Support**: Right-to-left language support
- **Responsive Design**: Mobile-friendly layouts
- **Ads Integration**: Support for video ads
- **File Type Icons**: Custom icons for various file types
- **Download Support**: ZIP download of playlists

### Shortcode Options (from Template.php)

| Option | Description |
|--------|-------------|
| `mode` | audio or video |
| `playlistthumbnails` | Show/hide thumbnails |
| `show_filedate` | Show file dates |
| `playlist_search` | Enable search in playlist |
| `maxwidth` | Maximum width |
| `media_ratio` | Aspect ratio (e.g., 16:9) |
| `maxheight` | Maximum height for playlist |
| `showplaylist` | Show playlist panel |
| `showplaylistonstart` | Open playlist on load |
| `playlistinline` | Inline playlist layout |
| `playlistautoplay` | Auto-advance to next track |
| `playlistloop` | Loop playlist |
| `mediabuttons` | Control buttons to display |
| `autoplay` | Auto-play first item |
| `ads` | Enable advertisements |
| `ads_skipable` | Allow skipping ads |

## Dependencies

### JavaScript Libraries
- jQuery
- MediaElement.js
- jPlayer
- jQuery UI Slider

### WordPress Dependencies
- WordPress core
- wp-mediaelement (optional)
- WPCloudPlugins.Polyfill
- WPCloudPlugins.Libraries

## Note

This repository contains only a **subset** of the full Use Your Drive plugin. The complete plugin includes:

| Component | Description |
|-----------|-------------|
| Main plugin PHP files | Core plugin functionality |
| Admin interface | Configuration and settings |
| Google Drive API | Cloud storage integration |
| Shortcode builder | Visual shortcode generator |
| User management | Permission and access control |
| Caching system | Performance optimization |

## Full Plugin

The complete Use Your Drive plugin is available at:
https://codecanyon.net/item/use-your-drive-google-drive-plugin-for-wordpress/6219776

## License

This plugin is a commercial WordPress plugin by WPCloudPlugins.
