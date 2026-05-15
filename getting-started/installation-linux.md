# Installing Dolphin Anty on Linux

Dolphin Anty supports Linux with the same features available on Windows and macOS.

## Download

Go to [dolphin-anty.com/download/linux](https://dolphin-anty.com/download/linux/) and download the Linux build.

## Install

1. Open a terminal in the directory where you saved the downloaded file
2. Make the file executable:
   ```bash
   chmod +x dolphin-anty-*.AppImage
   ```
3. Run the application:
   ```bash
   ./dolphin-anty-*.AppImage
   ```

## First launch

On first launch, Dolphin Anty downloads required browser components. Wait for this process to complete before attempting to log in or create profiles.

## Dependencies

If the application fails to start, you may need to install missing system libraries. Common dependencies include:

```bash
sudo apt-get install libglib2.0-0 libgtk-3-0 libnss3 libgbm1
```

For other distributions, install the equivalent packages using your package manager.

## Troubleshooting

If you encounter issues specific to Linux, contact support via the widget on [dolphin-anty.com/support](https://dolphin-anty.com/support/) or through the Telegram bot `@dolphinsupport_en_bot`.
