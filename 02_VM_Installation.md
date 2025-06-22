# 02 – Setting Up Kali Linux in VirtualBox (Complete Guide)

### Prerequisites

* Oracle VirtualBox installed.
* Kali Linux ISO (64-bit or ARM) from [kali.org](https://www.kali.org).

---

## 🔁 Step-by-Step Installation (Windows/macOS/Linux Hosts)

### 1. Download

* From **kali.org**, get the “Installer Image” (choose 64-bit for desktop/laptop).

### 2. Install VirtualBox

* Download from [virtualbox.org](https://www.virtualbox.org).
* Run the installer and accept any driver prompts (e.g. for the network adapter).

### 3. Create the Virtual Machine

-1. Open VirtualBox → Click **New**
-2. Name: "Kali Linux(use preferred name)"
-3. Type: **Linux**
-4. Version: **Debian (64-bit)**
-5. Allocate memory: ~ 15-25% of total RAM (e.g., 4 GB for 16 GB system)
-6. Hard disk:

   * Choose "Create a virtual hard disk now"
   * Storage: **Dynamically allocated**
   * Size: **20–25 GB**

### 4. Boot from ISO

* Select your VM → **Settings → Storage**
* Under **Controller: IDE**, select **Empty**
* Click the CD icon → Choose a disk file → Select your Kali `.iso`

### 5. Install Kali in the VM

-1. Start the VM → Choose **Graphical Install**
-2. Select language, location, and keyboard layout
-3. Configure hostname and domain (can leave domain blank)
-4. Set up user and password
-5. Disk partitioning:

   * Choose "Guided – use entire disk"
   * Accept default partition scheme

-6. Confirm "Write changes to disk"
-7. Select **No** for network mirror
-8. When asked, install **GRUB bootloader** → Choose "Enter device manually"

### 6. Complete Setup

* Wait for files to copy → Reboot when prompted
--------------------------------------------------------------------------------

**⚠️ Boot Issue Note**: On some systems, Kali might not automatically boot into the correct EFI partition after installation. If this happens:

1. At the EFI shell prompt, type `map` to list available drives.
2. Identify the correct bootable partition, usually labeled `FS0:`.
3. Start Kali manually with the command:

  FS0:\EFI\kali\grubaa64.efi
   
4. Once booted, Kali will function normally. You can later configure persistent EFI boot.

   *- helpful visual guide for persistent EFI, check out this YouTube video:
     - https://www.youtube.com/watch?v=YCegkcVheJA         Credit: OldTechBloke (YouTube Channel)
             

* Log in with the user account you created

---

## ✅ Outcome

A fully functional Kali Linux VM is now installed, ready for command-line learning, tool usage, and cybersecurity experiments in an isolated, safe environment.

You can now launch the terminal with `CTRL + ALT + T` or click the terminal icon.
