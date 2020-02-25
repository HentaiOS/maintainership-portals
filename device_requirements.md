# Device Requirements

1. The device has to use SELinux Enforcing to release builds

2. The device has to use FBE (File-Based Encryption)

3. The device must have the same hardware compatibility following the stock firmware, i.e. if IR Blaster works in stock firmware, it has to work on hentaiOS.

4. The device must pass SafetyNet OOB (Out-Of-Box) without any third-party modifications. Custom build fingerprints may be used in accordance with our guidelines.

5. The device has to not including any unused overlays and packages. This includes but not limited to packages not being built, packages that didn't work, obsolete and deprecated packages, untested and placebo "tweaks" or any packages that introduced any unnecessary and/or unwanted features.

6. The devices mustn't have the need for a lot of patches, and if a patch has to be applied for it, it has to be in accordance with the following

    - Needed for building the image, boot, or having the device working properly (e.g Fingerprint-On-Display)
    - Proper authorship and commit message
    - Be as minimal and polished as possible
