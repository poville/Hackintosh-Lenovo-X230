# Hackintosh-Lenovo-X230
Hackintosh-Lenovo-X230

#### Notice: I am not responsible for any damages you may cause.

<details>
<summary><strong> SUMMARY </strong></summary>
<br>

| MacOS          | OpenCore | Repo                                                                                     |
| ---------------| -------- | ---------------------------------------------------------------------------------------- |
| Monterey 12.7  | 0.9.5    | <a href="https://github.com/poville/Hackintosh-Lenovo-X230/tree/OC095Mac12.7">Here       |
| Sonoma 14.0    | 0.9.5    | <a href="https://github.com/poville/Hackintosh-Lenovo-X230/tree/OC095Mac14.0">Here       |
| Sonoma 14.4    | 0.9.9    | <a href="https://github.com/poville/Hackintosh-Lenovo-X230/tree/OC099Mac14.4">Here       |
| Sequoia 15.0.1 | 1.0.2    | <a href="https://github.com/poville/Hackintosh-Lenovo-X230/tree/OC102Mac15.0.1">Here     |

</details>


<details>
<summary><strong> HARDWARE </strong></summary>
<br>

| Category  | THINKPAD X230            |
| --------- | ------------------------ |
| Board     | Lenovo 2306CTO           |
| CPU       | Intel Core i5-3210M      |
| SSD       | Toshiba TR 200(400GB)    |
| Graphics  | Intel GMA HD 4000        |
| Display   | LEN40E2(12.5'1366x768)   |
| Network   | Intel 82579LM            |
| WiFi      | Intel Wireless-N 2200    |
| BlueTooth | Broadcom 20702a1         |
| Audio     | Realtek ALC269           |


- Refer to [X230-Platform_Specifications](https://psref.lenovo.com/syspool/Sys/PDF/withdrawnbook/ThinkPad_X230.pdf) for possible stock ThinkPad X230 configurations.

</details>

<details>
<summary><strong> Tips </strong></summary>

1. How to decide audio layout-id  
    - In AppleALC.kext\Contents\ , we will find a file named 'Info.plist'
    - In 'Info.plist', find key word 'ALC269','Thinkpad' and 'X230', we will find some descriptions like this:
        ```
                <dict>
                    <key>AFGLowPowerState</key>
                    <data>
                    AwAAAA==
                    </data>
                    <key>Codec</key>
                    <string>Hypereitan - ALC269VC for Thinkpad X230 i7</string>
                    <key>CodecID</key>
                    <integer>283902569</integer>
                    <key>ConfigData</key>
                    <data>
                    ASccEAEnHQEBJx6gAScfkAFHHEABRx0BAUce
                    EAFHH5ABVxxQAVcdEAFXHiEBVx8BAYcccAGH
                    HRABhx6hAYcfAQFHDAI=
                    </data>
                    <key>FuncGroup</key>
                    <integer>1</integer>
                    <key>LayoutID</key>
                    <integer>18</integer>
                    <key>WakeConfigData</key>
                    <data>
                    AUcMAg==
                    </data>
                    <key>WakeVerbReinit</key>
                    <true/>
                </dict>
        ```
    - Focus on the keyword 'LayoutID', the value is '18', this is the audio layout-id.
2. How to patch HD4000

    2-ways:
    - <a href="https://github.com/dortania/OpenCore-Legacy-Patcher">OpenCore-Legacy-Patcher
    - <a href="https://github.com/chris1111/Patch-HD4000-Monterey/">Patch-HD4000-Monterey

<br>