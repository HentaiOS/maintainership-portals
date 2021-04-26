# Performance and Internals Guidelines

1. Scheduler

    1.a. If you're running in WALT, we advise you to **NOT** using Touch Boosting and instead, picking this [commit](https://github.com/tytydraco/kernel_oneplus_sm8150/commit/41b92705a22b2d701b685ae879c1cc8174487c61#diff-50484c19f1afdaf3841a0d821ed393d2) and this [commit](https://github.com/tytydraco/kernel_oneplus_sm8150/commit/a1fe57e5366a6ec36b5a247f798503ae6702dc2f#diff-50484c19f1afdaf3841a0d821ed393d2) into your kernel.

    1.b. Following the prior, we also advise you to not overly boosting everything, because **Performance is not "all-about-boosting".** Efficiency is all that matters in this case.

    1.c. We advise you to tune your CPUSet according to your SoC, every SoC has its specific CPUSet tuning, so make sure you correctly tune it according to your SoC.

2. ZRAM

   2.a. We advise you to ship ZRAM depending on your device RAM size

   2.b. **We DON'T RECOMMEND keeping the ZRAM compression backend in LZO for performance reasons!** We recommend you to use Zstandard (zstd) as default ZRAM and ZSWAP (if your devices use this, Smugsungs?) compression backend as it'll be beneficial for the compression ratio and faster compared to LZO, you also can use lz4 for the compression backend if you favoring performance over compression ratio. [Example commit from Disrupt Kernel Xiaomi-sdm845 for zstd zram](https://github.com/RaphielGang/spins_kernel_xiaomi_sdm845/commit/e8cac3f9a761224f5355355eeb5513b67f770fc9).

3. MSM-IRQBalance

   3.a. We advise you to blacklist msm_drm and kgsl_3d0 IRQs, [Example commit from AOSPA OnePlus-sdm845](https://github.com/AOSPA/android_device_oneplus_sdm845-common/commit/7e590e891ac9b3b83d95543b88a1516a016038f5), keep in mind that changes may vary between all devices, so make sure you blacklisted the correct IRQ.

   3.b. Following the prior, Divide the IRQ's affinity, [Example commit from AOSPA OnePlus-sdm845](https://github.com/AOSPA/android_device_oneplus_sdm845-common/commit/e317060e5e03b11787ad727a6e08c204f7b39d13), following prior guidelines, make sure you divided the correct IRQ.

4. The use of compilation flags

   We don't advise you to generically build your images under a generic CPU variant. We recommend you to use your SoC-specific optimization flags instead of using generic compilation flags as we aren't going to ship Generic System Image.

5. Kernel Default Configurations

   5.a. We advise you to ship your kernel default configuration (known as "defconfig") as-is without any masking.

   5.b. The use of Google kernel/configs is recommended.
