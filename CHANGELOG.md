# Changelog

All notable changes to LCP Optimizer Universal PRO will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [2.3.4] - 2024-11-04

### Fixed
- Removed hardcoded default fonts from Target Font Families field
  

## [2.3.3] - 2024-11-04

### 🔍 Improved
- **Cache plugin detection messaging:** Now transparent about detection limitations. Shows "may be inactive" to prevent user confusion when installed-but-inactive plugins are detected.
- **Compatibility mode:** Remains active for safety regardless of plugin active status.

### 📚 Enhanced
- **Google Fonts documentation:** Added Tip 2 clarifying that manual URL always takes priority over auto-detection.
- **JavaScript preload warnings:** Added explicit examples of scripts that should NOT be preloaded:
  - ❌ Analytics (Google Analytics, GTM)
  - ❌ SEO plugins (Yoast, All-in-One SEO)
  - ❌ Chat widgets
  - ❌ Social sharing buttons
  - ❌ Non-critical third-party scripts

### 🔧 Fixed
- Added `require_once` for `is_plugin_active()` function to ensure availability
- Improved error handling in cache plugin detection routine
- Better admin notice styling for detected plugins

### 💡 User Experience
- Clearer messaging throughout admin interface
- Better guidance on when to use advanced features
- Prevents common misconfigurations that can harm performance
- More honest about plugin capabilities and limitations

### 🎯 Why This Update
Due to WordPress plugin loading timing, cache plugin detection may include installed-but-inactive plugins. Rather than hide this technical limitation, we're transparent about it while keeping compatibility mode active for maximum safety.


## [2.3.2] - 2024-10-27

### 🔗 Added
- Re-added "Google Fonts CSS URL" input field in Font Optimization tab
- Manual control over Google Fonts URL for better optimization
- Performance tip to load only required font weights
- Optional field with auto-detection fallback

### 🐛 Fixed
- Resolved issue where Google Fonts CSS URL field was missing
- Improved font optimization workflow

---

## [2.3.1] - 2024-10-26

### 🛠️ Added
- Quick-access buttons to performance testing tools in Performance tab:
  - PageSpeed Insights (with pre-filled site URL)
  - GTmetrix (with pre-filled site URL)
  - Pingdom Tools
  - WebPageTest (with pre-filled site URL)
- One-click access to industry-standard testing platforms
- Automatic URL pre-filling for faster testing

### ✨ Improved
- Enhanced user experience with direct testing tool integration
- Streamlined performance testing workflow

---

## [2.3.0] - 2024-10-25

### 🌍 Added
- Complete English translation of admin panel
- Enhanced help texts and tooltips throughout interface
- Professional documentation in all sections

### 📚 Improved
- Comprehensive WP Rocket configuration guide
- Detailed optimization delay explanation
- Performance impact notes for fonts
- DNS prefetch auto-inclusion transparency

### 🔒 Security
- Debug panel now visible only to administrators
- Enhanced admin-only features for better security

---

## [2.2.0] - 2024-10-20

### ⚡ Added
- Early Hints support (HTTP/2+) for faster resource loading
- Intelligent INP optimization via debouncing
- Automatic DNS prefetch for common CDNs

### 🖼️ Improved
- Enhanced image lazy loading with above-the-fold detection
- Better aspect-ratio preservation
- Optimized fetchpriority="high" attribution

### 🐛 Fixed
- Menu flashing issue with certain themes
- CLS calculation improvements
- Better Elementor editor compatibility

---

## [2.1.0] - 2024-10-15

### 🔤 Added
- Font preload functionality for WOFF2/WOFF/TTF files
- Global font-display: swap support
- Google Fonts async loading

### 📥 Improved
- Auto-detection of critical CSS files
- Enhanced LCP image preloading (up to 3 images)
- Better cache plugin compatibility

### 🛠️ Changed
- Reduced inline CSS footprint to <2KB
- Optimized DOM manipulation timing

---

## [2.0.0] - 2024-10-10

### 🚀 Major Release
- Complete rewrite for Core Web Vitals 2024 standards
- New admin interface with tabbed navigation
- Real-time optimization status indicators

### ✨ Added
- LCP optimization engine
- INP optimization engine
- CLS prevention system
- Elementor full compatibility
- WP Rocket integration guide

### 🔧 Technical
- PHP 7.4+ requirement
- WordPress 6.0+ requirement
- Removed jQuery dependency
- Modern JavaScript ES6+ implementation

---

## [1.5.0] - 2024-09-01

### Added
- Basic LCP preload functionality
- Image lazy loading
- Font optimization basics

### Fixed
- Various minor bugs
- Performance improvements

---

## [1.0.0] - 2024-08-01

### 🎉 Initial Release
- Basic Core Web Vitals optimization
- LCP image preloading
- Simple admin interface
- GPL-2.0 license

---

## Upgrade Notes

### From 2.3.1 to 2.3.2
- No breaking changes
- Settings are preserved
- Clear cache after upgrade recommended

### From 2.2.x to 2.3.x
- New English interface (Italian version removed)
- Review WP Rocket settings with new guide
- Test performance after upgrade

### From 2.1.x to 2.2.x
- Early Hints requires HTTP/2+ server support
- Check DNS prefetch settings
- Clear all caches after upgrade

### From 2.0.x to 2.1.x
- Font optimization settings added
- Review font preload configuration
- Test with WP Rocket if using CSS minification

### From 1.x to 2.0
- **Breaking changes:** Complete rewrite
- Backup your site before upgrading
- Re-configure plugin settings
- Test thoroughly on staging first

---

## Deprecation Warnings

### Version 3.0 (Planned Q2 2025)
- PHP 7.4 support will be deprecated (minimum PHP 8.0)
- WordPress 6.0-6.1 support will be deprecated (minimum WP 6.2)

---

## Links

- [GitHub Repository](https://github.com/emanuelcelano/lcp-optimizer-universal-pro)
- [Download Latest Release](https://github.com/emanuelcelano/lcp-optimizer-universal-pro/releases/latest)
- [Report Issues](https://github.com/emanuelcelano/lcp-optimizer-universal-pro/issues)
- [Documentation](https://github.com/emanuelcelano/lcp-optimizer-universal-pro/wiki)
