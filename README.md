# Google Consent Mode v2 Bundle

Complete Google Consent Mode v2 implementation with integrated Google Analytics in a single minified file.

## Features

- ✅ **Google Consent Mode v2** - Full compliance with all 4 parameters
- ✅ **Auto Google Analytics** - Automatically loads and configures GA
- ✅ **GDPR Compliant** - All cookies denied by default
- ✅ **Responsive Design** - Works on all devices
- ✅ **Customizable** - Colors and text fully configurable
- ✅ **Lightweight** - Only ~6KB minified
- ✅ **Zero Dependencies** - No external libraries required

## Quick Start

1. Include the script in your `<head>`:
```html
<script src="https://cdn.jsdelivr.net/gh/wladislaw353/Concent-GA-Bundle@1.0/consent-bundle.min.js"></script>
```

2. Initialize with your Google Analytics ID:
```html
<script>
ConsentModeBundle.init({
    gaId: 'G-YOUR-GA-ID'
});
</script>
```
**Note:** No need to include Google Analytics separately - the script automatically loads and configures GA with your provided ID.

**That's it!** The consent banner will appear on first visit and handle all cookie consent automatically.

## Configuration

```javascript
ConsentModeBundle.init({
    gaId: 'G-YOUR-GA-ID',
    primaryColor: '#007bff',
    primaryHover: '#0056b3',
    text: {
        title: 'We use cookies',
        description: 'This website uses cookies to improve your experience.',
        acceptAll: 'Accept All',
        rejectAll: 'Reject All',
        settings: 'Settings',
        settingsTitle: 'Cookie Settings',
        settingsDescription: 'Manage your cookie preferences below.',
        save: 'Save Settings',
        cancel: 'Cancel',
        necessary: {
            title: 'Necessary Cookies',
            description: 'Essential cookies required for website functionality.'
        },
        analytics: {
            title: 'Analytics Cookies',
            description: 'Help us understand how visitors use our website.'
        },
        advertising: {
            title: 'Advertising Cookies',
            description: 'Used for relevant advertising and campaign measurement.'
        }
    }
});
```

## How It Works

1. **Auto-loads Google Analytics**: No need to include GA scripts manually
2. **Default State**: All consent parameters set to "denied" for GDPR compliance
3. **First Visit**: Banner appears asking for cookie consent
4. **User Choice**: Selections are saved in localStorage
5. **Subsequent Visits**: Previous choices are automatically applied
6. **Google Analytics**: Respects consent mode settings automatically

## API Methods

After initialization, these methods are available:

```javascript
ConsentModeBundle.acceptAll()     // Accept all cookies
ConsentModeBundle.rejectAll()     // Reject all cookies
ConsentModeBundle.showSettings()  // Show settings modal
ConsentModeBundle.hideSettings()  // Hide settings modal
ConsentModeBundle.showBanner()    // Show consent banner
ConsentModeBundle.hideBanner()    // Hide consent banner
```

## Testing

To test the consent banner:

1. Clear localStorage: `localStorage.removeItem('cookie_consent_status')`
2. Refresh the page
3. The banner should appear asking for consent

## License

MIT License - Free to use in any project.