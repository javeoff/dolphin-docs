# Common Mistakes When Creating a Profile

Avoid these mistakes to get the most out of your browser profiles.

## Changing default fingerprint settings unnecessarily

The defaults Dolphin Anty generates are based on real device data. Overriding them without a specific reason often makes the profile less convincing to anti-fraud systems.

**What to do instead:** Create a profile with default settings, test it, and only adjust parameters if you have concrete evidence that a change is needed.

## Using the wrong OS for your device

Setting a profile to Windows while running Dolphin Anty on macOS creates detectable inconsistencies in system fonts and other signals.

**What to do instead:** Match the profile OS to your actual device OS.

## Sharing one proxy across multiple profiles

Using the same IP address for multiple profiles allows platforms to link those accounts together.

**What to do instead:** Assign a unique proxy to each profile.

## Opening a profile on two devices at once

Simultaneous access to the same profile from different machines causes sync conflicts and data loss.

**What to do instead:** Stop the profile on one device before opening it on another.

## Installing extensions inside profile windows

Adding extensions directly inside a profile's browser window causes unexpected behavior and malfunctions.

**What to do instead:** Go to the **Extensions** section in the Dolphin Anty main menu and install extensions from there.

## Ignoring the Do Not Track parameter

Enabling "Do Not Track" makes the profile stand out — fewer than 5% of real users have this enabled.

**What to do instead:** Leave the Do Not Track parameter at its default value.

## Not keeping enough free disk space

Profiles store their data locally. Running low on disk space (less than 10–15 GB free on the system drive) causes `Error 409: Datadir damaged` and data corruption.

**What to do instead:** Monitor available disk space and free up storage before it becomes critical.
