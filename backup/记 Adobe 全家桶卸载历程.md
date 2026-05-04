Adobe 全家桶的流氓一向是有目共睹的，我使用 Acrobat 编辑PDF，Photoshop处理图像。功能没话说，毕竟这么多年的技术沉淀，但太繁重了，不管是体积还是内存占用都和我要解决的问题不成正比，并且在AI愈来强大的今天，很多步骤已经不需要人来操作了。我真正需要的，仅仅是能够快速处理一些简单事物的轻量化工具。

## 官方清理工具
[Adobe Creative Cloud Cleaner Tool ](https://helpx.adobe.com/cn/creative-cloud/apps/troubleshoot/diagnostics-repair-tools/run-creative-cloud-cleaner-tool.html)是官方提供的用于清理Adobe应用的工具，下载下来后，以管理员模式运行，选择要卸载的组件即可。但是我运行后竟然没能找到Acrobat，于是先到控制面板卸载Acrobat，然后在去运行工具，我选择全部清除。

虽然该工具由官方提供，但是并没有那么可靠，因为Creative Cloud Cleaner Tool 主要针对 Creative Cloud 系列套件，对于部分工具或者较早的版本是无法识别的。因此系统中还有大量的残余文件和注册表遗留，需要手动删除大量目录，包括
- %ProgramData%\Adobe
- %ProgramFiles(x86)%\Adobe
- %ProgramFiles%\Adobe
- %ProgramFiles(x86)%\Common Files\Adobe
- %ProgramFiles%\Common Files\Adobe
- %LocalAppData%\Adobe
- %UserProfile%\AppData\LocalLow\Adobe
- %AppData%\Adobe

到这里还没完，Adobe还在其他地方散落了不少文件夹……

因为，我的建议是使用文件查找工具（比如listary、everything）直接找Adobe、Photoshop、Acrobat、Creative Cloud等关键词，删之前注意看看该文件的完整路径，因为很可能是其他软件用到了相关的工具。

接下来打开注册表，找到以下位置，删除它们（编辑注册表是危险行为，请记得备份）。
- HKEY_CURRENT_USER\SOFTWARE\Adobe
- HKEY_LOCAL_MACHINE\SOFTWARE\Adobe
- HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Adobe
- HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Adobe

## 替代品
[affinity](https://www.affinity.studio/download)是一款知名的专业设计创意软件，已被设计平台 Canva 收购。升级为整合图像修图、矢量设计和排版三大功能的 Affinity Studio，并已向所有用户永久免费开放。不仅免费，更整合了Photoshop的主力功能甚至提供了RAW文件处理等专业能力。但像AI填充、AI背景移除等高级AI功能可能要订阅Canva付费，但大部分功能已经够用了。

[KillerPDF](https://github.com/SteveTheKiller/KillerPDF)是一款仅 6MB 大小的 PDF 编辑工具，支持标注、合并、拆分、编辑文字、手绘、签名和加密等功能（适用于 Windows 10/11 系统），性能优异，并且无需安装即可运行。已知限制包括：不支持提取表格、不能导出Word、不支持OCR，适合快速批注、合并等基础操作，不适合复杂格式转换。