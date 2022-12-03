<p align="center"><img src="https://portswigger.net/burp/communitydownload/images/burp-pro-logo.svg" alt="Burp Suite Professional logo" width="360" height="260"></p>

<h1 align="center">Welcome to Burp Suite loader👋</h1>

<div align="center">
  <!-- Platform -->
  <a href="Platform">
    <img src="https://img.shields.io/badge/Platform-Windows%E3%80%81Linux%E3%80%81macOS-green?color=gerrn&style=flat-square" alt="Platform">
  </a>
  <!-- License -->
  <a href="LICENSE">
    <img src="https://img.shields.io/github/license/x-Ai/BurpSuite?color=gerrn&style=flat-square" alt="LICENSE">
  </a>
  <!-- ❤︎ -->
  <a href="❤︎">
    <img src="https://img.shields.io/badge/❤︎-致敬永远好奇的心-green?color=gerrn&style=flat-square" alt="❤︎">
  </a>
</div>
<br>
<div align="center">
  😈插播一条避坑指南：杭州<亚信安全>天坑，各位注意😈<br><br>
  ⚡️Burp Suite Professional 2022.9 Loader已由<a href="https://github.com/Hywell">Hywell</a>更新，祝玩的愉快...⚡️<br><br>
  商业使用请购买正版软件 - https://portswigger.net/buy/pro<br>
  ！<a href="https://github.com/x-Ai/BurpSuiteLoader">旧项目</a>已被PortSwigger投诉导致DMCA ！*未混淆，请自行围观jar包*
</div>

#### **<p align="center">✨如果本项目对您有帮助，点一下Star吧🥰✨</p>**


<h1 align="center"></h1>
<br><p align="center">时隔两年再次建立此项目是因为看到了SCZ师傅的<a href="https://mp.weixin.qq.com/s/4KXxKdnPeWqsEsylObhg8w">公众号文章</a>，想了想还是写一篇更加详细的文档来帮助需要的同学</p>
<br><p align="center">2022.09.13：偷懒没有从新跟流程，直接使用了SCZ师傅的修改正则范围<a href="https://mp.weixin.qq.com/s/y4NOtfKx90zCJsedBlD8-g">(文章地址)</a>，再次感谢前辈🤝。</p>
<h1 align="center"></h1>


### BurpSuitePro 下载地址

&ensp;&ensp;&ensp;&ensp;https://portswigger.net/burp/releases

### Loader

&ensp;&ensp;&ensp;&ensp;<a href="https://raw.githubusercontent.com/x-Ai/BurpSuite/main/BurpSuiteLoader.jar">BurpSuiteLoader.jar(166KB)</a>
- SHA256: B4DFB539F8A37E0D08F47ED5222D6067C9234A4D558A0E37EF07D3ECBB0B9EC9
- MD5: 2E5AF5B059E848FFCB64EDD18CB33B0C
### Keygen

&ensp;&ensp;&ensp;&ensp;<a href="https://raw.githubusercontent.com/x-Ai/BurpSuite/main/burp-keygen-scz.jar">burp-keygen-scz.jar(48KB)</a>
- SHA256: 74893842A782238F52F0F225C06FA744568321911FEA077BC290BD9914B73402
- MD5: E646B3EEF03EFBA637E6ED794CED4114

### Windows 启动器源码
&ensp;&ensp;&ensp;&ensp;<a href="https://raw.githubusercontent.com/x-Ai/BurpSuite/main/BurpSuiteLoadSources.zip">BurpSuiteLoadSources.zip(14KB)</a>
- SHA256: F38DF9B30E4A310073A8713372A512A20372F236809B9FDD8B18983FD64E3E1F
- MD5: 2AA4B21E470206A625669C9241EBE96D

## 🚀 使用方式

<div align="center">
  <sub>！强烈建议下载安装包进行安装后使用 ！</sub>
</div>

### 命令行
> java --illegal-access=permit -noverify -Dsun.java2d.d3d=false -Dsun.java2d.noddraw=true --add-opens=java.desktop/javax.swing=ALL-UNNAMED --add-opens=java.base/java.lang=ALL-UNNAMED --add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED --add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED --add-opens=java.base/jdk.internal.org.objectweb.asm.Opcodes=ALL-UNNAMED -javaagent:BurpSuiteLoader.jar  -jar burpsuite_pro.jar
### Windows
1. 下载：https://portswigger-cdn.net/burp/releases/download?product=pro&version=2022.3.1&type=WindowsX64
2. 放置进安装目录

<p align="center"><img src="/static/Launch.png" alt="Burp启动器"></p>
&ensp;&ensp;&ensp;&ensp;<a href="https://raw.githubusercontent.com/x-Ai/BurpSuite/main/BurpSuite.zip">BurpSuite.zip(9KB)</a>

- SHA256: DA6A4A5A480E8FBC7520B306BD738C710F813338CD40394114DCE37298BE2EA5
- MD5: 3837BE938FF57DEF1ACE15FC05FCBFD3

&ensp;&ensp;3. 使用编译好的启动器

### macOS
1. 下载MacOS (Intel)或MacOS (ARM/M1)
2. 放置Loader至如下路径
> /Applications/Burp Suite Professional.app/Contents/java/app

<p align="center"><img src="/static/macOSLoader路径.png" alt="macOSLoader路径"></p>

&ensp;&ensp;3. 修改如下路径文件内容

> /Applications/Burp Suite Professional.app/Contents/Info.plist
<p align="center"><img src="/static/InfoPlist路径.png" alt="Info.plist路径"></p>

&ensp;&ensp;4. 修改Info.plist文件，`<string>-Dexe4j.moduleName=$APP_PACKAGE</string>` 后插入如下语句

```
......
<string>-Dexe4j.moduleName=$APP_PACKAGE</string>
<string>-noverify</string>
<string>-javaagent:$APP_PACKAGE/Contents/Resources/app/BurpSuiteLoader.jar</string>
```
&ensp;&ensp;5. 使用启动台中的BurpSuite快捷方式
## 💻展示

<p align="center"><img src="/static/Main.png" alt="BurpSuitePro"></p>


## 📝讨论

如果您在使用过程中存在疑问或更好的建议，可以提出 [issue](https://github.com/x-Ai/BurpSuite/issues)。

## ❤️致谢

- **surferxyz** && **scz** 二位大拿
- <a href="https://github.com/Hywell">Hywell</a> 
