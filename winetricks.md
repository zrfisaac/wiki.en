# Winetricks

**Winetricks** is a script for Wine that helps configure Wine, install libraries, and add additional components that might be needed to run Windows applications more effectively. It provides an easy way to configure Wine and install additional dependencies that many Windows applications require.

## Index

- [Commands](#commands)
  - [Winetricks Force and Silent](#winetricks-force-and-silent)
- [All verbs](#all-verbs)
  - [Apps](#apps)
  - [Benchmarks](#benchmarks)
  - [DLLs](#dlls)
  - [Fonts](#fonts)
  - [Prefix](#prefix)
  - [Settings](#settings)

---

## Commands

### Winetricks Force and Silent

```bash
winetricks --force --unattended mdac28
```

## All verbs

### Apps
|name                     |description|
|-------------------------|-----------|
|`3m_library`             | 3M Cloud Library (3M Company, 2015) [downloadable]|
|`7zip`                   | 7-Zip 19.00 (Igor Pavlov, 2019) [downloadable]|
|`adobe_diged`            |  Adobe Digital Editions 1.7 (Adobe, 2011) [downloadable]|
|`adobe_diged4`           |  Adobe Digital Editions 4.5 (Adobe, 2015) [downloadable]|
|`autohotkey`             |  AutoHotKey (autohotkey.org, 2010) [downloadable]|
|`busybox`                |  BusyBox FRP-4621-gf3c5e8bc3 (Ron Yorston / Busybox authors, 2021) [downloadable]|
|`cmake`                  |  CMake 2.8 (Kitware, 2013) [downloadable]|
|`colorprofile`           |  Standard RGB color profile (Microsoft, 2005) [downloadable]|
|`controlpad`             |  MS ActiveX Control Pad (Microsoft, 1997) [downloadable]|
|`controlspy`             |  Control Spy 6  (Microsoft, 2005) [downloadable]|
|`dotnet20sdk`            |  MS .NET 2.0 SDK (Microsoft, 2006) [downloadable]|
|`dxsdk_aug2006`          |  MS DirectX SDK, August 2006 (developers only) (Microsoft, 2006) [downloadable]|
|`dxsdk_jun2010`          |  MS DirectX SDK, June 2010 (developers only) (Microsoft, 2010) [downloadable]|
|`dxwnd`                  |  Window hooker to run fullscreen programs in window and much more... (ghotik, 2011) [downloadable]|
|`emu8086`                |  emu8086 (emu8086.com, 2015) [downloadable]|
|`ev3`                    |  Lego Mindstorms EV3 Home Edition (Lego, 2014) [downloadable]|
|`firefox`                |  Firefox 51.0 (Mozilla, 2017) [downloadable]|
|`fontxplorer`            |  Font Xplorer 1.2.2 (Moon Software, 2001) [downloadable]|
|`foobar2000`             |  foobar2000 v1.4 (Peter Pawlowski, 2018)|
|`hhw`                    |  HTML Help Workshop (Microsoft, 2000) [downloadable]|
|`iceweasel`              |  GNU Icecat 31.7.0 (GNU Foundation, 2015) [downloadable]|
|`irfanview`              |  Irfanview (Irfan Skiljan, 2016) [downloadable]|
|`kindle`                 |  Amazon Kindle (Amazon, 2017) [downloadable]|
|`kobo`                   |  Kobo e-book reader (Kobo, 2011) [downloadable]|
|`mingw`                  |  Minimalist GNU for Windows, including GCC for Windows (GNU, 2013) [downloadable]|
|`mozillabuild`           |  Mozilla build environment (Mozilla Foundation, 2015) [downloadable]|
|`mpc`                    |  Media Player Classic - Home Cinema (doom9 folks, 2014) [downloadable]|
|`mspaint`                |  MS Paint (Microsoft, 2010) [downloadable]|
|`mt4`                    |  Meta Trader 4 (, 2005) [downloadable]|
|`njcwp_trial`            |  NJStar Chinese Word Processor trial (NJStar, 2015) [downloadable]|
|`njjwp_trial`            |  NJStar Japanese Word Processor trial (NJStar, 2009) [downloadable]|
|`nook`                   |  Nook for PC (e-book reader) (Barnes & Noble, 2011) [downloadable]|
|`npp`                    |  Notepad++ (Don Ho, 2019) [downloadable]|
|`office2003pro`          |  Microsoft Office 2003 Professional (Microsoft, 2002)|
|`office2007pro`          |  Microsoft Office 2007 Professional (Microsoft, 2006)|
|`office2013pro`          |  Microsoft Office 2013 Professional (Microsoft, 2013) [downloadable]|
|`ollydbg110`             |  OllyDbg (ollydbg.de, 2004) [downloadable]|
|`ollydbg200`             |  OllyDbg (ollydbg.de, 2010) [downloadable]|
|`ollydbg201`             |  OllyDbg (ollydbg.de, 2013) [downloadable]|
|`openwatcom`             |  Open Watcom C/C++ compiler (can compile win16 code!) (Watcom, 2010) [downloadable]|
|`origin`                 |  EA Origin (EA, 2011) [downloadable]|
|`protectionid`           |  Protection ID (CDKiLLER & TippeX, 2016)|
|`psdk2003`               |  MS Platform SDK 2003 (Microsoft, 2003) [downloadable]|
|`psdkwin71`              |  MS Windows 7.1 SDK (Microsoft, 2010) [downloadable]|
|`qq`                     |  QQ 8.9.6(Chinese chat app) (Tencent, 2017) [downloadable]|
|`qqintl`                 |  QQ International Instant Messenger 2.11 (Tencent, 2014) [downloadable]|
|`safari`                 |  Safari (Apple, 2010) [downloadable]|
|`sketchup`               |  SketchUp 8 (Google, 2012) [downloadable]|
|`steam`                  |  Steam (Valve, 2010) [downloadable]|
|`ubisoftconnect`         |  Ubisoft Connect (Ubisoft, 2020) [downloadable]|
|`utorrent`               |  µTorrent 2.2.1 (BitTorrent, 2011)|
|`utorrent3`              |  µTorrent 3.4 (BitTorrent, 2011) [downloadable]|
|`vc2005express`          |  MS Visual C++ 2005 Express (Microsoft, 2005) [downloadable]|
|`vc2005expresssp1`       |  MS Visual C++ 2005 Express SP1 (Microsoft, 2007) [downloadable]|
|`vc2005trial`            |  MS Visual C++ 2005 Trial (Microsoft, 2005) [downloadable]|
|`vc2008express`          |  MS Visual C++ 2008 Express (Microsoft, 2008) [downloadable]|
|`vc2010express`          |  MS Visual C++ 2010 Express (Microsoft, 2010) [downloadable]|
|`vlc`                    |  VLC media player 2.2.1 (VideoLAN, 2015) [downloadable]|
|`vstools2019`            |  MS Visual Studio Build Tools 2019 (Microsoft, 2019) [downloadable]|
|`winamp`                 |  Winamp (Radionomy (AOL (Nullsoft)), 2013) [downloadable]|
|`winrar`                 |  WinRAR 6.11 (RARLAB, 1993) [downloadable]|
|`wme9`                   |  MS Windows Media Encoder 9 (broken in Wine) (Microsoft, 2002) [downloadable]|

### Benchmarks
|name                     |description|
|-------------------------|-----------|
|`3dmark03`               |  3D Mark 03 (Futuremark, 2003)|
|`3dmark05`               |  3D Mark 05 (Futuremark, 2005) [downloadable]|
|`3dmark06`               |  3D Mark 06 (Futuremark, 2006)|
|`3dmark2000`             |  3DMark2000 (MadOnion.com, 2000) [downloadable]|
|`3dmark2001`             |  3DMark2001 (MadOnion.com, 2001) [downloadable]|
|`stalker_pripyat_bench`  |  S.T.A.L.K.E.R.: Call of Pripyat benchmark (GSC Game World, 2009)|
|`unigine_heaven`         |  Unigen Heaven 2.1 Benchmark (Unigen, 2010)|
|`wglgears`               |  wglgears (Clinton L. Jeffery, 2005) [downloadable]|

### DLLs
|name                     |description|
|-------------------------|-----------|
|`allcodecs`              |  All codecs (dirac, ffdshow, icodecs, cinepak, l3codecx, xvid) except wmp (various, 1995-2009) [downloadable]|
|`amstream`               |  MS amstream.dll (Microsoft, 2011) [downloadable]|
|`art2k7min`              |  MS Access 2007 runtime (Microsoft, 2007) [downloadable]|
|`art2kmin`               |  MS Access 2000 runtime (Microsoft, 2000) [downloadable]|
|`atmlib`                 |  Adobe Type Manager (Adobe, 2009) [downloadable]|
|`avifil32`               |  MS avifil32 (Microsoft, 2004) [downloadable]|
|`binkw32`                |  RAD Game Tools binkw32.dll (RAD Game Tools, Inc., 2000) [downloadable]|
|`cabinet`                |  Microsoft cabinet.dll (Microsoft, 2002) [downloadable]|
|`cinepak`                |  Cinepak Codec (Radius, 1995) [downloadable]|
|`cmd`                    |  MS cmd.exe (Microsoft, 2004) [downloadable]|
|`cnc_ddraw`              |  Reimplentation of ddraw for CnC games (CnCNet, 2021) [downloadable]|
|`comctl32`               |  MS common controls 5.80 (Microsoft, 2001) [downloadable]|
|`comctl32ocx`            |  MS comctl32.ocx and mscomctl.ocx, comctl32 wrappers for VB6 (Microsoft, 2012) [downloadable]|
|`comdlg32ocx`            |  Common Dialog ActiveX Control for VB6 (Microsoft, 2012) [downloadable]|
|`crypt32`                |  MS crypt32 (Microsoft, 2011) [downloadable]|
|`crypt32_winxp`          |  MS crypt32 (Microsoft, 2004) [downloadable]|
|`d3dcompiler_42`         |  MS d3dcompiler_42.dll (Microsoft, 2010) [downloadable]|
|`d3dcompiler_43`         |  MS d3dcompiler_43.dll (Microsoft, 2010) [downloadable]|
|`d3dcompiler_46`         |  MS d3dcompiler_46.dll (Microsoft, 2010) [downloadable]|
|`d3dcompiler_47`         |  MS d3dcompiler_47.dll (Microsoft, FIXME) [downloadable]|
|`d3drm`                  |  MS d3drm.dll (Microsoft, 2010) [downloadable]|
|`d3dx10`                 |  MS d3dx10_??.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]|
|`d3dx10_43`              |  MS d3dx10_43.dll (Microsoft, 2010) [downloadable]|
|`d3dx11_42`              |  MS d3dx11_42.dll (Microsoft, 2010) [downloadable]|
|`d3dx11_43`              |  MS d3dx11_43.dll (Microsoft, 2010) [downloadable]|
|`d3dx9`                  |  MS d3dx9_??.dll from DirectX 9 redistributable (Microsoft, 2010) [downloadable]|
|`d3dx9_24`               |  MS d3dx9_24.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_25`               |  MS d3dx9_25.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_26`               |  MS d3dx9_26.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_27`               |  MS d3dx9_27.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_28`               |  MS d3dx9_28.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_29`               |  MS d3dx9_29.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_30`               |  MS d3dx9_30.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_31`               |  MS d3dx9_31.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_32`               |  MS d3dx9_32.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_33`               |  MS d3dx9_33.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_34`               |  MS d3dx9_34.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_35`               |  MS d3dx9_35.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_36`               |  MS d3dx9_36.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_37`               |  MS d3dx9_37.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_38`               |  MS d3dx9_38.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_39`               |  MS d3dx9_39.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_40`               |  MS d3dx9_40.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_41`               |  MS d3dx9_41.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_42`               |  MS d3dx9_42.dll (Microsoft, 2010) [downloadable]|
|`d3dx9_43`               |  MS d3dx9_43.dll (Microsoft, 2010) [downloadable]|
|`d3dxof`                 |  MS d3dxof.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]|
|`dbghelp`                |  MS dbghelp (Microsoft, 2008) [downloadable]|
|`devenum                  MS devenum.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dinput                   MS dinput.dll; breaks mouse, use only on Rayman 2 etc. (Microsoft, 2010) [downloadable]
|`dinput8                  MS DirectInput 8 from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dirac                    The Dirac directshow filter v1.0.2 (Dirac, 2009) [downloadable]
|`directmusic              MS DirectMusic from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`directplay               MS DirectPlay from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`directshow               DirectShow runtime DLLs (amstream, qasf, qcap, qdvd, qedit, quartz) (Microsoft, 2011) [downloadable]
|`directx9                 MS DirectX 9 (Deprecated, no-op) (Microsoft, 2010) [downloadable]
|`dmband                   MS dmband.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dmcompos                 MS dmcompos.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dmime                    MS dmime.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dmloader                 MS dmloader.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dmscript                 MS dmscript.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dmstyle                  MS dmstyle.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dmsynth                  MS dmsynth.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dmusic                   MS dmusic.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dmusic32                 MS dmusic32.dll from DirectX user redistributable (Microsoft, 2006) [downloadable]
|`dotnet11                 MS .NET 1.1 (Microsoft, 2003) [downloadable]
|`dotnet11sp1              MS .NET 1.1 SP1 (Microsoft, 2004) [downloadable]
|`dotnet20                 MS .NET 2.0 (Microsoft, 2006) [downloadable]
|`dotnet20sp1              MS .NET 2.0 SP1 (Microsoft, 2008) [downloadable]
|`dotnet20sp2              MS .NET 2.0 SP2 (Microsoft, 2009) [downloadable]
|`dotnet30                 MS .NET 3.0 (Microsoft, 2006) [downloadable]
|`dotnet30sp1              MS .NET 3.0 SP1 (Microsoft, 2007) [downloadable]
|`dotnet35                 MS .NET 3.5 (Microsoft, 2007) [downloadable]
|`dotnet35sp1              MS .NET 3.5 SP1 (Microsoft, 2008) [downloadable]
|`dotnet40                 MS .NET 4.0 (Microsoft, 2011) [downloadable]
|`dotnet40_kb2468871       MS .NET 4.0 KB2468871 (Microsoft, 2011) [downloadable]
|`dotnet45                 MS .NET 4.5 (Microsoft, 2012) [downloadable]
|`dotnet452                MS .NET 4.5.2 (Microsoft, 2012) [downloadable]
|`dotnet46                 MS .NET 4.6 (Microsoft, 2015) [downloadable]
|`dotnet461                MS .NET 4.6.1 (Microsoft, 2015) [downloadable]
|`dotnet462                MS .NET 4.6.2 (Microsoft, 2016) [downloadable]
|`dotnet471                MS .NET 4.7.1 (Microsoft, 2017) [downloadable]
|`dotnet472                MS .NET 4.7.2 (Microsoft, 2018) [downloadable]
|`dotnet48                 MS .NET 4.8 (Microsoft, 2019) [downloadable]
|`dotnet6                  MS .NET Runtime 6.0 LTS (Microsoft, 2023) [downloadable]
|`dotnet7                  MS .NET Runtime 7.0 LTS (Microsoft, 2023) [downloadable]
|`dotnet_verifier          MS .NET Verifier (Microsoft, 2016) [downloadable]
|`dotnetcore2              MS .NET Core Runtime 2.1 LTS (Microsoft, 2020) [downloadable]
|`dotnetcore3              MS .NET Core Runtime 3.1 LTS (Microsoft, 2020) [downloadable]
|`dotnetcoredesktop3       MS .NET Core Desktop Runtime 3.1 LTS (Microsoft, 2020) [downloadable]
|`dotnetdesktop6           MS .NET Desktop Runtime 6.0 LTS (Microsoft, 2023) [downloadable]
|`dotnetdesktop7           MS .NET Desktop Runtime 7.0 LTS (Microsoft, 2023) [downloadable]
|`dpvoice                  Microsoft dpvoice dpvvox dpvacm Audio dlls (Microsoft, 2002) [downloadable]
|`dsdmo                    MS dsdmo.dll (Microsoft, 2010) [downloadable]
|`dsound                   MS DirectSound from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dswave                   MS dswave.dll from DirectX user redistributable (Microsoft, 2010) [downloadable]
|`dx8vb                    MS dx8vb.dll from DirectX 8.1 runtime (Microsoft, 2001) [downloadable]
|`dxdiag                   DirectX Diagnostic Tool (Microsoft, 2010) [downloadable]
|`dxdiagn                  DirectX Diagnostic Library (Microsoft, 2011) [downloadable]
|`dxdiagn_feb2010          DirectX Diagnostic Library (February 2010) (Microsoft, 2010) [downloadable]
|`dxtrans                  MS dxtrans.dll (Microsoft, 2002) [downloadable]
|`dxvk                     Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (latest) (Philip Rebohle, 2023) [downloadable]
|`dxvk0054                 Vulkan-based D3D11 implementation for Linux / Wine (0.54) (Philip Rebohle, 2017) [downloadable]
|`dxvk0060                 Vulkan-based D3D11 implementation for Linux / Wine (0.60) (Philip Rebohle, 2017) [downloadable]
|`dxvk0061                 Vulkan-based D3D11 implementation for Linux / Wine (0.61) (Philip Rebohle, 2017) [downloadable]
|`dxvk0062                 Vulkan-based D3D11 implementation for Linux / Wine (0.62) (Philip Rebohle, 2017) [downloadable]
|`dxvk0063                 Vulkan-based D3D11 implementation for Linux / Wine (0.63) (Philip Rebohle, 2017) [downloadable]
|`dxvk0064                 Vulkan-based D3D11 implementation for Linux / Wine (0.64) (Philip Rebohle, 2017) [downloadable]
|`dxvk0065                 Vulkan-based D3D11 implementation for Linux / Wine (0.65) (Philip Rebohle, 2017) [downloadable]
|`dxvk0070                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.70) (Philip Rebohle, 2017) [downloadable]
|`dxvk0071                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.71) (Philip Rebohle, 2017) [downloadable]
|`dxvk0072                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.72) (Philip Rebohle, 2017) [downloadable]
|`dxvk0080                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.80) (Philip Rebohle, 2017) [downloadable]
|`dxvk0081                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.81) (Philip Rebohle, 2017) [downloadable]
|`dxvk0090                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.90) (Philip Rebohle, 2017) [downloadable]
|`dxvk0091                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.91) (Philip Rebohle, 2017) [downloadable]
|`dxvk0092                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.92) (Philip Rebohle, 2017) [downloadable]
|`dxvk0093                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.93) (Philip Rebohle, 2017) [downloadable]
|`dxvk0094                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.94) (Philip Rebohle, 2017) [downloadable]
|`dxvk0095                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.95) (Philip Rebohle, 2017) [downloadable]
|`dxvk0096                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (0.96) (Philip Rebohle, 2017) [downloadable]
|`dxvk1000                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.0) (Philip Rebohle, 2017) [downloadable]
|`dxvk1001                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.0.1) (Philip Rebohle, 2017) [downloadable]
|`dxvk1002                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.0.2) (Philip Rebohle, 2017) [downloadable]
dxvk1003                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.0.3) (Philip Rebohle, 2017) [downloadable]
dxvk1011                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.1.1) (Philip Rebohle, 2017) [downloadable]
dxvk1020                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.2) (Philip Rebohle, 2017) [downloadable]
dxvk1021                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.2.1) (Philip Rebohle, 2017) [downloadable]
dxvk1022                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.2.2) (Philip Rebohle, 2017) [downloadable]
dxvk1023                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.2.3) (Philip Rebohle, 2017) [downloadable]
dxvk1030                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.3) (Philip Rebohle, 2017) [downloadable]
dxvk1031                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.3.1) (Philip Rebohle, 2017) [downloadable]
dxvk1032                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.3.2) (Philip Rebohle, 2017) [downloadable]
dxvk1033                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.3.3) (Philip Rebohle, 2017) [downloadable]
dxvk1034                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.3.4) (Philip Rebohle, 2017) [downloadable]
dxvk1040                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.4) (Philip Rebohle, 2017) [downloadable]
dxvk1041                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.4.1) (Philip Rebohle, 2017) [downloadable]
dxvk1042                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.4.2) (Philip Rebohle, 2017) [downloadable]
dxvk1043                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.4.3) (Philip Rebohle, 2017) [downloadable]
dxvk1044                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.4.4) (Philip Rebohle, 2017) [downloadable]
dxvk1045                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.4.5) (Philip Rebohle, 2017) [downloadable]
dxvk1046                 Vulkan-based D3D10/D3D11 implementation for Linux / Wine (1.4.6) (Philip Rebohle, 2017) [downloadable]
dxvk1050                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.5) (Philip Rebohle, 2017) [downloadable]
dxvk1051                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.5.1) (Philip Rebohle, 2017) [downloadable]
dxvk1052                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.5.2) (Philip Rebohle, 2017) [downloadable]
dxvk1053                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.5.3) (Philip Rebohle, 2017) [downloadable]
dxvk1054                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.5.4) (Philip Rebohle, 2017) [downloadable]
dxvk1055                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.5.5) (Philip Rebohle, 2017) [downloadable]
dxvk1060                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.6) (Philip Rebohle, 2017) [downloadable]
dxvk1061                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.6.1) (Philip Rebohle, 2017) [downloadable]
dxvk1070                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.7) (Philip Rebohle, 2017) [downloadable]
dxvk1071                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.7.1) (Philip Rebohle, 2017) [downloadable]
dxvk1072                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.7.2) (Philip Rebohle, 2017) [downloadable]
dxvk1073                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.7.3) (Philip Rebohle, 2017) [downloadable]
dxvk1080                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.8) (Philip Rebohle, 2017) [downloadable]
dxvk1081                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.8.1) (Philip Rebohle, 2017) [downloadable]
dxvk1090                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.9) (Philip Rebohle, 2017) [downloadable]
dxvk1091                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.9.1) (Philip Rebohle, 2017) [downloadable]
dxvk1092                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.9.2) (Philip Rebohle, 2017) [downloadable]
dxvk1093                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.9.3) (Philip Rebohle, 2017) [downloadable]
dxvk1094                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.9.4) (Philip Rebohle, 2017) [downloadable]
dxvk1100                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.10) (Philip Rebohle, 2017) [downloadable]
dxvk1101                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.10.1) (Philip Rebohle, 2017) [downloadable]
dxvk1102                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.10.2) (Philip Rebohle, 2017) [downloadable]
dxvk1103                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (1.10.3) (Philip Rebohle, 2022) [downloadable]
dxvk2000                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (2.0) (Philip Rebohle, 2022) [downloadable]
dxvk2010                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (2.1) (Philip Rebohle, 2023) [downloadable]
dxvk2020                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (2.2) (Philip Rebohle, 2023) [downloadable]
dxvk2030                 Vulkan-based D3D9/D3D10/D3D11 implementation for Linux / Wine (2.3) (Philip Rebohle, 2023) [downloadable]
dxvk_nvapi0061           Alternative NVAPI Vulkan implementation on top of DXVK for Linux / Wine (0.6.1) (Jens Peters, 2023) [downloadable]
esent                    MS Extensible Storage Engine (Microsoft, 2011) [downloadable]
faudio                   FAudio (xaudio reimplementation, with xna support) builds for win32 (20.07) (Kron4ek, 2019) [downloadable]
faudio1901               FAudio (xaudio reimplementation, with xna support) builds for win32 (19.01) (Kron4ek, 2019) [downloadable]
faudio1902               FAudio (xaudio reimplementation, with xna support) builds for win32 (19.02) (Kron4ek, 2019) [downloadable]
faudio1903               FAudio (xaudio reimplementation, with xna support) builds for win32 (19.03) (Kron4ek, 2019) [downloadable]
faudio1904               FAudio (xaudio reimplementation, with xna support) builds for win32 (19.04) (Kron4ek, 2019) [downloadable]
faudio1905               FAudio (xaudio reimplementation, with xna support) builds for win32 (19.05) (Kron4ek, 2019) [downloadable]
faudio1906               FAudio (xaudio reimplementation, with xna support) builds for win32 (19.06) (Kron4ek, 2019) [downloadable]
faudio190607             FAudio (xaudio reimplementation, with xna support) builds for win32 (19.06.07) (Kron4ek, 2019) [downloadable]
ffdshow                  ffdshow video codecs (doom9 folks, 2010) [downloadable]
filever                  Microsoft's filever, for dumping file version info (Microsoft, 20??) [downloadable]
galliumnine              Gallium Nine Standalone (latest) (Gallium Nine Team, 2023) [downloadable]
galliumnine02            Gallium Nine Standalone (v0.2) (Gallium Nine Team, 2019) [downloadable]
galliumnine03            Gallium Nine Standalone (v0.3) (Gallium Nine Team, 2019) [downloadable]
galliumnine04            Gallium Nine Standalone (v0.4) (Gallium Nine Team, 2019) [downloadable]
galliumnine05            Gallium Nine Standalone (v0.5) (Gallium Nine Team, 2019) [downloadable]
galliumnine06            Gallium Nine Standalone (v0.6) (Gallium Nine Team, 2020) [downloadable]
galliumnine07            Gallium Nine Standalone (v0.7) (Gallium Nine Team, 2020) [downloadable]
galliumnine08            Gallium Nine Standalone (v0.8) (Gallium Nine Team, 2021) [downloadable]
galliumnine09            Gallium Nine Standalone (v0.9) (Gallium Nine Team, 2023) [downloadable]
gdiplus                  MS GDI+ (Microsoft, 2011) [downloadable]
gdiplus_winxp            MS GDI+ (Microsoft, 2009)
gfw                      MS Games For Windows Live (xlive.dll) (Microsoft, 2008) [downloadable]
glidewrapper             GlideWrapper (Rolf Neuberger, 2005) [downloadable]
glut                     The glut utility library for OpenGL (Mark J. Kilgard, 2001) [downloadable]
gmdls                    General MIDI DLS Collection (Microsoft / Roland, 1999) [downloadable]
hid                      MS hid (Microsoft, 2003) [downloadable]
icodecs                  Indeo codecs (Intel, 1998) [downloadable]
ie6                      Internet Explorer 6 (Microsoft, 2002) [downloadable]
ie7                      Internet Explorer 7 (Microsoft, 2008) [downloadable]
ie8                      Internet Explorer 8 (Microsoft, 2009) [downloadable]
ie8_kb2936068            Cumulative Security Update for Internet Explorer 8 (Microsoft, 2014) [downloadable]
ie8_tls12                TLS 1.1 and 1.2 for Internet Explorer 8 (Microsoft, 2017) [downloadable]
iertutil                 MS Runtime Utility (Microsoft, 2011) [downloadable]
itircl                   MS itircl.dll (Microsoft, 1999) [downloadable]
itss                     MS itss.dll (Microsoft, 1999) [downloadable]
jet40                    MS Jet 4.0 Service Pack 8 (Microsoft, 2003) [downloadable]
l3codecx                 MPEG Layer-3 Audio Codec for Microsoft DirectShow (Microsoft, 2010) [downloadable]
lavfilters               LAV Filters (Hendrik Leppkes, 2019) [downloadable]
lavfilters702            LAV Filters 0.70.2 (Hendrik Leppkes, 2017) [downloadable]
mdac27                   Microsoft Data Access Components 2.7 sp1 (Microsoft, 2006) [downloadable]
mdac28                   Microsoft Data Access Components 2.8 sp1 (Microsoft, 2005) [downloadable]
mdx                      Managed DirectX (Microsoft, 2006) [downloadable]
mf                       MS Media Foundation (Microsoft, 2011) [downloadable]
mfc100                   Visual C++ 2010 mfc100 library; part of vcrun2010 (Microsoft, 2010) [downloadable]
mfc110                   Visual C++ 2012 mfc110 library; part of vcrun2012 (Microsoft, 2012) [downloadable]
mfc120                   Visual C++ 2013 mfc120 library; part of vcrun2013 (Microsoft, 2013) [downloadable]
mfc140                   Visual C++ 2015 mfc140 library; part of vcrun2015 (Microsoft, 2015) [downloadable]
mfc40                    MS mfc40 (Microsoft Foundation Classes from win7sp1) (Microsoft, 1999) [downloadable]
mfc42                    Visual C++ 6 SP4 mfc42 library; part of vcrun6 (Microsoft, 2000) [downloadable]
mfc70                    Visual Studio (.NET) 2002 mfc70 library (Microsoft, 2006) [downloadable]
mfc71                    Visual C++ 2003 mfc71 library; part of vcrun2003 (Microsoft, 2003) [downloadable]
mfc80                    Visual C++ 2005 mfc80 library; part of vcrun2005 (Microsoft, 2011) [downloadable]
mfc90                    Visual C++ 2008 mfc90 library; part of vcrun2008 (Microsoft, 2011) [downloadable]
msaa                     MS Active Accessibility (oleacc.dll, oleaccrc.dll, msaatext.dll) (Microsoft, 2003) [downloadable]
msacm32                  MS ACM32 (Microsoft, 2003) [downloadable]
msasn1                   MS ASN1 (Microsoft, 2003) [downloadable]
msctf                    MS Text Service Module (Microsoft, 2003) [downloadable]
msdelta                  MSDelta differential compression library (Microsoft, 2011) [downloadable]
msdxmocx                 MS Windows Media Player 2 ActiveX control for VB6 (Microsoft, 1999) [downloadable]
msflxgrd                 MS FlexGrid Control (msflxgrd.ocx) (Microsoft, 2012) [downloadable]
msftedit                 Microsoft RichEdit Control (Microsoft, 2011) [downloadable]
mshflxgd                 MS Hierarchical FlexGrid Control (mshflxgd.ocx) (Microsoft, 2012) [downloadable]
msls31                   MS Line Services (Microsoft, 2001) [downloadable]
msmask                   MS Masked Edit Control (Microsoft, 2009) [downloadable]
mspatcha                 MS mspatcha (Microsoft, 2004) [downloadable]
msscript                 MS Windows Script Control (Microsoft, 2004) [downloadable]
msvcirt                  Visual C++ 6 SP4 msvcirt library; part of vcrun6 (Microsoft, 2000) [downloadable]
msvcrt40                 fixme (Microsoft, 2011) [downloadable]
msxml3                   MS XML Core Services 3.0 (Microsoft, 2005) [downloadable]
msxml4                   MS XML Core Services 4.0 (Microsoft, 2009) [downloadable]
msxml6                   MS XML Core Services 6.0 sp2 (Microsoft, 2014) [downloadable]
nuget                    NuGet Package manager (Outercurve Foundation, 2013) [downloadable]
ogg                      OpenCodecs 0.85: FLAC, Speex, Theora, Vorbis, WebM (Xiph.Org Foundation, 2011) [downloadable]
ole32                    MS ole32 Module (ole32.dll) (Microsoft, 2004) [downloadable]
oleaut32                 MS oleaut32.dll (Microsoft, 2011) [downloadable]
openal                   OpenAL Runtime (Creative, 2023) [downloadable]
pdh                      MS pdh.dll (Performance Data Helper) (Microsoft, 2011) [downloadable]
pdh_nt4                  MS pdh.dll (Performance Data Helper); WinNT 4.0 Version (Microsoft, 1997) [downloadable]
peverify                 MS peverify (from .NET 2.0 SDK) (Microsoft, 2006) [downloadable]
physx                    PhysX (Nvidia, 2021) [downloadable]
pngfilt                  pngfilt.dll (from winxp) (Microsoft, 2004) [downloadable]
prntvpt                  prntvpt.dll (Microsoft, 2011) [downloadable]
python26                 Python interpreter 2.6.2 (Python Software Foundaton, 2009) [downloadable]
python27                 Python interpreter 2.7.16 (Python Software Foundaton, 2019) [downloadable]
qasf                     qasf.dll (Microsoft, 2011) [downloadable]
qcap                     qcap.dll (Microsoft, 2011) [downloadable]
qdvd                     qdvd.dll (Microsoft, 2011) [downloadable]
qedit                    qedit.dll (Microsoft, 2011) [downloadable]
quartz                   quartz.dll (Microsoft, 2011) [downloadable]
quartz_feb2010           quartz.dll (February 2010) (Microsoft, 2010) [downloadable]
quicktime72              Apple QuickTime 7.2 (Apple, 2010) [downloadable]
quicktime76              Apple QuickTime 7.6 (Apple, 2010) [downloadable]
riched20                 MS RichEdit Control 2.0 (riched20.dll) (Microsoft, 2004) [downloadable]
riched30                 MS RichEdit Control 3.0 (riched20.dll, msls31.dll) (Microsoft, 2001) [downloadable]
richtx32                 MS Rich TextBox Control 6.0 (Microsoft, 2012) [downloadable]
sapi                     MS Speech API (Microsoft, 2011) [downloadable]
sdl                      Simple DirectMedia Layer (Sam Lantinga, 2012) [downloadable]
secur32                  MS Security Support Provider Interface (Microsoft, 2011) [downloadable]
setupapi                 MS Setup API (Microsoft, 2004) [downloadable]
shockwave                Shockwave (Adobe, 2018) [downloadable]
speechsdk                MS Speech SDK 5.1 (Microsoft, 2009) [downloadable]
tabctl32                 Microsoft Tabbed Dialog Control 6.0 (tabctl32.ocx) (Microsoft, 2012) [downloadable]
ucrtbase2019             Visual C++ 2019 library (ucrtbase.dll) (Microsoft, 2019) [downloadable]
uiribbon                 Windows UIRibbon (Microsoft, 2011) [downloadable]
updspapi                 Windows Update Service API (Microsoft, 2004) [downloadable]
urlmon                   MS urlmon (Microsoft, 2011) [downloadable]
usp10                    Uniscribe (Microsoft, 2011) [downloadable]
vb2run                   MS Visual Basic 2 runtime (Microsoft, 1993) [downloadable]
vb3run                   MS Visual Basic 3 runtime (Microsoft, 1998) [downloadable]
vb4run                   MS Visual Basic 4 runtime (Microsoft, 1998) [downloadable]
vb5run                   MS Visual Basic 5 runtime (Microsoft, 2001) [downloadable]
vb6run                   MS Visual Basic 6 runtime sp6 (Microsoft, 2004) [downloadable]
vcrun2003                Visual C++ 2003 libraries (mfc71,msvcp71,msvcr71) (Microsoft, 2003) [downloadable]
vcrun2005                Visual C++ 2005 libraries (mfc80,msvcp80,msvcr80) (Microsoft, 2011) [downloadable]
vcrun2008                Visual C++ 2008 libraries (mfc90,msvcp90,msvcr90) (Microsoft, 2011) [downloadable]
vcrun2010                Visual C++ 2010 libraries (mfc100,msvcp100,msvcr100) (Microsoft, 2010) [downloadable]
vcrun2012                Visual C++ 2012 libraries (atl110,mfc110,mfc110u,msvcp110,msvcr110,vcomp110) (Microsoft, 2012) [downloadable]
vcrun2013                Visual C++ 2013 libraries (mfc120,mfc120u,msvcp120,msvcr120,vcomp120) (Microsoft, 2013) [downloadable]
vcrun2015                Visual C++ 2015 libraries (concrt140.dll,mfc140.dll,mfc140u.dll,mfcm140.dll,mfcm140u.dll,msvcp140.dll,msvcp140_1.dll,msvcp140_atomic_wait.dll,vcamp140.dll,vccorlib140.dll,vcomp140.dll,vcruntime140.dll,vcruntime140_1.dll) (Microsoft, 2015) [downloadable]
vcrun2017                Visual C++ 2017 libraries (concrt140.dll,mfc140.dll,mfc140u.dll,mfcm140.dll,mfcm140u.dll,msvcp140.dll,msvcp140_1.dll,msvcp140_2.dll,msvcp140_atomic_wait.dll,vcamp140.dll,vccorlib140.dll,vcomp140.dll,vcruntime140.dll,vcruntime140_1.dll) (Microsoft, 2017) [downloadable]
vcrun2019                Visual C++ 2015-2019 libraries (concrt140.dll,mfc140.dll,mfc140u.dll,mfcm140.dll,mfcm140u.dll,msvcp140.dll,msvcp140_1.dll,msvcp140_2.dll,msvcp140_atomic_wait.dll,msvcp140_codecvt_ids.dll,vcamp140.dll,vccorlib140.dll,vcomp140.dll,vcruntime140.dll,vcruntime140_1.dll (Microsoft, 2019) [downloadable]
vcrun2022                Visual C++ 2015-2022 libraries (concrt140.dll,mfc140.dll,mfc140chs.dll,mfc140cht.dll,mfc140deu.dll,mfc140enu.dll,mfc140esn.dll,mfc140fra.dll,mfc140ita.dll,mfc140jpn.dll,mfc140kor.dll,mfc140rus.dll,mfc140u.dll,mfcm140.dll,mfcm140u.dll,msvcp140.dll,msvcp140_1.dll,msvcp140_2.dll,msvcp140_atomic_wait.dll,msvcp140_codecvt_ids.dll,vcamp140.dll,vccorlib140.dll,vcomp140.dll,vcruntime140.dll,vcruntime140_1.dll) (Microsoft, 2022) [downloadable]
vcrun6                   Visual C++ 6 SP4 libraries (mfc42, msvcp60, msvcirt) (Microsoft, 2000) [downloadable]
vcrun6sp6                Visual C++ 6 SP6 libraries (with fixes in ATL and MFC) (Microsoft, 2004) [downloadable]
vjrun20                  MS Visual J# 2.0 SE libraries (requires dotnet20) (Microsoft, 2007) [downloadable]
vkd3d                    Vulkan-based D3D12 implementation for Linux / Wine (latest) (Hans-Kristian Arntzen , 2020) [downloadable]
webio                    MS Windows Web I/O (Microsoft, 2011) [downloadable]
windowscodecs            MS Windows Imaging Component (Microsoft, 2006) [downloadable]
winhttp                  MS Windows HTTP Services (Microsoft, 2005) [downloadable]
wininet                  MS Windows Internet API (Microsoft, 2011) [downloadable]
wininet_win2k            MS Windows Internet API (Microsoft, 2008) [downloadable]
wmi                      Windows Management Instrumentation (aka WBEM) Core 1.5 (Microsoft, 2000) [downloadable]
wmp10                    Windows Media Player 10 (Microsoft, 2006) [downloadable]
wmp11                    Windows Media Player 11 (Microsoft, 2007) [downloadable]
wmp9                     Windows Media Player 9 (Microsoft, 2003) [downloadable]
wmv9vcm                  MS Windows Media Video 9 Video Compression Manager (Microsoft, 2013) [downloadable]
wsh57                    MS Windows Script Host 5.7 (Microsoft, 2007) [downloadable]
xact                     MS XACT Engine (32-bit only) (Microsoft, 2010) [downloadable]
xact_x64                 MS XACT Engine (64-bit only) (Microsoft, 2010) [downloadable]
xinput                   Microsoft XInput (Xbox controller support) (Microsoft, 2010) [downloadable]
xmllite                  MS xmllite dll (Microsoft, 2011) [downloadable]
xna31                    MS XNA Framework Redistributable 3.1 (Microsoft, 2009) [downloadable]
xna40                    MS XNA Framework Redistributable 4.0 (Microsoft, 2010) [downloadable]
xvid                     Xvid Video Codec (xvid.org, 2019) [downloadable]

### Fonts
allfonts                 All fonts (various, 1998-2010) [downloadable]
andale                   MS Andale Mono font (Microsoft, 2008) [downloadable]
arial                    MS Arial / Arial Black fonts (Microsoft, 2008) [downloadable]
baekmuk                  Baekmuk Korean fonts (Wooderart Inc. / kldp.net, 1999) [downloadable]
calibri                  MS Calibri font (Microsoft, 2007) [downloadable]
cambria                  MS Cambria font (Microsoft, 2009) [downloadable]
candara                  MS Candara font (Microsoft, 2009) [downloadable]
cjkfonts                 All Chinese, Japanese, Korean fonts and aliases (Various, ) [downloadable]
comicsans                MS Comic Sans fonts (Microsoft, 2008) [downloadable]
consolas                 MS Consolas console font (Microsoft, 2011) [downloadable]
constantia               MS Constantia font (Microsoft, 2009) [downloadable]
corbel                   MS Corbel font (Microsoft, 2009) [downloadable]
corefonts                MS Arial, Courier, Times fonts (Microsoft, 2008) [downloadable]
courier                  MS Courier fonts (Microsoft, 2008) [downloadable]
droid                    Droid fonts (Ascender Corporation, 2009) [downloadable]
eufonts                  Updated fonts for Romanian and Bulgarian (Microsoft, 2008) [downloadable]
fakechinese              Creates aliases for Chinese fonts using Source Han Sans fonts (Adobe, 2019)
fakejapanese             Creates aliases for Japanese fonts using Source Han Sans fonts (Adobe, 2019)
fakejapanese_ipamona     Creates aliases for Japanese fonts using IPAMona fonts (Jun Kobayashi, 2008)
fakejapanese_vlgothic    Creates aliases for Japanese Meiryo fonts using VLGothic fonts (Project Vine / Daisuke Suzuki, 2014)
fakekorean               Creates aliases for Korean fonts using Source Han Sans fonts (Adobe, 2019)
georgia                  MS Georgia fonts (Microsoft, 2008) [downloadable]
impact                   MS Impact fonts (Microsoft, 2008) [downloadable]
ipamona                  IPAMona Japanese fonts (Jun Kobayashi, 2008) [downloadable]
liberation               Red Hat Liberation fonts (Mono, Sans, SansNarrow, Serif) (Red Hat, 2008) [downloadable]
lucida                   MS Lucida Console font (Microsoft, 1998) [downloadable]
meiryo                   MS Meiryo font (Microsoft, 2009) [downloadable]
opensymbol               OpenSymbol fonts (replacement for Wingdings) (libreoffice.org, 2022) [downloadable]
pptfonts                 All MS PowerPoint Viewer fonts (various, ) [downloadable]
sourcehansans            Source Han Sans fonts (Adobe, 2021) [downloadable]
tahoma                   MS Tahoma font (not part of corefonts) (Microsoft, 1999) [downloadable]
takao                    Takao Japanese fonts (Jun Kobayashi, 2010) [downloadable]
times                    MS Times fonts (Microsoft, 2008) [downloadable]
trebuchet                MS Trebuchet fonts (Microsoft, 2008) [downloadable]
uff                      Ubuntu Font Family (Ubuntu, 2010) [downloadable]
unifont                  Unifont alternative to Arial Unicode MS (Roman Czyborra / GNU, 2021) [downloadable]
verdana                  MS Verdana fonts (Microsoft, 2008) [downloadable]
vlgothic                 VLGothic Japanese fonts (Project Vine / Daisuke Suzuki, 2014) [downloadable]
webdings                 MS Webdings fonts (Microsoft, 2008) [downloadable]
wenquanyi                WenQuanYi CJK font (wenq.org, 2009) [downloadable]
wenquanyizenhei          WenQuanYi ZenHei font (wenq.org, 2009) [downloadable]

### Prefix
apps
benchmarks
dlls
fonts
settings

### Settings
alldlls=builtin          Override most common DLLs to builtin
alldlls=default          Remove all DLL overrides
autostart_winedbg=disabled Prevent winedbg from launching when an unhandled exception occurs
autostart_winedbg=enabled Automatically launch winedbg when an unhandled exception occurs (default)
bad                      Fake verb that always returns false
cfc=disabled             Disable CheckFloatConstants (default)
cfc=enabled              Enable CheckFloatConstants
csmt=force               Enable and force serialisation of OpenGL or Vulkan commands between multiple command streams in the same application
csmt=off                 Disable Command Stream Multithreading
csmt=on                  Enable Command Stream Multithreading (default)
fontfix                  Check for broken fonts
fontsmooth=bgr           Enable subpixel font smoothing for BGR LCDs
fontsmooth=disable       Disable font smoothing
fontsmooth=gray          Enable subpixel font smoothing
fontsmooth=rgb           Enable subpixel font smoothing for RGB LCDs
forcemono                Force using Mono instead of .NET (for debugging)
good                     Fake verb that always returns true
grabfullscreen=n         Disable cursor clipping for full-screen windows (default)
grabfullscreen=y         Force cursor clipping for full-screen windows (needed by some games)
gsm=0                    Set MaxShaderModelGS to 0
gsm=1                    Set MaxShaderModelGS to 1
gsm=2                    Set MaxShaderModelGS to 2
gsm=3                    Set MaxShaderModelGS to 3
heapcheck                Enable heap checking with GlobalFlag
hidewineexports=disable  Disable hiding Wine exports from applications (wine-staging)
hidewineexports=enable   Enable hiding Wine exports from applications (wine-staging)
hosts                    Add empty C:\windows\system32\drivers\etc\{hosts,services} files
isolate_home             Remove wineprefix links to /home/austin
macdriver=mac            Enable the Mac native Quartz driver (default)
macdriver=x11            Disable the Mac native Quartz driver, use X11 instead
mackeyremap=both         Enable mapping opt->alt and cmd->ctrl keys for the Mac native driver
mackeyremap=left         Enable mapping of left opt->alt and cmd->ctrl keys for the Mac native driver
mackeyremap=none         Do not remap keys for the Mac native driver (default)
mimeassoc=off            Disable exporting MIME-type file associations to the native desktop
mimeassoc=on             Enable exporting MIME-type file associations to the native desktop (default)
mwo=disable              Set DirectInput MouseWarpOverride to disable
mwo=enabled              Set DirectInput MouseWarpOverride to enabled (default)
mwo=force                Set DirectInput MouseWarpOverride to force (needed by some games)
native_mdac              Override odbc32, odbccp32 and oledb32
native_oleaut32          Override oleaut32
nocrashdialog            Disable crash dialog
npm=repack               Set NonPower2Mode to repack
nt351                    Set Windows version to Windows NT 3.51
nt40                     Set Windows version to Windows NT 4.0
orm=backbuffer           Set OffscreenRenderingMode=backbuffer
orm=fbo                  Set OffscreenRenderingMode=fbo (default)
psm=0                    Set MaxShaderModelPS to 0
psm=1                    Set MaxShaderModelPS to 1
psm=2                    Set MaxShaderModelPS to 2
psm=3                    Set MaxShaderModelPS to 3
remove_mono              Remove builtin wine-mono
renderer=gdi             Set renderer to gdi
renderer=gl              Set renderer to gl
`renderer=no3d            Set renderer to no3d
`renderer=vulkan          Set renderer to vulkan
`rtlm=auto                Set RenderTargetLockMode to auto (default)
`rtlm=disabled            Set RenderTargetLockMode to disabled
`rtlm=readdraw            Set RenderTargetLockMode to readdraw
`rtlm=readtex             Set RenderTargetLockMode to readtex
`rtlm=texdraw             Set RenderTargetLockMode to texdraw
`rtlm=textex              Set RenderTargetLockMode to textex
`sandbox`                  Sandbox the wineprefix - remove links to /home/austin
`set_mididevice`           Set MIDImap device to the value specified in the MIDI_DEVICE environment variable
`set_userpath`             set user PATH variable in wine prefix specified by native and/or wine paths in WINEPATH environment variable with ';' as path separator
`shader_backend=arb`       Set shader_backend to arb
`shader_backend=glsl`      Set shader_backend to glsl
`shader_backend=none`      Set shader_backend to none
`sound=alsa`               Set sound driver to ALSA
`sound=coreaudio`          Set sound driver to Mac CoreAudio
`sound=disabled           Set sound driver to disabled
`sound=oss                Set sound driver to OSS
`sound=pulse              Set sound driver to PulseAudio
`ssm=disabled             Disable Struct Shader Math (default)
`ssm=enabled              Enable Struct Shader Math
`usetakefocus=n           Disable UseTakeFocus (default)
`usetakefocus=y           Enable UseTakeFocus
`vd=1024x768              Enable virtual desktop, set size to 1024x768
`vd=1280x1024             Enable virtual desktop, set size to 1280x1024
`vd=1440x900              Enable virtual desktop, set size to 1440x900
`vd=640x480               Enable virtual desktop, set size to 640x480
`vd=800x600               Enable virtual desktop, set size to 800x600
`vd=off                   Disable virtual desktop
`videomemorysize=1024     Tell Wine your video card has 1024MB RAM
`videomemorysize=2048     Tell Wine your video card has 2048MB RAM
`videomemorysize=512      Tell Wine your video card has 512MB RAM
`videomemorysize=default`  Let Wine detect amount of video card memory
`vista`                    Set Windows version to Windows Vista
`vsm=0`                    Set MaxShaderModelVS to 0
`vsm=1`                    Set MaxShaderModelVS to 1
`vsm=2`                    Set MaxShaderModelVS to 2
`vsm=3`                    Set MaxShaderModelVS to 3
`win10`                    Set Windows version to Windows 10
`win11`                    Set Windows version to Windows 11
`win20`                    Set Windows version to Windows 2.0
`win2k`                    Set Windows version to Windows 2000
`win2k3`                   Set Windows version to Windows 2003
`win2k8`                   Set Windows version to Windows 2008
`win2k8r2`                 Set Windows version to Windows 2008 R2
`win30`                    Set Windows version to Windows 3.0
`win31`                    Set Windows version to Windows 3.1
`win7`                     Set Windows version to Windows 7
`win8`                     Set Windows version to Windows 8
`win81`                    Set Windows version to Windows 8.1
`win95`                    Set Windows version to Windows 95
`win98`                    Set Windows version to Windows 98
`windowmanagerdecorated=n` Prevent the window manager from decorating windows
`windowmanagerdecorated=y` Allow the window manager to decorate windows (default)
`windowmanagermanaged=n`   Prevent the window manager from controlling windows
`windowmanagermanaged=y`   Allow the window manager to control windows (default)
`winme`                    Set Windows version to Windows ME
`winver=`                  Set Windows version to default (win7)
`winxp`                    Set Windows version to Windows XP