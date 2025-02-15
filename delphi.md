<!-- # [ zrfisaac ] -->

<!-- # [ about ] -->
<!-- # - author : Isaac Caires -->
<!-- # . - email : zrfisaac@gmail.com -->
<!-- # . - site : zrfisaac.github.io -->
<!-- # - version : zrfisaac.wiki.en.delphi : 0.0.1 -->

<!-- # [ markdown ] -->

<!-- # - : http://blong.com/Conferences/DCon2001/Debugging/Debugging.htm -->

<!-- # [ markdown ] -->
# Delphi

## Description
Delphi is a high-level, object-oriented programming language and an integrated development environment (IDE) for rapid application development (RAD). Originally developed by Borland and now maintained by Embarcadero, Delphi is primarily used for creating Windows, macOS, iOS, Android, and Linux applications. It is based on Object Pascal and features a powerful visual component framework (VCL and FireMonkey) that allows developers to build applications with a rich graphical user interface. Delphi is known for its strong database support, performance, and ease of use, making it popular for enterprise and business applications.

---

## Index
- [Debug](#debug)
  - [CPU](#cpu)
    - [CPU Registers](#cpu-registers)
    - [CPU Flags](#cpu-flags)
    - [CPU Assembly Instructions](#cpu-assembly-instructions)
- Download
  - CodeGear :
    [`2007`](https://altd.codegear.com/download/radstudio2007/CodeGearRADStudio2007_Dec2007.iso)
  - Embarcadero :
    [`12.2 Athens`](https://altd.embarcadero.com/download/radstudio/12.0/RADStudio_12_2_i_0329_C2CC.iso)
    [`11.3 Alexandria`](https://altd.embarcadero.com/download/radstudio/11.0/RADStudio_11_3_61_3236a.iso)
    [`10.4.2 Sydney`](https://altd.embarcadero.com/download/radstudio/10.4/RADStudio-1042-4203.iso)
    [`10.3.3 Rio`](https://altd.embarcadero.com/download/radstudio/10.3/delphicbuilder10_3_3_7899_nt.iso)
    [`10.2.3 Tokyo`](https://altd.embarcadero.com/download/radstudio/10.2/delphicbuilder10_2_3_2631.iso)
    [`10.1 Berlin`](https://altd.embarcadero.com/download/radstudio/10.1/delphicbuilder10_1_upd1.iso)
    [`10 Seattle`](https://altd.embarcadero.com/download/radstudio/10/delphicbuilder10___upd1.iso)
    [`XE8`](http://altd.embarcadero.com/download/radstudio/xe8/delphicbuilder_xe8_upd1_subscription.iso)
    [`XE7`](https://altd.embarcadero.com/download/radstudio/xe7/delphicbuilder_xe7_upd1_win.iso)
    [`XE6`](https://altd.embarcadero.com/download/radstudio/xe6/delphicbuilder_xe6_upd1_win.iso)
    [`XE5`](https://altd.embarcadero.com/download/radstudio/xe5/delphicbuilder_xe5_upd2_win.iso)
    [`XE4`](https://altd.embarcadero.com/download/radstudio/xe4/delphicbuilder_xe4_upd1_win.iso)
    [`XE2`](https://altd.embarcadero.com/download/radstudio/xe2/delphicbuilder_xe2_4429_win_dl.iso)
    [`XE`](https://altd.embarcadero.com/download/RADStudioXE/delphicbuilder_xe_3953B_win.iso)
    [`2010`](https://altd.embarcadero.com/download/RADStudio2010/delphicbuilder_2010_3615_win.iso)
    [`2009`](https://altd.embarcadero.com/download/Delphi_C++Builder2009/Delphi_C++Builder2009_ISO_June2009.iso)
    [`7`](https://altd.embarcadero.com/download/delphi/d7/english/ent/delphi_7_ent_en.iso)
  - WinWorld :
    [`7`](https://winworldpc.com/product/delphi/70)
    [`6`](https://winworldpc.com/product/delphi/60)
    [`4`](https://winworldpc.com/product/delphi/4x)
    [`3`](https://winworldpc.com/product/delphi/3x)
    [`2`](https://winworldpc.com/product/delphi/2x)
    [`1`](https://winworldpc.com/product/delphi/1x)
- [Version](#version)

---

## [Debug](#index)

### [CPU](#index)

#### [CPU Registers](#index)

| Register | Register name | Size | Comments |
|---|---|---|---|
| EAX | Extended accumulator | 32 bits | General purpose register |
| EBX | Extended base | 32 bits | General purpose register |
| ECX | Extended count | 32 bits | General purpose register |
| EDX | Extended data | 32 bits | General purpose register |
| ESI | Extended source indicator | 32 bits | General purpose register |
| EDI | Extended destination indicator | 32 bits | General purpose register |
| EBP | Extended base pointer | 32 bits | General purpose register |
| ESP | Extended stack pointer | 32 bits | General purpose register |
| EIP | Extended instruction pointer | 32 bits | Status/control register |
| EFL | Extended flags | 32 bits | Status/control register |
| CS | Code segment | 16 bits | To hold a segment selector |
| DS | Data segment | 16 bits | To hold a segment selector |
| SS | Stack segment | 16 bits | To hold a segment selector |
| ES | Extra segment | 16 bits | To hold a segment selector |
| FS | Another extra segment | 16 bits | To hold a segment selector |
| GS | Another extra segment | 16 bits | To hold a segment selector |
| AX | Accumulator | 16 bits | Low word of EAX |
| AH | Accumulator high | 8 bits | High byte of AX |
| AL | Accumulator low | 8 bits | Low byte of AX |
| BX | Base | 16 bits | Low word of EBX |
| BH | Base high | 8 bits | High byte of BX |
| BL | Base low | 8 bits | Low byte of BX |
| CX | Count | 16 bits | Low word of ECX |
| CH | Count high | 8 bits | High byte if CX |
| CL | Count low | 8 bits | Low byte of CX |
| DX | Data | 16 bits | Low word of EDX |
| DH | Data high | 8 bits | High byte of DX |
| DL | Data low | 8 bits | Low byte of DX |

#### [CPU Flags](#index)

| Value | EFL register bit(s) | Flag/bit name | Flag type |
|---|---|---|---|
| CF | 0 | Carry flag | Status |
| PF | 2 | Parity flag | Status |
| AF | 4 | Adjust flag | Status |
| ZF | 6 | Zero flag | Status |
| SF | 7 | Sign flag | Status |
| TF | 8 | Trap flag | System |
| IF | 9 | Interrupt flag | System |
| DF | 10 | Direction flag | Control |
| OF | 11 | Overflow flag | Status |
| IO | 12 and 13 | I/O privilege level field | System |
| NF | 14 | Nested task flag | System |
| RF | 16 | Resume flag | System |
| VM | 17 | Virtual 8086 mode flag | System |
| AC | 18 | Alignment check flag | System |
| VF | 19 | Virtual interrupt flag | System |
| VP | 20 | Virtual interrupt pending flag | System |
| ID | 21 | Identification flag | System |

#### [CPU Assembly Instructions](#index)

| Assembly instruction | Meaning |
|---|---|
| `mov eax, 1` | Set EAX to 1 |
| `xor eax, eax` | Same as `mov eax, 0` but more efficient |
| `mov eax, esi` | Copy ESI value to EAX |
| `mov edx, [eax]` | Move DWord pointed to by EAX into EDX |
| `mov dl, $01` | Set low byte of EDX to 1, leaving other bytes unchanged |
| `push eax` | Push EAX onto the stack, so EAX can be re-used |
| `pop eax` | Pop value off stack and store it in EAX |
| `ret` | Return from routine (return address is on stack) |
| `call $410123` | Push address of next instruction on stack and jump to address $410123 |
| `mov ebx, [ebp-$5]` | Move the DWord starting at the address 5 less than that stored in EBP into EBX |
| `cmp dword ptr [ebx+$3C], $00` | Compare the DWord at the address $3C bytes after the address stored in EBX with zero |
| `jz SomeRoutine+$A0` | If the last compare operation suggested the two values are equal, jump to $A0 bytes after the first byte of the SomeRoutine routine. Compare operations are implemented as subtractions. JZ is a contraction of **J**ump if **Z**ero. |
| `movsb` | Copy byte pointed to by ESI to the address pointed to by EDI, then increments ESI and EDI by 1 (unless direction flag is set, where they are decremented) |
| `movsw` | Copy word pointed to by ESI to the address pointed to by EDI, then increments ESI and EDI by 2 (unless direction flag is set, where they are decremented) |
| `add esp, -$08` | Subtract 8 from stack pointer |

## [Version](#index)
| **Product**                | **Product version** | **Other names** | **Internal version** | **Package version** | **CompilerVersion const** | **RTLVersion const** | **Defined Symbol**  |
|----------------------------|---------------------|-----------------|----------------------|---------------------|---------------------------|----------------------|---------------------|
| **Delphi 12 Athens**       | 29                  | BDS 23          | 36                   | 290                 | 36.0                      | 36.0                 | VER360              |
| **Delphi 11 Alexandria**   | 28                  | BDS 22          | 35                   | 280                 | 35.0                      | 35.0                 | VER350              |
| **Delphi 10.4 Sydney**     | 27                  | BDS 21          | 34                   | 270                 | 34.0                      | 34.0                 | VER340              |
| **Delphi 10.3 Rio**        | 26                  | BDS 20          | 33                   | 260                 | 33.0                      | 33.0                 | VER330              |
| **Delphi 10.2 Tokyo**      | 25                  | BDS 19          | 32                   | 250                 | 32.0                      | 32.0                 | VER320              |
| **Delphi 10.1 Berlin**     | 24                  | BDS 18          | 31                   | 240                 | 31.0                      | 31.0                 | VER310              |
| **Delphi 10 Seattle**      | 23                  | BDS 17          | 30                   | 230                 | 30.0                      | 30.0                 | VER300              |
| **Delphi XE8**             | 22                  | BDS 16          | 29                   | 220                 | 29.0                      | 29.0                 | VER290              |
| **Delphi XE7**             | 21                  | BDS 15          | 28                   | 210                 | 28.0                      | 28.0                 | VER280              |
| **Delphi XE6**             | 20                  | BDS 14          | 27                   | 200                 | 27.0                      | 27.0                 | VER270              |
| **Delphi XE5**             | 19                  | BDS 12          | 26                   | 190                 | 26.0                      | 26.0                 | VER260              |
| **Delphi XE4**             | 18                  | BDS 11          | 25                   | 180                 | 25.0                      | 25.0                 | VER250              |
| **Delphi XE3**             | 17                  | BDS 10          | 24                   | 170                 | 24.0                      | 24.0                 | VER240              |
| **Delphi XE2**             | 16                  | BDS 9           | 23                   | 160 & 161†          | 23.0                      | 23.0                 | VER230              |
| **Delphi XE**              | 15                  | BDS 8           | 22                   | 150                 | 22.0                      | 22.0                 | VER220              |
| **Delphi 2010**            | 14                  | BDS 7           | 21                   | 140                 | 21.0                      | 21.0                 | VER210              |
| **Delphi 2009**            | 12                  | BDS 6           | 20                   | 120                 | 20.0                      | 20.0                 | VER200              |
| **Delphi 2007 .NET**       | 11                  | BDS 5           | 19                   | 110                 | 19.0                      | 19.0                 | VER190              |
| **Delphi 2007 Win32**      | 11                  | BDS 5           | 18.5                 | 110                 | 18.5                      | 18.0                 | VER180 & VER185     |
| **Delphi 2006**            | 10                  | BDS 4           | 18                   | 100                 | 18.0                      | 18.0                 | VER180              |
| **Delphi 2005**            | 9                   | BDS 3           | 17                   | 90                  | 17.0                      | 17.0                 | VER170              |
| **Delphi 8 (.NET only)**   | 8                   | BDS 2           | 16                   | 80                  | 16.0                      | 16.0                 | VER160              |
| **C++ Builder 7**          | 7?                  |                 | 15                   | 70?                 | 15.0?                     | ?                    | VER150 & BCB        |
| **Delphi 7**               | 7                   |                 | 15                   | 70                  | 15.0                      | 15.0                 | VER150              |
| **C++ Builder 6**          | 6                   |                 | 14                   | 60                  | 14.0                      | ?                    | VER140 & BCB        |
| **Delphi 6**               | 6                   |                 | 14                   | 60                  | 14.0                      | 14.0                 | VER140              |
| **C++ Builder 5**          | 5                   |                 | 13                   | 50                  | 13.0                      | ?                    | VER130 & BCB        |
| **Delphi 5**               | 5                   |                 | 13                   | 50                  | 13.0                      | 13.0                 | VER130              |
| **C++ Builder 4**          | 4                   |                 | 12                   | 40                  | 12.0                      | ?                    | VER120 & BCB        |
| **Delphi 4**               | 4                   |                 | 12                   | 40                  | 12.0                      | 12.0                 | VER120              |
| **C++ Builder 3**          | 3                   |                 | 11                   | 30                  | 11.0                      | ?                    | VER110 & BCB        |
| **Delphi 3**               | 3                   |                 | 11                   | 30                  | 11.0                      | 11.0                 | VER110              |
| **C++ Builder 1**          | 1                   |                 | 10.5                 | 10                  | 10.0                      | ?                    | VER100 & BCB        |
| **Delphi 2**               | 2                   |                 | 10                   | 20                  | 10.0                      | 10.0                 | VER100              |
| **Delphi 1**               | 1                   |                 | 8                    | 10                  | 8.0                       | 8.0                  | VER80               |
