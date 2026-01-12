# Troubleshooting Guide

This comprehensive troubleshooting guide helps you resolve common issues with BMobile ROM. Follow the steps in order for best results.

## Boot Issues

### Device Won't Boot After Installation

#### Symptoms
- Stuck on boot animation
- Bootloop (restarts continuously)
- Black screen after logo

#### Solutions

1. **Enter Recovery Mode**:
   ```
   Hold Power + Volume Down for 10-15 seconds
   If that doesn't work, try:
   Power + Volume Up
   or device-specific key combination
   ```

2. **Clear Cache**:
   ```
   TWRP → Wipe → Advanced Wipe
   Select: Dalvik/ART Cache, Cache
   Swipe to wipe
   ```

3. **Wipe Data (Factory Reset)**:
   ```
   TWRP → Wipe → Advanced Wipe
   Select: System, Data
   Swipe to wipe
   ```

4. **Restore from Backup**:
   ```
   TWRP → Restore → Select your backup
   Restore System and Data partitions
   ```

5. **Clean Flash ROM**:
   - Download ROM again (corruption possible)
   - Format Data in TWRP
   - Flash ROM and GApps (if used)

### Stuck at Boot Animation

#### Quick Fixes
1. **Wait Longer**: First boot can take 5-10 minutes
2. **Check Battery**: Ensure 50%+ battery level
3. **Try Safe Mode**:
   ```
   Hold Power button during boot
   Select "Safe Mode" when prompted
   ```

#### Advanced Solutions
1. **Log Collection**:
   ```
   adb logcat > boot_log.txt
   # Analyze for specific errors
   ```

2. **Partition Issues**:
   ```
   TWRP → Advanced → Terminal
   e2fsck /dev/block/by-name/system
   e2fsck /dev/block/by-name/data
   ```

## Performance Issues

### Slow Performance

#### System Optimization
1. **Disable Animations**:
   ```
   Settings → System → Developer options
   Set all animation scales to 0.5x
   ```

2. **Background Apps**:
   ```
   Settings → System → Developer options
   Background process limit → 2 or 3 processes
   ```

3. **Memory Management**:
   ```
   Settings → Apps → See all apps
   Force stop unused apps
   Disable unnecessary apps
   ```

#### Storage Cleanup
1. **Clear Cache**:
   ```
   Settings → Storage → Free up space
   Clear cache for all apps
   ```

2. **Remove Bloatware**:
   ```
   Settings → Apps → See all apps
   Uninstall or disable unused system apps
   ```

### Battery Drain

#### Battery Optimization
1. **Check Battery Usage**:
   ```
   Settings → Battery → Battery usage
   Identify power-hungry apps
   ```

2. **Adaptive Battery**:
   ```
   Settings → Battery → Adaptive preferences
   Enable adaptive battery
   ```

3. **Background Restrictions**:
   ```
   Settings → Apps → See all apps
   Select app → Battery → Background restriction
   ```

#### Advanced Fixes
1. **Disable Location**:
   ```
   Settings → Location → Turn off when not needed
   ```

2. **Sync Settings**:
   ```
   Settings → Accounts → Disable unnecessary sync
   ```

3. **Network Settings**:
   ```
   Settings → Network & internet → Data usage → Data saver
   Enable data saver
   ```

## App Issues

### Apps Crashing

#### General Fixes
1. **Clear App Cache**:
   ```
   Settings → Apps → Select app → Storage → Clear cache
   ```

2. **Clear App Data**:
   ```
   Settings → Apps → Select app → Storage → Clear storage
   ```

3. **Reinstall App**:
   ```
   Settings → Apps → Uninstall app
   Reinstall from F-Droid/Play Store
   ```

#### System Apps
1. **Reset App Preferences**:
   ```
   Settings → Apps → See all apps → Three dots menu
   Reset app preferences
   ```

2. **Wipe Dalvik Cache**:
   ```
   Boot to TWRP → Wipe → Advanced Wipe
   Select Dalvik/ART Cache
   ```

### Apps Not Installing

#### Installation Issues
1. **Check Storage Space**:
   ```
   Settings → Storage → Free up space if needed
   ```

2. **Unknown Sources**:
   ```
   Settings → Apps → Special app access
   Install unknown apps → Allow for your source
   ```

3. **Corrupted APK**:
   - Redownload the APK
   - Check file integrity

#### Google Play Issues
1. **Clear Play Store Cache**:
   ```
   Settings → Apps → Google Play Store → Storage → Clear cache
   ```

2. **Reset Play Store**:
   ```
   Settings → Apps → Google Play Store → Storage → Clear storage
   ```

### App Permissions

#### Permission Denied
1. **Grant Permissions**:
   ```
   Settings → Apps → Select app → Permissions
   Grant required permissions
   ```

2. **Reset Permissions**:
   ```
   Settings → Apps → See all apps → Three dots menu
   Reset app preferences
   ```

## Network Issues

### WiFi Problems

#### Connection Issues
1. **Forget Network**:
   ```
   Settings → Network & internet → WiFi
   Select network → Forget
   Reconnect with correct password
   ```

2. **Reset Network Settings**:
   ```
   Settings → System → Reset options → Reset WiFi, mobile & Bluetooth
   ```

3. **IP Configuration**:
   ```
   Settings → Network & internet → WiFi → Network details
   Change IP settings to DHCP
   ```

#### Advanced Fixes
1. **DNS Issues**:
   ```
   Settings → Network & internet → Advanced → Private DNS
   Set to "Automatic" or custom DNS
   ```

2. **MAC Address Randomization**:
   ```
   Settings → Network & internet → WiFi → Network details
   Disable MAC address randomization
   ```

### Mobile Data Issues

#### Data Connection
1. **Airplane Mode Toggle**:
   ```
   Quick Settings → Airplane mode ON → Wait 30s → OFF
   ```

2. **APN Settings**:
   ```
   Settings → Network & internet → Mobile network → Access Point Names
   Reset to default APN
   ```

3. **SIM Issues**:
   - Remove and reinsert SIM card
   - Try SIM in another device
   - Contact carrier for SIM replacement

### Bluetooth Problems

#### Pairing Issues
1. **Forget Device**:
   ```
   Settings → Connected devices → Previously connected devices
   Forget problematic device
   ```

2. **Reset Bluetooth**:
   ```
   Settings → System → Reset options → Reset WiFi, mobile & Bluetooth
   ```

3. **Device-Specific Issues**:
   - Update device firmware
   - Check device compatibility

## Audio Issues

### No Sound

#### Audio Troubleshooting
1. **Volume Check**:
   ```
   Hardware buttons → Increase volume
   Check all volume sliders in Settings → Sound
   ```

2. **Safe Mode Test**:
   ```
   Boot to Safe Mode → Test audio
   If works, issue is with third-party app
   ```

3. **Audio Settings**:
   ```
   Settings → Sound & vibration → Reset sound settings
   ```

#### Speaker Issues
1. **Clean Speaker Grill**:
   - Remove debris from speaker openings
   - Use compressed air carefully

2. **Audio Output**:
   ```
   Settings → Sound & vibration → Sound quality and effects
   Reset audio enhancements
   ```

### Microphone Problems

#### Mic Testing
1. **Voice Recorder Test**:
   ```
   Open Voice Recorder app → Test recording
   ```

2. **Call Test**:
   - Make a test call
   - Check if other party can hear you

3. **App Permissions**:
   ```
   Settings → Apps → Voice Recorder → Permissions
   Grant microphone permission
   ```

## Display Issues

### Screen Problems

#### Touch Screen Issues
1. **Calibration**:
   ```
   Settings → System → Developer options → Pointer location
   Touch screen to test responsiveness
   ```

2. **Clean Screen**:
   - Clean screen with microfiber cloth
   - Remove screen protector if damaged

3. **Safe Mode Test**:
   ```
   Boot to Safe Mode → Test touch
   If works, issue is with third-party app
   ```

#### Display Quality
1. **Resolution Check**:
   ```
   Settings → Display → Display size
   Adjust display size slider
   ```

2. **Color Calibration**:
   ```
   Settings → Display → Advanced → Colors
   Reset color calibration
   ```

### Black Screen Issues

#### Black Screen Fixes
1. **Brightness Check**:
   ```
   Hardware buttons → Increase brightness
   Check auto-brightness setting
   ```

2. **Power Cycle**:
   ```
   Hold Power button 20+ seconds
   Wait 1 minute, then power on
   ```

3. **Recovery Boot**:
   ```
   Boot to recovery → Check if display works
   If works, issue is with system
   ```

## System Issues

### Overheating

#### Temperature Management
1. **Check Temperature**:
   ```
   Use apps like "CPU-Z" or "Device Info HW"
   Monitor temperature
   ```

2. **Cooling Measures**:
   - Remove case if using one
   - Avoid direct sunlight
   - Close background apps

3. **Performance Mode**:
   ```
   Settings → Battery → Battery optimization
   Set to "Optimized" or "High performance"
   ```

### Random Reboots

#### Stability Issues
1. **Recent Changes**:
   - Uninstall recently installed apps
   - Check for app updates
   - Review recent system changes

2. **Safe Mode Test**:
   ```
   Boot to Safe Mode
   If stable, issue is with third-party app
   ```

3. **System Updates**:
   ```
   Settings → System → System update
   Install any available updates
   ```

### Storage Full

#### Storage Management
1. **Storage Analysis**:
   ```
   Settings → Storage → Free up space
   Review storage usage breakdown
   ```

2. **Clear Cache**:
   ```
   Settings → Storage → Free up space → Clear cache
   ```

3. **Move to SD Card**:
   ```
   Settings → Apps → Select app → Storage → Change storage
   Move compatible apps to external storage
   ```

## Advanced Troubleshooting

### Log Collection

#### System Logs
```bash
# ADB logcat
adb logcat > system_log.txt

# Kernel logs
adb logcat -b kernel > kernel_log.txt

# Specific app logs
adb logcat | grep "com.example.app" > app_log.txt
```

#### Recovery Logs
```
TWRP → Advanced → Copy Log
Save to external storage
```

### Hardware Diagnostics

#### Hardware Tests
1. **Device Test Apps**:
   - "Hardware Test" apps from Play Store
   - Test sensors, hardware components

2. **Built-in Tests**:
   ```
   Dial *#*#4636#*#* → Phone information → Run ping test
   Dial *#*#34971539#*#* → Camera firmware info
   ```

### Recovery Options

#### TWRP Recovery Issues
1. **Reinstall TWRP**:
   ```
   Boot to bootloader → fastboot flash recovery twrp.img
   ```

2. **Stock Recovery**:
   - Flash stock recovery if available
   - Use device-specific tools

#### Bootloader Issues
1. **Fastboot Commands**:
   ```bash
   fastboot devices
   fastboot reboot
   fastboot oem unlock
   ```

2. **Bootloader Unlock**:
   - Check device-specific unlock method
   - Follow OEM instructions carefully

## Getting Help

### Community Support
1. **BMobile Forums**: Check official forums
2. **XDA Developers**: Device-specific threads
3. **Reddit**: r/BMobile or r/android
4. **GitHub Issues**: Report bugs officially

### Information to Provide
When seeking help, include:
- Device model and variant
- BMobile version
- Steps to reproduce issue
- Screenshots/logs when possible
- Recent changes made

### Professional Help
1. **Local Repair Shops**: For hardware issues
2. **Manufacturer Support**: Warranty claims
3. **Authorized Service Centers**: Official repairs

## Prevention Tips

### Regular Maintenance
1. **Weekly Cache Clear**: Clear app caches regularly
2. **Monthly Updates**: Keep system and apps updated
3. **Storage Management**: Maintain 20%+ free space

### Best Practices
1. **Backup Regularly**: Create backups before changes
2. **Test Changes**: Try modifications one at a time
3. **Document Setup**: Keep notes on your configuration

### Monitoring
1. **System Monitoring**: Use monitoring apps
2. **Battery Health**: Track battery performance
3. **Storage Trends**: Monitor storage usage patterns

Remember: Most issues have solutions. Start with basic troubleshooting, gather information, and don't hesitate to ask for help when needed!