# Kali Linux Live USB: Portable Cybersecurity Environment

## 1. Project Overview

### Objective

The goal of this project was to create a portable Kali Linux environment using a USB flash drive and Rufus, then test whether it could boot successfully on a separate laptop without installing Kali Linux onto its internal drive.

A Live USB makes it possible to run a Linux operating system directly from removable media. This is useful for learning Linux, exploring cybersecurity tools, and conducting authorized security testing in a portable environment.

### Key Objectives

- Download the official Kali Linux Live ISO.
- Create a bootable USB using Rufus.
- Configure the USB to boot using the computer's BIOS/UEFI boot menu.
- Test Kali Linux on a separate laptop.
- Understand the benefits and limitations of a non-persistent Live environment.

### Why a Non-Persistent Live USB?

A standard non-persistent Live session generally does not retain changes made to the Live system after a reboot. This provides a convenient way to return to a fresh environment for another session.

However, non-persistence does not guarantee that no traces remain elsewhere. Network activity, files saved to other drives, firmware settings, and activity on the host operating system may leave records. For this reason, I treat the Live USB as a portable environment rather than an automatically anonymous or completely untraceable system.

## 2. Hardware and Tools

| Component        | Details                            |
| ---------------- | ---------------------------------- |
| Host computer    | Windows PC used to prepare the USB |
| Test computer    | Acer laptop                        |
| USB drive        | SanDisk 16 GB flash drive          |
| USB imaging tool | Rufus 4.15                         |
| Operating system | Kali Linux Live, 64-bit AMD64      |
| ISO image        | `kali-linux-2026.2-live-amd64.iso` |

## 3. Implementation

### Step 1: Downloading the Kali Linux Image

I downloaded the Kali Linux Live ISO from the official Kali Linux website.

Official download page: [https://www.kali.org/get-kali/#kali-live](https://www.kali.org/get-kali/#kali-live)

The Live image was selected because the objective was to run Kali from removable media rather than install it on the test laptop.

### Step 2: Preparing the USB Drive

I connected the SanDisk 16 GB USB flash drive to the Windows computer.

The drive had previously been used for another operating system project, so I checked that the correct USB device was selected before proceeding. Writing the Kali image erased the existing contents of the selected USB drive.

### Step 3: Writing the Image with Rufus

I opened Rufus and selected the downloaded Kali Linux ISO.

Rufus detected the ISOHybrid image structure and prompted me to use DD image writing mode. I selected the appropriate option and allowed Rufus to write the image to the USB drive.

After the writing process finished, Rufus displayed the `READY` status.

**Important:** Selecting the wrong drive when writing an image can erase unrelated data. The target device should always be verified before starting.
<img width="469" height="600" alt="image" src="https://github.com/user-attachments/assets/2ede3c4d-cf51-4185-96ce-8afc4f7d67b0" />

<img width="451" height="591" alt="image" src="https://github.com/user-attachments/assets/cae2efb5-136a-4992-b0d5-af04d1fb3fb9" />

### Step 4: Booting on the Acer Laptop

After preparing the USB drive, I connected it to the Acer laptop and opened the computer's boot menu during startup using the F12 key.

I located the USB entry identified as `USB HDD : SanDisk` and selected it to boot from the flash drive.

The Kali boot menu appeared, allowing me to choose the Live System option.
<img width="2560" height="1920" alt="image" src="https://github.com/user-attachments/assets/91997fef-fd61-4296-9002-86582cd586f7" />


### Step 5: Starting the Live Session

I selected `Live System (amd64)` from the Kali boot menu.

This option starts Kali Linux without requiring a conventional installation onto the internal drive. I used the session to verify that the system could boot from the USB and reach the Kali desktop.

A successful boot demonstrates that the USB image and the laptop's boot configuration were compatible. It does not, by itself, verify that every hardware component or cybersecurity tool works correctly.

<img width="2560" height="1920" alt="image" src="https://github.com/user-attachments/assets/7a9e0af7-dd98-44fe-a464-6704ee6be0e5" />



## 4. Testing and Verification

The following checks can be recorded after testing the system:

| Test                                         | Result               |
| -------------------------------------------- | -------------------- |
| Kali ISO downloaded from the official source | Completed            |
| USB image written using Rufus                | Completed            |
| USB detected in the boot menu                | Completed            |
| Kali Live System started                     | verified             |
| Wi-Fi, audio, and other hardware tested      | all works            |
| Session changes discarded after reboot       | confirmed |
| Internal drive left unchanged                | confirmed            |

The main test was whether Kali Linux could boot from the SanDisk USB drive and start a Live session on the Acer laptop.

A separate reboot test can be used to check whether session changes persist. Any such test should use a harmless temporary file and should not involve important data.

## 5. Security Considerations and Limitations

### Non-Persistence

A standard non-persistent Live session generally discards changes to the Live system when the session ends. Persistence can be added separately, so the actual configuration matters.

### Host Storage

Booting from USB avoids a conventional installation onto the internal drive, but it does not prove that the drive was never accessed or modified. Avoid mounting or writing to internal storage when it is not needed.

### Privacy and Network Traffic

A Live USB does not automatically anonymize network activity. I did not treat Tor, Anonsurf, or Nipe as configured components unless they were separately installed, configured, and tested.

### Authorized Use

Kali Linux contains security-testing tools. Any scanning, exploitation, or other security testing should be restricted to systems I own or have explicit permission to test.

## 6. Challenges and Lessons Learned

This project helped me understand the practical process of preparing bootable Linux media and selecting a USB device from a computer's boot menu.

Key lessons:

- The Live ISO and Installer ISO serve different purposes.
- Rufus may offer different writing modes depending on the image.
- BIOS/UEFI boot menus make it possible to select removable boot media.
- A successful boot is only the first verification step; individual hardware and tools may need further testing.
- Non-persistence, privacy, and anonymity are separate concepts and should not be treated as interchangeable.

## 7. Conclusion

I prepared a Kali Linux Live USB using Rufus and used an Acer laptop to test the boot process.

The project provided practical experience with Linux boot media, removable operating systems, and BIOS/UEFI boot selection. It also highlighted the importance of distinguishing a portable Live environment from a fully isolated or anonymous system.

Future improvements could include testing additional hardware compatibility, verifying session behavior after reboot, and documenting a small authorized lab exercise performed from the Live environment.

## 8. References

- Kali Linux official downloads: [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)
- Kali Linux Live USB documentation: [https://www.kali.org/docs/usb/](https://www.kali.org/docs/usb/)
- Rufus official website: [https://rufus.ie/](https://rufus.ie/)
