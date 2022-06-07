# Checksums for Released Portmaster Artifacts

Find the main project repository here: [safing/portmaster](https://github.com/safing/portmaster)

Verify installers on Linux:

```sh
# Download installers
wget https://updates.safing.io/latest/linux_amd64/packages/portmaster-installer.deb
wget https://updates.safing.io/latest/linux_amd64/packages/portmaster-installer.rpm
# Download checksums
wget https://raw.githubusercontent.com/safing/checksums/master/sha256_installers.txt
wget https://updates.safing.io/sha256_installers.txt -O sha256_installers_safing.txt
# Verify checksums
sha256sum --check --ignore-missing sha256_installers.txt
sha256sum --check --ignore-missing sha256_installers_safing.txt
```

Verify all articats on Linux:

```sh
# Go to Portmaster updates directory
cd /opt/safing/portmaster/updates
# Download checksums
wget --quiet https://raw.githubusercontent.com/safing/checksums/master/sha256.txt -O - | sudo tee sha256.txt
# Verify checksums
sha256sum --check --ignore-missing sha256.txt
```

#### Contribute

Help us add more guides how to verify the checksums on different systems!
