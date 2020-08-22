<div align="center">
  <h1>Windows 10 Setup Script</h1>

**"Windows 10 Setup Script" is a set of tweaks for OS fine-tuning and automating the routine tasks**
</div>


## Core features

- Set up Privacy & Telemetry;
- Turn off diagnostics tracking scheduled tasks;
- Set up UI & Personalization;
- Uninstall OneDrive "correctly";
- Interactive prompts;
- Change %TEMP% environment variable path to %SystemDrive%\Temp
- Change location of the user folders programmatically (without moving user files) within interactive menu using up/down arrows and Enter key to make a selection
  - "Desktop";
  - "Documents";
  - "Downloads";
  - "Music";
  - "Pictures"
  - "Videos.
- Uninstall UWP apps from all accounts with exception apps list with pop-up form written in [WPF](#Screenshots);
- Turn off Windows features;
- Remove Windows capabilities with pop-up form written in [WPF](#Screenshots);
- Create a Windows cleaning up task in the Task Scheduler;
  - A toast notification will pop up a minute before the task [starts](#Screenshots)
- Create tasks in the Task Scheduler to clear
  - %SystemRoot%\SoftwareDistribution\Download
  - %TEMP%
- Unpin all Start menu tiles;
- Pin shortcuts to Start menu using [syspin.exe](http://www.technosys.net/products/utils/pintotaskbar)
  - Three shortcuts are preconfigured to be pinned: Control Panel, "old style" Devices and Printers, and Command Prompt
- Turn on Controlled folder access and add protected folders using dialog menu;
- Add exclusion folder from Microsoft Defender Antivirus scanning using dialog menu;
- Add exclusion file from Microsoft Defender Antivirus scanning using dialog menu;
- Refresh desktop icons, environment variables and taskbar without restarting File Explorer;
- Many more File Explorer and context menu "deep" tweaks.

## Usage

To run the script:

- Download [up-to-date version](https://github.com/farag2/Setup-Windows-10/releases);
- Expand the archive;
- Check whether .ps1 is encoded in **UTF-8 with BOM**;
- Set execution policy to be able to run scripts only in the current PowerShell session

  ```powershell
  Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process -Force
  ```

- Run .ps1 file via powershell.exe with elevated privileges;
  - or launch Start.cmd as Administrator.

## Supported Windows 10 versions

|Version|Code name|   Marketing name   |Build | Arch |      Editions     |
|:-----:|:-------:|:------------------:|:----:|:----:|:-----------------:|
| 2004  |  20H1   |   May 2020 Update  |19041 |  x64 |Home/Pro/Enterprise|
| 1909  |  19H2   |November 2019 Update|18363 |  x64 |Home/Pro/Enterprise|
| 1903  |  19H1   |   May 2019 Update  |18362 |  x64 |Home/Pro/Enterprise|
| 1809  |         |LTSC Enterprise 2019|17763 |  x64 |   Enterprise      |

## GUI version (C#)

[oz-zo](https://github.com/oz-zo) still cooking (moved to the private repository)

## 21H1 test version
https://gist.github.com/farag2/5a6d9952247aefe42ba81a9d95507765

## Microsoft Docs

- [Release information](https://docs.microsoft.com/en-us/windows/release-information)
- [Known issues for 1909](https://docs.microsoft.com/en-us/windows/release-information/status-windows-10-1909)
- [Known issues for 2004](https://docs.microsoft.com/ru-ru/windows/release-information/status-windows-10-2004)

## Ask a question on

- [Habr](https://habr.com/en/post/465365/)
- [Ru-Board](http://forum.ru-board.com/topic.cgi?forum=62&topic=30617#15)
- [4PDA](https://4pda.ru/forum/index.php?s=&showtopic=523489&view=findpost&p=95909388)
- [My Digital Life](https://forums.mydigitallife.net/threads/powershell-script-setup-windows-10.81675/)
- [Reddit](https://www.reddit.com/r/PowerShell/comments/go2n5v/powershell_script_setup_windows_10/)
