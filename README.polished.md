# NOTICE
This polished version is still in the making. Please be patient!!

# Ditch Enrollment
A guide on how to unenroll Chromebooks with different kernel versions.

## Table of Contents:
* [Unenrollment](#unenrollment)
* [Questions](#questions)
* [Keyrolled: Kernver 6](#keyrolled-kernver-6)
* [USB-less Exploits](#usb-less-exploits)
* [Payloads](#payloads)
* [Links](#links)

> [!WARNING]
> I am not held responsible for ANY trouble you get in using this repo

## Requirements
- A USB stick with at least **8 GB** of storage
- Another computer (Preferably with Linux installed)

## Necessary Knowledge Before Reading
You will need to know your Chromebook's board name and kernel version to pick a method.

You can see your board name by going to [`chrome://version`](chrome://version):

![Partial chrome://version screenshot, with the baseboard "`dedede`" visible and a red arrow pointing to the baseboard name.](/images/arrow_to_baseboard_in_chrome-version.png)

or more complicatedly, find your customization ID in the "Diagnostics" app and search it at [crOS.tech](https://cros.tech/):

![Partial Diagnostics app screenshot, with the text "`sasukette, version 150.16700.0`" visible, and a red arrow pointing to said text.](/images/arrow_to_customID_in_diag.png)

![Partial crOS.tech screenshot, with the text "`sasukette`" already written inside the search bar.](/images/searching_sasukette_in_crOS.tech.png)

![Partial crOS.tech screenshot, with Chrome's URL bar visible on top, with the URL [cros.tech/device/sasukette/](https://cros.tech/device/sasukette/), and a red arrow pointing to the text "BOARD: DEDEDE" in the contents of the crOS.tech page.](/images/arrow_to_baseboard_in_crOS.tech.png)

## Unenrollment Methods

### KV1: SH1MMER
1. Open [crOS.download's RMA Shims page](https://cros.download/shims)

![Partial screenshot of the RMA Shims page, with the header and a few board shims visible.](/images/crOS.download_RMA_Shims_page.png)

2. Download the ZIP archive with your board name (in my case, `dedede`)

![Partial screenshot of the RMA Shims page and the in-built Chrome search function, with the search query "dedede" already typed in.](/images/searching_for_dedede_in_crOS.download-shims.png)

4. After downloading your corresponding shim, open the [Wax4Web](https://sh1mmer.me/builder) builder.
  - After finishing, Wax4Web will (try to) download a file with the name `injected-shim.bin`. It's better practice to rename the file to something like `sh1mmer-dedede.bin` for example, if you're doing this on multiple boards, or just want to use the image in the future without going through the building process all over again.

5. You'll now need to flash the shim to a USB stick. This can be done with any program that takes in ISOs, since `.bin`s, `.img`s and `.iso`s are all the same in this situation. (don't take this at face value!) You can use [Rufus](https://rufus.ie), [Balena Etcher](https://etcher.balena.io/), or if you did this process on a Chromebook with unblocked extensions, you can use the [Chromebook Recovery Utility](https://chromewebstore.google.com/detail/chromebook-recovery-utili/pocpnlppkickgojjlmhdmidojbmbodfm).

6. After the USB stick is fully flashed, you'll connect the newly-flashed USB stick to your Chromebook (if it isn't already), and boot into the shim. The process is simple, you'll first enter Recovery Mode by pressing `Esc+⟳+⏻` (`Esc +  Refresh + Power`), then enter Developer Mode (`Ctrl+D` → `Enter`). If all goes well, you should see this screen:

![An image of the "Developer Mode is blocked by policy" screen](/images/dev_mode_is_disabled_by_policy.jpeg)

You'll then use the key combo to enter Recovery Mode once again, and you should boot into SH1MMER.

After that, you can select the "Unenroll" option, but you can also choose any other payload you desire.

# KERNVER 2, v120 CRYPTOSMITE:
so head over to: https://github.com/FWNavy/CryptoSmite/blob/main/cryptosmite.md
and download the stateful.tar.xz and st.tar.xz files.
then use [Wax4Web](https://sh1mmer.me/builder) to get a injected-shim.bin file and then flash onto Your USB Via, [Chromebook Recovery Utility](https://chromewebstore.google.com/detail/chromebook-recovery-utili/pocpnlppkickgojjlmhdmidojbmbodfm?hl=en) then select use local image.

<img width="792" height="538" alt="image" src="https://github.com/user-attachments/assets/cef135d4-ef65-4d54-92ea-b7c01568ed78" />

Then just wait for the image to finish Downloading and then press the keys: (esc+refresh+power) and you should see this screen: 

<img width="1347" height="1000" alt="image" src="https://github.com/user-attachments/assets/c9915277-1e28-4202-8348-7c1576b81ffd" />

Then plug in Your USB Drive, and Hooray!!! You should Be Unenrolled Now!



# KERNVER: ALL KERNVERS: DAUB:
so head over to: https://dl.snerill.org/Daub then download the shim corresponding to your boardname, then flash onto USB via Chromebook Recovery Utility, then press and hold down the keys: (esc+refresh+power) then plug in your USB drive then just wait. Then you should be unenrolled now! Hooray!

# KERNVER 3, v124 OlyBmmer: so first get a RECOVERY IMAGE, NOT AN RMA SHIM:  [CROS.DOWNLOAD](https://cros.download/recovery)
and download that, afer thats done head over to, the BadRecovery Web Builder: https://binbashbanana.github.io/badrecovery/ and then you'll get a BadRecovery .bin file then flash that .bin file onto The USB Via [Chromebook Recovery Utility](https://chromewebstore.google.com/detail/chromebook-recovery-utili/pocpnlppkickgojjlmhdmidojbmbodfm?hl=en) then  press the keys: (esc+refesh+power) and Then: Plug in Your USB Drive and then just wait, Then you should be unenrolled now! Hooray!


# KERNVER 4, v130 ICARUS:
So head over to here: https://dl.snerill.org/icarus to get your RMA shim (Corresponding to your Board Name)
So after you unenroll go to WiFi-Settings, then Change the Proxy Type to Manual. And to Host your own proxy here: https://www.youtube.com/watch?v=trqwRNPcVV4
AND AFTER HOSTING ICARUS ON YOUR OWN COMPUTER, MAKE SURE TO THAT After unenrolling change back to direct internet connection in proxy settings

# KERNVER 5, v133 Br0ker:
So first get your Br0ker shim from here: https://github.com/ading2210/sh1mmer/releases/tag/2025.9.19 and btw IGNORE THE ASSETS SECTION. SO first download the RMA shim corresponding to your Boardname and then flash with chromebook recovery utility, then press the keys (esc+refresh+power) then plug in Your USB then just wait, and then yeah your unenrolled after that!


# KERNVER 6, v141 QUICKSILVER:
# so first head over to https://dl.snerill.org/QuickSilver then download the shim, corresponding to your boardname, then unzip the file and flash the .bin file onto your USB and then boot into quicksilver by pressing, esc+refresh+power then plug in/insert your usb and there you go, goodjob!



# KEYROLLED: KERNVER 6: 
There are five methods, : https://github.com/crosbreaker/badbr0ker or Visit https://github.com/crosbreaker/badsh1mmer or https://dl.snerill.org/BadSilver and https://github.com/crosbreaker/baddieapple. So First head over to: https://dl.snerill.org/ and select your method. Then after the file is done downloading, unzip the file then flash onto a USB drive, via  [Chromebook Recovery Utility](https://chromewebstore.google.com/detail/chromebook-recovery-utili/pocpnlppkickgojjlmhdmidojbmbodfm). Then press the keys: (esc+refresh+power) then plug in your USB Drive. and then Hooray Your Unenrolled Now!


# Dededeicarus
> [!WARNING]
> DEDEDEICARUS IS ONLY FOR KEYROLLED DEDEDE CHROMEBOOKS IF YOUR CHROMEBOOK IS NOT A DEDEDE BOARD, THEN DEDEDEICARUS IS NOT FOR YOUR CHROMEBOOK
# INSTRUCTIONS ARE ON HERE: https://github.com/crosbreaker/dededeicarus



# Credits:
# Mercury Workshop Team, ading2210, FWNavy, BinBashBannana, Kkilobyte and Crosbreaker


# QUESTIONS:

## What Kernver and ChromeOS version do I have?

# *(You can find your Kernver version by pressing, esc+refresh+power and pressing Tab, Its the line that reads: tpm_kernver=0x00010004, if it reads that, Then Your Kernver is 4, and for your chromeos version you just have to press, Alt+V on then sign-in screen and you'll see your version.)*



# And What should I do After Unenrolling?



# ANSWER: I WOULD USE MURKMOD AFTER UNENROLLING SUCCESFULLY BECAUSE MURKMOD SPOOFS THE FACT THAT THE CHROMEBOOK GOT UNENROLLED, BECAUSE IF YOU DON'T USE MURKMOD AFTER UNENROLLING YOUR SYSADMIN WILL PROBABLY FIGURE OUT THAT THE CHROMEBOOK IS UNENROLLED FROM THE GOOGLE ADMIN CONSOLE
(MURKMOD LINK: https://github.com/rainestorme/murkmod)



# What even is Keyrolling?


# So Keyrolling is where newer boardnames, (Like Nissa) are like LOCKED DOWN so you can't just like unenroll without Newer Methods (Like BadSH1mmer) and stuff like that# So Keyrolling is where newer boardnames, (Like Nissa) are like LOCKED DOWN so you can't just like unenroll without Newer Methods (Like BadSH1mmer) and stuff like that

# Payloads

# SH1MMER and Br0ker

<img width="1366" height="768" alt="sh1mmer" src="https://github.com/user-attachments/assets/dca4aabf-6caa-4037-bb6b-791ee3f2ddfd" />

# BadRecovery or (OlyBmmer)


<img width="3024" height="4032" alt="badrecovery" src="https://github.com/user-attachments/assets/67461f1c-d6e1-4728-8f4f-41bda4aedfc3" />

# Links 
# (Kept for Archival Purposes)

# SH1MMER: https://github.com/MercuryWorkshop/sh1mmer
# Cryptosmite: https://github.com/FWNavy/CryptoSmite
# DAUB: https://dl.snerill.org/Daub
# OlyBmmer: https://github.com/BinBashBanana/badrecovery
# Icarus: https://github.com/cosmicdevv/Icarus-Lite]
# Br0ker: https://github.com/ading2210/sh1mmer/releases/tag/2025.9.19
# Quicksilver: https://dl.snerill.org/QuickSilver

# USB-less Exploits:

# KERNVER 1, REQUIRES ChromeOS v101 and below: SHroot
1. open crosh, (ctrl+alt+t)
2. paste the following in:
3. ```set_cellular_ppp \';dbus-send${IFS}--system${IFS}--print-reply${IFS}--dest=org.chromium.SessionManager${IFS}/org/chromium/SessionManager${IFS}org.chromium.SessionManagerInterface.ClearForcedReEnrollmentVpd;exit;\'```
4. press enter
5. Just like this:

6. <img width="1217" height="216" alt="crosh-rootesc" src="https://github.com/user-attachments/assets/9ab2be14-337d-468a-bcc6-ee9a950e42f4" />



## ChromeOS v129 and below - BadApple + Icarus
Basically, this abuses both BadApple and Icarus, all without a USB flash drive (unless you need to downgrade). BadApple is an exploit in Ti50/2023+ devices that abuses the Internet Recovery to access a root shell, from which you can use Icarus.
1. Ensure you on on ChromeOS v129 or lower, if you are on KV4, downgrade to a version like v126, if you are on v132, this will not work.
2. Enter recovery using Esc+refresh+Pwr. If you downgraded from ChromeOS v132, go to Options, then select `Internet Recovery (old)`. If you did not downgrade, just select normal `Internet Recovery`.
3. Wait for MiniOS to load, then go through the setup process until you get to Wi-Fi setup. Here you need to login to a Wi-Fi network, and then STOP.
4. Now you press Ctrl+Alt+F3, if it shows a black screen, repeat step 2 but open `Internet Recovery (old)`.
5. On an Android or Linux device, use Termux/Terminal to host Icarus_



## CRSH2TTY: All versions (PATCHED!)
CRSH2TTY has been patched! It will no longer work for ANY Chromebook because it was a server-side bug. The steps remain below for archival purposes.

CRSH2TTY is a very funny exploit. It's a cool universal USB-less exploit that should not even work at all yet it has been tested on many devices, including new ones like `nissa craaskbowl` or `dedede boten` to extremely old ones like `peppy` or `clapper`. No one is exactly sure how this works, but it requires two 2-second waits and then one 15-hour wait to work.

1. Powerwash using `ctrl+shift+q+q` and then `ctrl+alt+shift+r`. If this doesn't work, press `esc+⟳+⏻ ` (`esc+refresh+power`) and then `ctrl+d`, and then `enter`.
2. Proceed through ChromeOS setup as normal.
3. When it starts to enroll, wait 2 seconds then restart by preforming an EC reset by pressing `⟳+⏻ ` (`refresh+power`).
4. When it starts to enroll again, wait 2 seconds and press the recovery shortcut, `esc+⟳+⏻ ` (`esc+refresh+power`) then `⏻ ` (`power`) to turn it off.
5. Leave it off for ***15 hours*** or more.
6. Once 15 hours is up, turn on the Chromebook. You should be greeted at the `Welcome to your Chromebook` screen, you should already be connected to Wi-Fi, so press `Get started`.
7. On the `Get connected` screen, just press `Next`, you should see `Getting your device ready`, wait on this screen, and then you should see `Choose your Chromebook's setup`. 
9. Hooray!!!
<img src="/img/tutorial/craaskbowl-unroll-google.png" width="400">
