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
<script src="https://cdn.jsdelivr.net/gh/wladislaw353/Concent-GA-Bundle@1.1/consent-bundle.min.js"></script>
```

2. Initialize with ALL required parameters:
```html
<script>
ConsentModeBundle.init({
    gaId: 'G-YOUR-GA-ID',
    primaryColor: '#28a745',
    primaryHover: '#218838',
    text: {
        title: 'We use cookies',
        description: 'This website uses cookies to analyze traffic and improve your experience. You can choose which cookies you want to allow.',
        acceptAll: 'Accept All',
        rejectAll: 'Reject All',
        settings: 'Settings',
        settingsTitle: 'Cookie Settings',
        settingsDescription: 'Here you can manage your cookie preferences. You can enable or disable different types of cookies below.',
        save: 'Save Settings',
        cancel: 'Cancel',
        necessary: {
            title: 'Necessary Cookies',
            description: 'These cookies are essential for the website to function properly and cannot be disabled. They are usually only set in response to actions made by you which amount to a request for services.'
        },
        analytics: {
            title: 'Analytics Cookies',
            description: 'These cookies help us understand how visitors interact with our website by collecting and reporting information. All information these cookies collect is aggregated and therefore anonymous.'
        },
        advertising: {
            title: 'Advertising Cookies',
            description: 'These cookies are used to make advertising messages more relevant to you and your interests. They may be used to prevent the same ad from being shown to you too many times and to measure the effectiveness of advertising campaigns.'
        }
    }
});
</script>
```
**Note:** No need to include Google Analytics separately - the script automatically loads and configures GA with your provided ID.

**That's it!** The consent banner will appear on first visit and handle all cookie consent automatically.

## How It Works

1. **Auto-loads Google Analytics**: No need to include GA scripts manually
2. **Default State**: All consent parameters set to "denied" for GDPR compliance
3. **First Visit**: Banner appears asking for cookie consent
4. **User Choice**: Selections are saved in localStorage
5. **Subsequent Visits**: Previous choices are automatically applied
6. **Google Analytics**: Respects consent mode settings automatically

## Testing

To test the consent banner:

1. Clear localStorage: `localStorage.removeItem('cookie_consent_status')`
2. Refresh the page
3. The banner should appear asking for consent

## License

MIT License - Free to use in any project.