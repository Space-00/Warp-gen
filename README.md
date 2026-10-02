# Cloudflare WARP Config Generator for AmneziaWG and Clash
Do not run the scripts locally, as Roskomnadzor (RKN) has blocked the requests needed to fetch the configuration. Instead, it is better to run them on remote servers. Below are a few suitable services that provide free, temporary servers.
## 1. WARP for AmneziaWG
### Option 1: Killercoda
1. Go to https://killercoda.com/playgrounds/scenario/ubuntu
2. Log in via Google.
3. Once the login process is complete, a terminal will appear. Paste the command (Shift + Insert):
```bash
bash <(wget --inet4-only -qO- https://raw.githubusercontent.com/ImMALWARE/bash-warp-generator/main/warp_generator.sh)
```
4. After the config is generated, copy it and paste it into a new text file. Alternatively, to download it as a file, highlight the link, press Ctrl + C, and then paste it into your browser's address bar. Import the file into [AmneziaWG](https://wiki.malw.link/network/vpns/amneziawg) or [AmneziaVPN](https://wiki.malw.link/network/vpns/amneziavpn).

### Option 2: Replit
1. Go here: [![Run on Repl.it](https://repl.it/badge/github/replit/upm)](https://replit.com/new/github/ImMALWARE/bash-warp-generator)
2. Log in or create an account.
3. In the central tabbed panel, open a new tab and select **Console**. 4. Click the **▶️Project** button (it might be labeled **▶️Run .replit run command**).
5. Enter the command in Terminal 1 to generate the AmneziaWG config and press Enter.
6. Once the config is generated, it will be saved as `warp.conf`. In the right-hand menu, click "File Tree," then right-click on `warp.conf` and select "Download."
Alternatively, you can copy the config from the terminal and paste it into a new text file. Or, to download it as a file, highlight the link, press Ctrl + Shift + C, and paste it into your browser's address bar. Import the file into [AmneziaWG](https://wiki.malw.link/network/vpns/amneziawg) or [AmneziaVPN](https://wiki.malw.link/network/vpns/amneziavpn).

### Option 3: GitHub Codespaces
1. Go to this link: https://github.com/ImMALWARE/bash-warp-generator/codespaces
2. Log in to GitHub.
3. Click **`Create codespace on main`**.
4. Wait for the environment to load. This may take 10–30 seconds.
5. If the terminal does not appear at the bottom of the screen, go to the top menu and select Terminal -> New Terminal. Then, paste the following command into the terminal (Shift + Insert):
```bash
bash warp_generator.sh
```
6. Once the config is generated, it will be saved as `warp.conf`. In the left-hand file menu, right-click on `warp.conf` and select "Download."
Alternatively, you can copy the config from the terminal and paste it into a new text file. Alternatively, to download it as a file, highlight the link, press Ctrl + Shift + C, and then paste it into your browser's address bar. Import the file into [AmneziaWG](https://wiki.malw.link/network/vpns/amneziawg) or [AmneziaVPN](https://wiki.malw.link/network/vpns/amneziavpn).

## 2. WARP MASQUE for Clash
### Option 1: Killercoda
1. Go to https://killercoda.com/playgrounds/scenario/ubuntu
2. Log in via Google.
3. Once the login process completes, a terminal will appear. Paste the command (Shift + Insert):
```bash
bash <(wget --inet4-only -qO- https://raw.githubusercontent.com/ImMALWARE/bash-warp-generator/main/masque_generator.sh)
```
4. After the config is generated, copy it and paste it into a new text file. Alternatively, to download it as a file, highlight the link, press Ctrl + C, and then paste it into your browser's address bar. Connection instructions are provided below.

### Option 2: Replit
1. Go here: [![Run on Repl.it](https://repl.it/badge/github/replit/upm)](https://replit.com/new/github/ImMALWARE/bash-warp-generator)
2. Log in or create an account.
3. In the right-hand panel, open a new tab and select **Console**.
4. Click the **▶️Project** button (it might be labeled **▶️Run .replit run command**).
5. Enter `2` in the terminal to generate the MASQUE config and press Enter. 6. Once the config is generated, it will be saved as `warp-masque-clash.yaml`. In the right-hand menu, click "File Tree," then right-click on `warp-masque-clash.yaml` and select "Download."
Alternatively, you can copy the config from the terminal and paste it into a new text file. Or, to download it as a file, highlight the link, press Ctrl + Shift + C, and paste it into your browser's address bar. Connection instructions are provided below.

### Option 3: GitHub Codespaces
1. Go to this link: https://github.com/ImMALWARE/bash-warp-generator/codespaces
2. Log in to GitHub.
3. Click **`Create codespace on main`**
4. Wait for the environment to load. This may take 10–30 seconds.
5. If a terminal does not appear at the bottom of the screen, go to the top menu and select Terminal -> New Terminal. Then, paste the following command into the terminal (Shift + Insert):
```bash
bash masque_generator.sh
```
6. Once the config is generated, it will be saved as `warp-masque-clash.yaml`. In the left-hand file menu, right-click on `warp-masque-clash.yaml` and select "Download".
Alternatively, you can copy the config from the terminal and paste it into a new text file. Or, to download it as a file, highlight the link, press Ctrl + Shift + C, and then paste it into your browser's address bar. Connection instructions are provided below.

## Connecting to WARP via the MASQUE protocol
### Clash Verge Rev for Windows, macOS, Linux

1. Install Clash Verge Rev.

Windows: https://github.com/clash-verge-rev/clash-verge-rev/releases/download/v2.5.2/Clash.Verge_2.5.2_x64-setup.exe

macOS ARM: https://github.com/clash-verge-rev/clash-verge-rev/releases/download/v2.5.2/Clash.Verge_2.5.2_aarch64.dmg

macOS Intel: https://github.com/clash-verge-rev/clash-verge-rev/releases/download/v2.5.2/Clash.Verge_2.5.2_x64.dmg

Linux deb: https://github.com/clash-verge-rev/clash-verge-rev/releases/download/v2.5.2/Clash.Verge_2.5.2_amd64.deb

AUR: `clash-verge-bin`

2. Go to the "Profiles" section on the left.
3. Click "NEW". Set the Type to "Local". Click "SELECT FILE" and choose the downloaded `warp-masque-clash.yaml` config. Click "SAVE". <img src="https://wiki.malw.link/img/network/vpns/warp/clash-verge-create-profile.png" class="center" width="600px">
4. Right-click on the newly appeared profile and select "Select".
5. Go to the "Proxy" section on the left.
6. Click on the "PROXY" block. "WARP-Masque" should appear. Click "Check" on the right side of it.
<img src="https://wiki.malw.link/img/network/vpns/warp/clash-verge-check.png" class="center" width="600px">

If a number appears where "Check" was, that is the ping value. This means the connection to WARP was successful. Go to the "Home" section on the left, select "TUN Mode" in the network settings, and enable it. This ensures all device traffic goes through WARP.

If "Timeout" is displayed, the connection to WARP failed. However, it is worth trying a few times, as it doesn't always work on the first attempt.
### FlClash for Android
1. Download and install the FlClash APK: https://github.com/chen08209/FlClash/releases/download/v0.8.94/FlClash-0.8.94-android-arm64-v8a.apk
2. Go to the "Profiles" section. Tap "Add Profile" -> "File" -> Select the config file.
3. Go to the "Proxy" section. Tap "Latency Test". If a number appears, that is the ping value. This means the connection to WARP was successful. Go to the "Dashboard" section and enable the VPN by tapping the ▶️ button. If "Timeout" appears, the connection to WARP failed. However, it is best to try a few times, as it doesn't always work on the first attempt.
### Clash Mi for iOS
1. Install Clash Mi: https://apps.apple.com/us/app/clash-mi/id6744321968?l=ru
2. Go to "Profiles" -> tap the "+" button at the top -> "Import configuration file." Select the downloaded `warp-masque-clash.yaml` config file.
3. Select the newly added config from the list of profiles.
4. Turn on the VPN using the toggle switch at the top of the main screen.
5. Verify it is working by opening a website, such as https://ipinfo.io/what-is-my-ip.

# Common errors in AmneziaWG apps

## Two consecutive commas: ","

For some reason, the config was generated incorrectly. Delete it and try generating it again using a different method, or download a working one.

## Invalid tunnel name: "WARP (1)"

Rename the .conf file; the filename must not contain spaces or parentheses.

## Invalid key for the [Interface] section: "s1"

You need to import the WARP config into AmneziaWG or AmneziaVPN, not WireGuard!

## Invalid name

In the AmneziaWG mobile app, the config name must not exceed 15 characters.

## Enable WireGuard obfuscation

If the S1 and S2 values ​​are missing from the config, AmneziaVPN will prevent you from connecting and suggest enabling obfuscation. The AmneziaWG app can read such malformed configs, but using them is still not recommended. ## Unable to create Wintun interface

### Solution 1: Deleting a registry entry
1.  Open the Windows Registry Editor. You can find it via search or by running the command `regedit`.
2.  Navigate to **HKEY_CLASSES_ROOT** -> **CLSID**. Find and delete the key `{3d09c1ca-2bcc-40b7-b9bb-3f3ec143a87b}`.
3.  Restart the AmneziaWG application.

### Solution 2: Reinstalling AmneziaWG as administrator:

1.  Uninstall AmneziaWG via "Programs and Features".
2.  Copy the full path to the AmneziaWG installer .msi file. To do this, **hold down Shift**, right-click the file, and select "Copy as path".
3.  Open the Command Prompt as administrator.
4.  Paste the copied path into the Command Prompt by right-clicking inside the window, then press Enter.

This will launch the MSI file with administrator privileges. This may resolve the issue.

### Solution 3: Removing the Wintun driver:

1.  Uninstall AmneziaWG via "Programs and Features".
2.  Open the Command Prompt as administrator.
3.  Run the following commands:
```bat
dism /online /get-drivers /format:table > drivers.txt
notepad drivers.txt
```
4.  Find `wintun.inf`. You need the corresponding OEM number. In my case, it is `oem7.inf`:
<img src="https://wiki.malw.link/img/network/vpns/amneziawg/wintun-inf.png">
5.  Run the command to remove it:
```bat
pnputil.exe /d oem7.inf
```
Replace "7" with the number that corresponds to `wintun.inf` in your Notepad file!
6.  Copy the full path to the AmneziaWG installer .msi file. To do this, **hold down Shift**, right-click the file, and select "Copy as path".
7.  Paste the copied path into the command prompt by simply right-clicking inside the window, then press Enter. Install AmneziaWG.

### Solution 4: AmneziaVPN instead of AmneziaWG

The [AmneziaVPN](https://wiki.malw.link/network/vpns/amneziavpn) application fully supports AmneziaWG protocol configurations.

## Local network connections not working

Open the configuration file for editing:

<img src="https://wiki.malw.link/img/network/vpns/amneziawg/edit-tunnel.png"/>

Uncheck the "Block non-tunneled traffic" box.

## "Failed to set IPv4: error: Destination address required" on macOS

Remove the [IPv6 address](https://en.wikipedia.org/wiki/IPv6) from the configuration file.
