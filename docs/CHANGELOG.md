# Change Log

Notable changes to the PhoenixPE project.

## Release UNRELEASED

### Added

### Changed

### Fixed
- Fixed download links for prime95

### Removed

## Release 2023-03-28

### Added
- Total Commander script
- Default Ramdrive now uses Arsenal Image Mounter. This modern driver developed by the author of ImDisk solves some compatibility issues with modern software. The old ImDisk ramdrive script continues to be available in PhoenixPE, though ImDisk development has ceased.
  * Modern applications that utilize the Windows volume manger API's will work correctly
  * Dynamically allocated Ramdisks can be used, in addition to traditional fixed-size ramdisks.
  * Support for mounting BitLocker-protected volumes.
- New option in Tweaks > Visual Effects to enable/disable rounded corners in Win11. Visual Effects are now enabled by default.
- Added Multi-Monitor option for RDP client sessions.
- iSCSI script to include GUI components of the iSCSI Initiator. 
  * Note: Using iSCSI Initiator with a Win11 source currently requires the Components > Event Logging script to be enabled (Issue #30).

### Changed
- Audio script improvements
  * Updated mpeg123 to v1.31.3
  * added default startup sound
- .Net 6 runtime updated to v6.0.15
- AgentRansack updated to v2022 build 3367
- Bootice script now makes use of JFX's extensions to support multiple languages, DPI support, and dark mode.
- CPU-Z updated to v.2.05.1
- DesktopInfo updated to v3.10.1
- DiskGenius updated to v5.5.0.1488
- EaseUS Data Recovery Wizard updated to v15.8.1.0
- FurMark updated to v1.33.0.0
- Google Chrome updated to v111.0.5563.111
- HWinfo updated to v7.40
- MPC-BE updated to v1.6.6
- Macrium Reflect updated to v8.1.7279
- Moved the "Run All Programs from RAM" checkbox from advanced to basic interface on Config Source script.
- Notepad++ updated to v8.5.1.0
- Notepad3 updated to 6.23.203.2 - fixed broken download URL
- OpenShell updated to v4.4.189
- PowerShell Core updated to v7.3.3
- Rufus updated to v3.22
- Switch to Admin now allows swapping back and forth between Admin and SYSTEM sessions.
- Updated WinNTSetup to 5.3.0
- Ventoy updated to v1.0.90
- Visual C++ 14 Runtime updated to v14.34.31938.0
- WinMerge updated to v2.16.28
- WizTree updated to v4.13

### Fixed
- **Audio now works under the SYSTEM account!** Special thanks to Noel Blanc for the hours spent debugging and analyzing the issue.
- Fixed dependencies for newer versions of PotPlayer
- Fixed a bug in PhoenixAPI AddShortcut that did not properly handle start Minimized or start Maximized.
- Fixed an issue that could cause the ISO file not to be pre-selected in Rufus.
- Fixed %SetupFile% was not defined in Dependencies.script
- Fixed a bug in Network script that could cause .xml wireless profiles not to import correctly.
- Fixed theme signature check bypass for newer Win versions
- Fixed extraction of NSudo binary
- Fixed download button on WinMailPassView script.
- Fixed a bug in RDP script that prevented NLA from being configured in the connection profile.
- Fixed an issue with Ventoy where the latest version was not always extracted after downloading.

### Removed

## Release 2023-01-30

### Added
- StartAllBack (Win11 successor to StartIsBack) as an alternative start menu to OpenShell and StartIsBack++.
- New script that allows the option to use the modern Task Manager instead of the default Task Manger included in boot.wim/WinRE.wim.
- HxD Hex Editor
- MonitorTestUtility script that allows you to run various pattern and motion tests on your display.
- grepWin search and replace script
- Macrium Reflect - Well known backup/imaging solution.
- EaseUS Data Recovery Wizard - Free version allows you to recover up to 2GB of deleted data.
- Double Driver - A user friendly tool for offline driver backup.
- Nirsoft's ExtPassword! - A tool for recovering password from offline systems.
- Nirsoft's WinMailPassRec - A tool for recovering passwords from Win10/Win11 WinMail.
- Nirsoft's ShadowCopyView - Restore files from Volume Shadow Copy snapshots.
- GetBinaryResource command added to PhoenixAPI - Allows extracting of binary resources from exe, dll, etc.
- Zulu JRE 17 LTS script
- Options in MMC script for Certificate Management shortcuts
- Added "Remount Boot Media as Y:" to PECMD SysTray menu.
- Added an option in Misc Shortcuts script to Remount CD/USB as Y (some partition utilities have been known to unmount Y:)

### Changed
- Zulu JRE11 updated to v11.62.17
- Additional Files script defaults to no selected directories. Clicking the browse button creates a default structure in Workbench, but boot.wim and CD/USB now have their own folders. Previously the same directories were defaulted for both CD/USB and boot.wim.
- PCI-Z script now has the option to download the latest pci.ids database directly from the PCI ID Repository. This vastly improves identification as the database that ships with PCI-Z 2.0.0 is from 2017.
- Apps that dynamically download the latest version now log the program version during build.
- PinUtil (1.4.1.1-Homes32) updated to support pinning to StartAllBack.
- KeyboardTestUtility updated to v2.0.0
- HWinfo updated to v7.36
- WinContig added an option to register the WinContig shell extension.
- Open-Shell updated to v4.4.186
  * rewrote the extraction routines to make future updates easier.
  * added Win11 start button option.
- [**Script Breaking Change**] Fab's Auto Backup extraction routines were re-written because author of AutoBackup7 switched to distributing the program in an InnoSetup installer instead of a self-extracting 7z archive.  
  * Support extracting the official InnoSetup installer.
  * Added support for extracting Autobackup files from a .7z/.rar/.zip archive.  
  
  **Note:** Due to the changes the previous self extracting archives can no longer be used. Users must either provide the new InnoSetup package or construct an archive containing their AutoBackup7 program files.
- Improved handling of unsupported keyboard ID's in Localization script. Previously when one or more of the keyboard inputs were set to use HostOS and the language/keyboard pair contained a GUID it would cause DISM to fail with error code 87 (Thanks psct!).
- Set the My Computer > Properties context menu to open the classic System Properties dialog instead of failing to open the Settings App.
- AddShortcut will now detect and remove invalid characters from shortcut names and folders.
- Performance optimizations in CreateISO and OEMInfo scripts
- LetterSwap.exe (Mount CD/USB as Y:) updated to v2019.2.10.1
- Additional audio dll for extended application support.
- HeavyLoad/TreeSizeFree only supports x64 download. Added error message if x86 source is used.
- WinMerge updated to v2.16.26
- AgentRansack updated to v2022 Build 3349
- DMDE updated to v4.0.2.804
- Trellix (Formally McAfee) Stinger download URL's updated.
- Google Chrome updated to v109.0.5414.120
- WinSCP updated to v5.21.7
- Notepad3 updated to v6.23.118.1
- CUP-Z update to v2.04
- Attribute Changer update to v11.10
- PowerShell Core updated to v7.3.2

### Fixed
- Fixed an issue preventing network services from being installed if no NIC's were present.
- Fixed an issue with the Media Transfer Profile script that caused the mtp_helper.sys driver to be extracted to the wrong folder.
- Fixed a bug in InnoCleanup that did not cleanup files with suffixes greater then 1 digit.
- Fixed a bug in InnoRename that caused renamed files to be moved to the base path instead of the correct sub-folder when the NOREC parameter was not used.
- Fixed a bug in Driver Integration where the start menu shortcut would not be created.
- Fixed encoding on WinContig.ini that caused the config to be discarded in newer WinContig versions (5.0.0+).
- Fixed a bug that prevented Mouse ClickLock from being enabled/disabled
- Fixed a bug in Zulu JRE 11 that prevented the JRE from being added to the system PATH
- Fixed an intermittent issue with the transparent icon overlay that caused black icon on explorer refresh. 

### Removed
- Removed depreciated Techbench ISO download link in Config Source. Replaced with alternative ISO download link (https://files.rg-adguard.net/). Best practice remains to use the Download Source ISO button to use Fido, and use rg-adguard as a backup.

## Release 2022-12-25

### Added
- Added Acronis Cyber Protect Home Office script
- Added an option in Explorer script to change the default folder icon view
- Added the ability to login/switch to Administrator
- Added ChrisR's SetWG.exe to reliably set the computer Workgroup for PhoenixPE
  * This is useful for things such as Switch to Admin, as we still need a workgroup set even if we don't run PENetwork.

### Changed
- Added a comment to the Acronis True Image script that the program has been re-branded by the author
- Modified the behavior of Explorer Win11 support. The default has been changed to use explorer.exe included with install.wim, as of Win11 22H2 explorer no longer results in a blackscreen on boot.
- Add missing DLLs for file open dialog in some apps, e.g. notepad++
- .Net6 updated to v6.0.10
- Advanced IP Scanner updated to v2.5.4594.1
- AgentRansack updated to v2022 build 3349
- Aida64 updated to v6.85.6300
- BeyondCompare updated to v4.4.4.27058
- DesktopInfo updated to v3.8.1
- DiskGenius updated to v5.4.6.1441
- DISM Tool updated to v2.6.0
- Driver Store Explorer updated to v0.11.79
- FurMark updated to v1.32.1.0
- Google Chrome updated to v108.0.5359.125
- GPU-Z updated to 2.52.0
- FastStone Image Viewer updated to v7.7
- HWinfo updated to v7.34
- IrfanView updated to v4.62
- LibreOffice updated to v7.4.3
- MPC-BE updated to v1.6.5.3
- Notepad++ updated to v8.4.8.0
- PowerShell Core updated to v7.3.1
- Prime95 updated to v30.8b17
- Updated Rufus to v3.21
- Simplewall updated to v3.6.7
- Ventoy updated to v1.0.81
- WinMerge updated to v2.16.24
- WinSCP updated to v5.21.6
- WizTree updated to v4.12

### Fixed
- Broken download link in OCCT script
- Broken profile update URL in Simplewall script
- A few more workarounds for buggy or missing PENetwork config
- Fixed missing icons in Win11 (context menu, login screen, etc.) due to M$ font changes (SegoeIcons.ttf)
- Fixed an issue with AcronisTrueImage that could occur if drivers already existed in the target.
- Fixed an issue with AcronisCyberProtect that could occur if drivers already existed in the target.
- Fixed an issue with the DiskCyptor script where drivers were not correctly renamed after extraction.
- Fixed some URL and path names for x86/32 bit builds

### Removed
- Homepage link in Windows Login Unlocker script as the forum thread has been deleted :(
 
## Release 2022-08-16
 
**Script Breaking Change:** PhoenixPE now requires PEBakery v1.0.1 or greater due to the use of enhanced looping commands (ForEach, ForRange, While).
 
### Added

- Added an option in the PECMD script to register .wcs file extensions (PECMD scripts)
- Added additional files needed for explorer shell in the latest Win11 insider build
- Added Win11 explorer.exe workaround in Explorer script interface
- Added the ability to extract explorer.exe from a Win10 ISO when building from a Win11 source
- Added Certificate Management mmc snap-in and utils
  * provides the ability to import/export/manage user and computer certificates in WinPE via mmc or standalone utils (certutil.exe/certreq.exe) that may be needed for wireless access, internal servers, etc. in a corporate setting or to backup certificates from an offline system.
- Added SpeedCrunch - an open source calculator app
- Added LibreOffice application script

### Changed
 
- Enhanced FileDeleteEx and DirDeleteEx to allow unlimited retries instead of halting after 1 retry
- Optimize various script loop operations
- Optimized RequireFileEx, FileCopyEx and PinShortcut commands
- Enhancements for Source Image selection in Config Source
- Improvements to VMWare and VirtualBox test VM
  - enable HPET in VMWare to fix BSOD with multiple CPU's enabled
  - revised "Auto" cpu selection to balance guest/host performance
  - disable paravirtulization interface in VirtualBox to improve stability when more then one CPU is defined. This prevents the CPU from consuming all resources initializing multiple CPU's and hanging on boot
  - enable HPET and disable PAE in VirtualBox
- IME Preliminary Japanese IME support (WIP)
- IME Prevent ghost Old Hangul Korean IME from appearing
- Tweaked some error messages
- Misc minor fixes and tweaks
- Updated .NET 6 to v6.0.8
- Updated 7z to v22.00
- Updated AgentRansack to v2022b3335
- Updated AIDA64 to v6.75.6100
- Updated Azul Zulu Java to v11.58.17
- Updated Beyond Compare to v4.4.3.26655
- Updated CPU-Z to v2.0.1
- Updated DesktopInfo to v3.6.0
- Updated FurMark to v1.31.0
- Updated GPU-Z to v2.47.0
- Updated HWinfo to v7.26
- Updated ImDisk to v2.1.1
- Updated LibreOffice to v7.3.5
- Updated MPC to v1.6.3
- Updated Notepad++ to 8.4.4.0
- Updated OpenHashTab to 3.0.2
- Updated OpenShell to v4.4.170
- Updated PowerShell Core to v7.2.6
- Updated Prime95 to v30.8b16
- Updated Rufus to v3.20
- Updated SumatraPDF to v3.4.6
- Updated VC++ 12 to v12.0.40664
- Updated VC++ 14 to v14.32.31332.0 including preliminary support for arm64
- Updated Ventoy to v1.0.79
- Updated WinMerge to v2.16.22
- Updated WinNTSetup to 5.2.6
- Updated WinSCP to v5.21.2

### Fixed

- Fixed an issue with the Launch Program button in DesktopInfo script
- Fix an issue where the WLAN service would not start
- Fixed a bug in Acronis TrueImage affecting iSCISI registration
- Fixed a bug in the SumatraPDF script that could prevent registry hives from being unloaded
- Fixed a rare bug with the AddShortcut command

### Removed

None.
 
## Release 2022-05-22
  
Initial Public Release
