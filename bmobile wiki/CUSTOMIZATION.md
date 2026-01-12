# ROM Customization Tutorial

This tutorial covers how to customize your BMobile ROM experience, from basic theming to advanced modifications.

## Basic Customization

### System Themes

#### Material You Dynamic Colors
1. **Enable Dynamic Colors**:
   ```
   Settings → Wallpaper & style → Dynamic colors
   Toggle ON
   ```

2. **Wallpaper Integration**:
   - Set wallpaper that matches your style
   - Dynamic colors will adapt automatically
   - Preview changes in real-time

#### Dark Mode Configuration
1. **System-Wide Dark Mode**:
   ```
   Settings → Display → Dark theme
   Choose: System default / Light / Dark
   ```

2. **App-Specific Dark Mode**:
   - Some apps override system setting
   - Check individual app settings

#### Accent Colors
1. **Custom Accent Colors**:
   ```
   Settings → Wallpaper & style → Basic colors
   Select custom color
   ```

2. **Color Palette Options**:
   - Predefined Material colors
   - Custom color picker
   - Wallpaper-based colors

### Display & Interface

#### Font Customization
1. **System Fonts**:
   ```
   Settings → Display → Font size & style
   Choose from available fonts
   ```

2. **Custom Fonts** (Root Required):
   - Install font changer apps
   - Use Magisk modules for system fonts
   - Popular: Google Sans, Samsung Sans

#### Display Size & Density
1. **Font Size**:
   ```
   Settings → Display → Font size & style
   Drag slider for preferred size
   ```

2. **Display Size**:
   ```
   Settings → Display → Display size
   Adjust app and UI scaling
   ```

3. **Screen Density** (Advanced):
   ```
   Settings → System → Developer options → Minimum width
   Lower values = smaller UI elements
   ```

### Navigation & Gestures

#### Navigation Mode
1. **Gesture Navigation** (Recommended):
   ```
   Settings → System → Gestures → System navigation
   Select "Gesture navigation"
   ```

2. **3-Button Navigation**:
   - Traditional back/home/recent buttons
   - Customizable button arrangement

#### Gesture Customization
1. **Back Gesture Sensitivity**:
   ```
   Settings → System → Gestures → System navigation
   Adjust sensitivity slider
   ```

2. **Additional Gestures**:
   - **Quick Switch**: Swipe up from nav bar
   - **Screenshot**: Swipe palm across screen
   - **One-Handed Mode**: Triple tap navigation bar

### Quick Settings Panel

#### QS Tiles Customization
1. **Edit Quick Settings**:
   ```
   Pull down notification shade twice
   Tap pencil icon (edit)
   Drag tiles to rearrange
   ```

2. **Add/Remove Tiles**:
   - Drag tiles between active/inactive
   - Popular tiles: Battery, WiFi, Bluetooth, Location

#### QS Grid Size
1. **Adjust Grid** (Root Required):
   ```
   Use apps like "QuickSwitch" or "Custom Quick Settings"
   Adjust rows and columns
   ```

### Status Bar Customization

#### Status Bar Icons
1. **Icon Management**:
   ```
   Settings → Notifications → Status bar
   Toggle various status icons
   ```

2. **Battery Percentage**:
   ```
   Settings → Battery → Battery percentage
   Show in status bar
   ```

#### Clock Customization
1. **Clock Format**:
   ```
   Settings → System → Date & time
   12/24 hour format
   ```

2. **AM/PM Display**:
   - Automatic based on locale
   - Some ROMs allow custom formatting

## Advanced Customization

### Custom Launchers

#### Installing Custom Launchers
1. **Recommended Launchers**:
   - **Lawnchair**: Pixel-like experience
   - **Nova Launcher**: Highly customizable
   - **Action Launcher**: Unique features

2. **Set as Default**:
   ```
   Home button → Choose default launcher
   Select preferred launcher
   ```

#### Launcher Configuration
1. **Lawnchair Setup**:
   ```
   App drawer → Settings → Home screen
   Configure grid size, icon packs
   ```

2. **Icon Packs**:
   - Download from Play Store/F-Droid
   - Apply in launcher settings

### Icon Packs & Themes

#### Applying Icon Packs
1. **System-Wide Icons** (Limited):
   - Some launchers support system icon theming
   - Use Substratum for advanced theming

2. **Per-App Icons**:
   - Use apps like "Icon Pack Studio"
   - Create custom icon sets

### Custom Sounds & Notifications

#### Custom Ringtones
1. **Set Custom Ringtone**:
   ```
   Settings → Sound & vibration → Phone ringtone
   Select from storage
   ```

2. **Notification Sounds**:
   ```
   Settings → Sound & vibration → Default notification sound
   Choose notification tone
   ```

#### Audio Customization
1. **Equalizer**:
   - Built-in Android equalizer
   - Third-party apps like Wavelet

### Boot Animation

#### Custom Boot Animation (Root Required)
1. **Download Boot Animation**:
   - Find compatible boot animations
   - Ensure correct resolution for your device

2. **Install via Magisk**:
   ```
   Magisk Module: "Boot Animation Changer"
   Install module → Reboot
   ```

### Custom Recovery (TWRP)

#### TWRP Theme Customization
1. **TWRP Settings**:
   ```
   Boot into TWRP → Advanced → Settings
   Customize appearance and behavior
   ```

2. **Custom TWRP Builds**:
   - Some devices have themed TWRP versions
   - Check device-specific forums

## Performance Customization

### Developer Options

#### Enable Developer Options
1. **Access Developer Options**:
   ```
   Settings → About phone → Build number
   Tap 7 times to enable
   ```

#### Performance Tweaks
1. **Animation Scales**:
   ```
   Settings → System → Developer options → Animation scales
   Set to 0.5x for smoother feel
   ```

2. **Background Process Limit**:
   ```
   Developer options → Background process limit
   Increase for better multitasking
   ```

3. **Force GPU Rendering**:
   ```
   Developer options → Force GPU rendering
   Enable for better graphics performance
   ```

### Memory Management

#### RAM Optimization
1. **Disable Unnecessary Apps**:
   ```
   Settings → Apps → See all apps
   Disable bloatware and unused apps
   ```

2. **Background App Refresh**:
   ```
   Settings → Network & internet → Data usage → Data saver
   Enable to limit background data
   ```

### Battery Optimization

#### Battery Settings
1. **Adaptive Battery**:
   ```
   Settings → Battery → Adaptive preferences
   Enable for automatic optimization
   ```

2. **App Battery Usage**:
   ```
   Settings → Battery → Battery usage
   Review and restrict power-hungry apps
   ```

## Privacy & Security Customization

### Permission Management

#### App Permissions
1. **Review Permissions**:
   ```
   Settings → Privacy → Permission manager
   Review all app permissions
   ```

2. **One-Time Permissions**:
   - Grant permissions only when needed
   - Android 11+ feature

#### Location Settings
1. **Location Accuracy**:
   ```
   Settings → Location → Location services
   Enable Google Location Accuracy (optional)
   ```

### Firewall & Network

#### AFWall+ (Root Required)
1. **Install AFWall+**:
   ```
   F-Droid → Search "AFWall+"
   Install and grant root access
   ```

2. **Configure Rules**:
   ```
   AFWall+ → Menu → Rules/Profiles
   Set custom rules per app
   ```

### DNS Customization

#### Private DNS
1. **Enable Private DNS**:
   ```
   Settings → Network & internet → Advanced → Private DNS
   Choose provider or specify custom
   ```

2. **Recommended Providers**:
   - `p2.freedns.controld.com` (Control D)
   - `p0.freedns.controld.com` (no logging)
   - Custom: `8.8.8.8` or `1.1.1.1`

## Backup & Sync

### Google Services (Optional)
**Note**: We recommend avoiding Google services for privacy

1. **Google Account Setup** (if needed):
   ```
   Settings → Accounts → Add account → Google
   Sign in (use separate account for privacy)
   ```

2. **Sync Settings**:
   ```
   Settings → Accounts → Google → Account sync
   Enable only necessary sync options
   ```

### Alternative Sync Solutions
1. **Nextcloud**: Self-hosted cloud sync
2. **Syncthing**: Peer-to-peer file sync
3. **SeedVault**: Local encrypted backup

## Advanced Modifications

### Substratum Themes (Root Required)
1. **Install Substratum**:
   ```
   Play Store → Substratum
   Grant root access
   ```

2. **Apply Themes**:
   ```
   Substratum → Themes
   Select and apply system themes
   ```

### Custom ROM Features

#### BMobile-Specific Customizations
1. **Check BMobile Settings**:
   ```
   Settings → BMobile (if available)
   Customize ROM-specific features
   ```

2. **Theme Manager**:
   - Some custom ROMs include theme engines
   - Apply custom themes and icon packs

### Kernel Customization (Advanced)

#### Kernel Tweaks
1. **Install Kernel Manager**:
   ```
   F-Droid → Kernel Adiutor
   Grant root access
   ```

2. **CPU/GPU Control**:
   ```
   Kernel Adiutor → CPU → Set custom frequencies
   GPU → Adjust GPU settings
   ```

#### I/O Schedulers
1. **Change I/O Scheduler**:
   ```
   Kernel Adiutor → I/O Scheduler
   Try different schedulers for performance
   ```

## Troubleshooting Customizations

### Common Issues

#### Theme Conflicts
- **Reset Themes**: Use theme reset options
- **Clear Cache**: Clear system and app cache
- **Reboot**: Restart device after changes

#### Performance Issues
- **Reset to Defaults**: Return to stock settings
- **Monitor Resources**: Use apps like "CPU-Z"
- **Battery Drain**: Check battery usage stats

#### App Compatibility
- **Update Apps**: Ensure apps are updated
- **Alternative Apps**: Find compatible alternatives
- **Report Issues**: Check XDA or GitHub issues

### Recovery Options
1. **Soft Reset**:
   ```
   Hold power button → Restart
   ```

2. **Cache Wipe**:
   ```
   Boot to recovery → Wipe cache
   ```

3. **Factory Reset** (Last Resort):
   ```
   Settings → System → Reset options → Erase all data
   ```

## Recommended Apps for Customization

### Launchers
- **Lawnchair**: Feature-rich Pixel launcher
- **Nova Launcher**: Highly customizable
- **Action Launcher**: Unique gesture features

### Customization Tools
- **Substratum**: Advanced theming engine
- **Icon Pack Studio**: Create custom icon packs
- **Wallpapers**: Dynamic wallpaper apps

### Performance Tools
- **Kernel Adiutor**: Kernel and performance control
- **AFWall+**: Network firewall
- **3C Toolbox**: System maintenance

### Privacy Tools
- **NetGuard**: No-root firewall
- **TrackerControl**: Tracker and ad blocking
- **Exodus Privacy**: App tracker analysis

## Best Practices

### Gradual Changes
- **Test Changes**: Try one modification at a time
- **Backup Frequently**: Create backups before major changes
- **Document Setup**: Keep notes on your preferred settings

### Performance Balance
- **Battery vs Performance**: Find your sweet spot
- **Storage Management**: Regularly clean cache and junk
- **Update Regularly**: Keep ROM and apps updated

### Privacy First
- **Minimize Permissions**: Grant only necessary permissions
- **Regular Audits**: Review app permissions quarterly
- **Secure Backups**: Encrypt all sensitive backups

### Stability Focus
- **Avoid Experimental**: Stick to stable modifications
- **Test Thoroughly**: Use device for a few days before relying on it
- **Have Recovery Plan**: Always know how to revert changes

Remember: Customization is about making your device work better for you. Start small, backup often, and enjoy your personalized BMobile experience!