# You (as Maintainer)

1. MUST UPLOAD
All device sources are used for building the image on the hentaiOS-Devices Organization. these should be fully buildable. Using external repositories isn't allowed unless it's coming from LineageOS or Sony Open Devices Project (SODP).

2. MUST UPLOAD Changelogs for each build. These RECOMMENDED be user-friendly. simplifying the changelog for the average user who doesn't know technical jargon like SafetyNet, but still illustrates what changes have been made since the last update.

3. MUST HAVE conducted internal tests before pushing OTA Updates to users. Each build has to be thoroughly checked by the maintainer and all hardware and software functionality MUST be tested before the build is pushed to production.

4. MUST MAINTAIN authorship of Git commits that are pushed. These are mandatory requirements for ALL repositories, Force-pushes are acceptable.

5. In the event of any disagreements between maintainers, sort them via Direct Messages, don't take any of that into chats or threads, approach the Internal Boards if you want something sorted out quickly.

6. MUST NOT add any of the following:

    - Any features in their device-specific packages, e.g XiaomiParts, KCAL, Camera API2 Enforcement, etcetera, in an exception if that feature is available on stock firmware, e.g Alert Slider and Offscreen Gestures for OnePlus Devices, Fingerprint Gestures, Dirac Sound, or any Audio Enhancer that's part of stock firmware, otherwise, it can't be shipped.

7. In the case of A/B or Dynamic Partitioned devices, you MUST NOT ship TWRP prebuilt, it MUST ship AOSP Recovery.

**If any of these rules are violated, The Management Board will take direct action against the maintainer with or without prior warning.**
