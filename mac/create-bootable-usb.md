# Create bootable usb

1. Download the installer in the app store.
2. Create the bootable usb drive using the `createinstallmedia` utility:

```bash
sudo <installer-path>/Contents/Resources/createinstallmedia --volume /Volumes/<your-volume-name>
```
