# 2020-motorola-one-hyper

This document describes how to install OmniROM on Motorola One Hyper.

## Motorola One Hyper

### Specs

* [Motorola UK](https://www.motorola.co.uk/smartphones-motorola-one-hyper/p).
* [Lenovo UK](https://www.lenovo.com/gb/en/phones/moto/motorola-one/motorola-one-hyper/p/PMIPMCI21MJ).
* [GSMArena](https://www.gsmarena.com/motorola_one_hyper-9944.php).

### Disinfecting

[Cleaning your Motorola phone](https://support.motorola.com/uk/en/products/cell-phones/motorola-one-family/motorola-one-hyper/documents/MS149245)
> It is OK to use disinfecting wipes with 70% isopropyl alcohol to gently wipe your display.
> When disinfecting or cleaning your device, we recommend that you turn it off and avoid getting any moisture in its openings, including the charging port, headphone jack, microphones and speakers.
>
> Do not submerge your Motorola phone in any cleaning agents, avoid using any cleaners with bleach or abrasives, and avoid spraying cleaners directly on the screen.

> While this does not disinfect your Motorola phone, the best way to keep your Motorola phone clean is to wipe it thoroughly with a dry soft cloth.
> Avoid abrasive cloths, including paper towels and other materials with rough surfaces.

## OmniROM and Motorola One Hyper

Motorola One Hyper is listed among [OmniROM devices](https://omnirom.org/#devices) as unofficial.
Builds are published weekly with [microG](https://dl.omnirom.org/def/) and [GApps](https://dl.omnirom.org/tmp/def/).

[How to install OmniROM](https://docs.omnirom.org/Installing_Omni_on_your_device):

> 1. Unlock the bootloader.
>    ...
> 2. Install TWRP (a custom recovery).
>    TWRP is the only recovery officially supported by Omni.
>    ...
>    TWRP recovery images can be flashed (installed) ... via fastboot with the `fastboot flash recovery <recovery_file_name.img>` command from a computer for unlocked bootloaders.
>    ...
> 3. Download Omni ROM ...
>    ...
>    You can ... download the ROM to your computer and transfer it over USB ... .
> 4. Boot into recovery, do a factory reset, and install Omni ROM.
>    ...

## Unlock the Bootloader on Motorola One Hyper

From [How do I tell if my device has an unlockable/re-lockable bootloader?](https://support.motorola.com/us/en/Solution/MS92011):

> First is whether the device ships with a bootloader that is capable of being unlocked or re-locked.
> Second is whether the wireless carrier that sells the device allows the bootloader to be unlocked ... .
>
> ... please check the [bootloader introduction page][unlock].
> You will be able to check whether your device shipped with an unlockable bootloader.
> We will be adding devices to this list regularly.

[unlock]: https://motorola-global-portal.custhelp.com/app/standalone/bootloader/unlock-your-device-a

From the [bootloader introduction page][unlock]:

> NOTE: You will be asked to sign up/register to continue on.

> Can the bootloader on your device model be unlocked?
> Find out here >>>

[What devices are supported by the Bootloader Unlock program?](https://support.motorola.com/us/en/solution/MS87215):

> If your device is not listed below, feel free to visit [here](https://motorola-global-portal.custhelp.com/app/standalone/bootloader/unlock-your-device-a/action/auth) and follow the process to see if it is unlockable.

> * Bootloader unlock codes are not available from Moto or Amazon, for Amazon Prime devices.

> motorola one ... [Support](http://www.motorola.com/mymotoone)

Such page lists Motorola One Hyper and links to [its support page](https://support.motorola.com/uk/en/products/cell-phones/motorola-one-family/motorola-one-hyper).

### Impact

From [After I unlock my device bootloader, am I still eligible to receive software upgrades from Motorola?](https://support.motorola.com/us/en/Solution/MS91999):

> Unlocking your bootloader does not affect your eligibility to receive over-the-air (OTA) upgrades from Motorola.
> Upgrade packages to new versions of Android will be pushed to all eligible devices, regardless of their bootloader locking status.
>
> Nevertheless, there are some cases when the upgrade delivery or upgrade process might fail:
> * Applying an OTA upgrade patch might fail if you have modified some components ... .
> * Delivering a software upgrade image to your device will be impossible if you have replaced Motorola's original software with a custom Android ROM.
>   ... as our OTA software upgrade services have been removed from your device.

From [Can I re-lock my device after I have unlocked the bootloader?](https://support.motorola.com/us/en/Solution/MS92000):

> Yes, by re-loading an original Motorola software image and re-locking the bootloader.
> After relocking your device, you will only be able to reflash your device with a signed system image.
> If such an image is not available online, you will have to send it to MOTOROLA support for reflashing.
> ... Regardless of whether your device is re-locked, such device is still not covered by the MOTOROLA warranty.

From [Bootloader - Re-lock a device and revert to original software](https://support.motorola.com/us/en/solution/MS91987):

> Bootloader is a bit of code that tells your device's operating system how to boot up.
> Some developers [unlock the code][unlock] to customize the device.
> Re-locking a bootloader will ensure that the device will only boot to Motorola signed and provided Android Images.
>
> PLEASE NOTE: Re-locking a device will not reinstate your device warranty as damage might have occurred when the device was unlocked.
>
> To return to Original Software, you will need to reflash a Motorola signed software image to your device ... .
