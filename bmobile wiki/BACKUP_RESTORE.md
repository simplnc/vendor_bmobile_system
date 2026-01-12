# Backup & Restore Tutorial

This tutorial covers how to safely backup your data and restore it when using BMobile.

## Why Backup?

Before making any changes to your Android device, creating a backup is crucial:
- **Data Loss Prevention**: Protect your personal data, photos, and settings
- **Easy Recovery**: Quickly restore your device if something goes wrong
- **Peace of Mind**: Experiment with confidence knowing you can revert changes

## Types of Backups

### 1. TWRP Recovery Backup
The most comprehensive backup method using custom recovery.

#### Creating a TWRP Backup

1. **Boot into Recovery**:
   ```
   Power off your device
   Hold Volume Down + Power to enter recovery
   ```

2. **Navigate to Backup**:
   - Select "Backup" from TWRP main menu
   - Choose backup location (internal/external storage)

3. **Select Partitions**:
   - [x] System
   - [x] Data
   - [x] Boot
   - [x] Optional: EFS, Modem, etc.

4. **Start Backup**:
   - Swipe to backup
   - Wait for completion (may take 10-30 minutes)

#### Restoring from TWRP Backup

1. **Boot into Recovery**
2. **Navigate to Restore**:
   - Select "Restore" from main menu
   - Choose your backup file

3. **Select Partitions to Restore**:
   - Usually restore all partitions

4. **Restore**:
   - Swipe to restore
   - Wait for completion and reboot

### 2. ADB Backup (Data Only)
For backing up individual apps and data via USB.

#### Prerequisites
- Enable USB Debugging in Developer Options
- Install ADB on your computer
- Connect device via USB

#### Creating ADB Backup
```bash
# Backup all apps and data
adb backup -apk -shared -all -f backup.ab

# Backup specific app
adb backup -apk com.example.app -f app_backup.ab

# Backup without APK (data only)
adb backup -noapk -shared -all -f data_only.ab
```

#### Restoring ADB Backup
```bash
# Restore backup
adb restore backup.ab
```

**Note**: ADB backup requires password setup on device

### 3. Cloud Backup Solutions

#### SeedVault (Recommended)
BMobile includes SeedVault for secure, encrypted backups:

1. **Setup SeedVault**:
   - Go to Settings > System > Backup
   - Enable backup and choose storage location
   - Set up encryption password

2. **Manual Backup**:
   - Open SeedVault app
   - Select "Backup now"
   - Choose data to backup

3. **Automatic Backups**:
   - Enable automatic backups
   - Set backup schedule

#### Other Cloud Options
- **Nextcloud**: Self-hosted cloud storage
- **Decentralized Storage**: IPFS or similar
- **Avoid Google Drive**: For privacy reasons

### 4. App-Specific Backups

#### Signal Backup
```bash
# Export Signal backup
Settings > Chats > Chat backups > Create backup
```

#### Session Backup
Session automatically syncs across devices - no manual backup needed.

#### Browser Bookmarks
- **DuckDuckGo**: Sync via DuckDuckGo account (privacy-focused)
- **Alternative**: Export bookmarks manually

## Backup Best Practices

### Pre-ROM Installation
1. **Full TWRP Backup**: Before flashing any ROM
2. **External Storage**: Copy backups to PC/external drive
3. **Verify Backups**: Test restore functionality

### Regular Backups
- **Weekly**: For active users
- **Before Changes**: Before installing apps, mods, or updates
- **Before Rooting**: Always backup before root procedures

### Storage Strategy
- **Multiple Locations**: Store backups in at least 2 places
- **External Drives**: Use USB drives for offline storage
- **Cloud Encryption**: Encrypt cloud backups
- **Naming Convention**: Use descriptive names with dates

```
Format: DeviceName-ROM-Version-Date-Type.ab
Example: Pixel5-BMobile-2024-01-15-FullBackup.ab
```

## Restore Scenarios

### After Failed ROM Installation
1. Boot into recovery
2. Wipe system, data, cache
3. Restore from TWRP backup
4. Reboot

### App Data Recovery
1. Install app from F-Droid/Google Play
2. Use ADB to restore app data
3. Or use SeedVault restore

### Partial Restore
- Restore only system partition for ROM changes
- Restore only data for app recovery
- Selective partition restore when possible

## Troubleshooting Backups

### Common Issues

#### TWRP Backup Fails
- **Free Space**: Ensure adequate storage space
- **File System**: Check storage health
- **Permissions**: Some partitions may require special access

#### ADB Backup Issues
- **USB Debugging**: Verify developer options enabled
- **USB Connection**: Try different USB ports/cables
- **Driver Issues**: Install proper USB drivers

#### Restore Problems
- **Version Mismatch**: Ensure backup from same/similar ROM version
- **Storage Corruption**: Verify backup file integrity
- **Encryption Issues**: Ensure correct password/keys

### Verification Steps
```bash
# Check backup file integrity
ls -la /path/to/backup/

# Verify TWRP backup contents
# Boot into TWRP and check backup folder
```

### Recovery Commands
```bash
# Emergency ADB commands
adb reboot recovery
adb reboot bootloader

# Check device connection
adb devices
```

## Advanced Backup Techniques

### Encrypted Backups
- Use VeraCrypt for container-based backups
- Enable FDE (Full Disk Encryption) before backup
- Use cryptsetup for Linux-based encryption

### Automated Backups
- **Tasker**: Automate backup schedules
- **Scripts**: Create custom backup scripts
- **CI/CD**: Automated testing environment backups

### Network Backups
```bash
# Backup over network (advanced)
adb backup -apk -shared -all | ssh user@server 'cat > backup.ab'
```

## Maintenance

### Backup Rotation
- Keep last 3-5 backups
- Delete old backups regularly
- Archive important backups

### Testing Restores
- **Quarterly**: Test restore procedures
- **Before Major Changes**: Always test before important modifications
- **Document Process**: Keep notes on successful restore procedures

### Backup Security
- **Encrypt All Backups**: Never store unencrypted sensitive data
- **Secure Storage**: Use password managers for backup passwords
- **Access Control**: Limit who can access backup files

## Recommended Tools

### Free & Open Source
- **TWRP**: Custom recovery with backup features
- **ADB**: Android Debug Bridge
- **SeedVault**: Android backup solution
- **Bacula**: Enterprise backup solution

### Commercial Options
- **Acronis**: Professional backup software
- **EaseUS**: User-friendly backup tools
- **Macrium Reflect**: Disk imaging software

## Emergency Recovery

### If Device Won't Boot
1. Boot into recovery mode
2. Try restore from backup
3. If restore fails, clean flash ROM again
4. Restore data backup separately

### Data Recovery Services
- **Professional Services**: For physically damaged devices
- **Software Tools**: TestDisk, Recuva for deleted file recovery
- **Chip-off Recovery**: Advanced data recovery (expensive)

Remember: Regular backups are your safety net. Always backup before making changes, and test your restore process regularly.