# MANDATORY READING

**Please backup your projects before updating!** This is a WIP custom firmware, and there are probably going to be a lot of bugs, regressions etc. and your project data *could* be put at risk.

If you're using a beta build, please keep in mind that **BETA = BETA**. Beta builds may contain destructive changes from build to build. I strongly recommend against working on anything critical on beta builds. If you want to live on the edge, please be especially vigilant about reading the changelog before updating, and back up your data!

You can make backups either by saving snapshots if you have a +DRIVE (GLOBAL > FILE > SNAPSHOTS > SAVE), or better yet, by making SysEx backups (GLOBAL > FILE > SYSEX SEND).

If you're doing SysEx backups, be sure to verify them afterwards, either by sending them back via GLOBAL > FILE > SYSEX RECV > VERF, or by using Elektron C6 (check for any 'broken' messages at the bottom of the window).

In this firmware, SONG slots 13-24 are removed to make room for extended data. If you have anything on those slots, back them up first (GLOBAL > FILE > SYSEX SEND > SONG+P+K / 013-024), or move them to slots 1-12. **Any SONG data remaining in slots 13-24 WILL become corrupted on boot**. Existing SNAPSHOT data stored on the +DRIVE is preserved, as long as you don't overwrite it while the custom firmware is installed.

To install the firmware, turn on your Monomachine while holding FUNC, and select option 5. Send the firmware syx via the device's MIDI IN port.
