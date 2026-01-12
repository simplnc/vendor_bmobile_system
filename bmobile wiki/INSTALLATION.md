# BMobile Installation Guide

This guide will walk you through installing BMobile on your Android device.

## Prerequisites

- **Compatible Device**: Ensure your device is supported by LineageOS
- **Unlocked Bootloader**: Your device must have an unlocked bootloader
- **Custom Recovery**: TWRP or similar recovery installed
- **Backup**: Backup all important data before proceeding

## Pre-Installation Steps

1. **Charge your device**: Ensure battery is at least 50% charged
2. **Backup data**: Create a full backup of your current system
3. **Download files**:
   - BMobile ROM zip file
   - Latest TWRP recovery image
   - Google Apps (optional, not recommended for privacy)

## Installation Steps

### Step 1: Boot into Recovery
1. Power off your device completely
2. Boot into recovery mode (usually Volume Down + Power)
3. If needed, flash the latest TWRP recovery

### Step 2: Wipe Data
1. In TWRP, select "Wipe"
2. Select "Advanced Wipe"
3. Check the following:
   - [x] Dalvik/ART Cache
   - [x] System
   - [x] Data
   - [x] Cache
4. Swipe to wipe

### Step 3: Flash BMobile ROM
1. Return to main TWRP menu
2. Select "Install"
3. Navigate to your BMobile ROM zip file
4. Swipe to install
5. Wait for installation to complete

### Step 4: Optional - Install Google Apps
**Note**: We recommend against installing Google Apps for maximum privacy
1. If you must install GApps, flash them after the ROM
2. Reboot to recovery if needed
3. Install GApps zip
4. Reboot

### Step 5: First Boot
1. Reboot your device
2. The first boot may take 5-10 minutes
3. Follow the setup wizard
4. Configure your privacy settings

## Post-Installation Setup

1. **Security Setup**:
   - Set up screen lock
   - Configure biometric authentication
   - Review app permissions

2. **Privacy Configuration**:
   - Disable unnecessary location services
   - Review and configure network permissions
   - Set up firewall rules if available

3. **App Installation**:
   - The ROM comes with pre-installed privacy apps
   - Install additional FOSS apps from F-Droid

## Troubleshooting

### Boot Loop
- Wipe cache and retry
- Check if your device is compatible

### App Crashes
- Clear app data/cache
- Check for updates

### Performance Issues
- Disable animations in Developer Options
- Use lightweight launchers

## Support

If you encounter issues, check our troubleshooting section or community forums.