# ⚔️ 七杀·问尘 (Wen Chen)

> “凡事皆有迹，道在微尘间”。这把剑不出鞘，仅凭剑心与剑意，便能感知凡尘中隐藏的蛛丝马迹。

**问尘 (Wen Chen)** 是一款专为渗透人员打造的Burp Suite被动辅助插件。它旨在从海量的JavaScript文件中，精准地发现隐藏的API端点、URI路径和潜在的攻击面，并最终可以为您自动生成一份精准可直接用于实战的目录字典。

---

### ✨ 功能演示 (Demo)

<details>
<summary><strong>点击展开/折叠插件界面截图</strong></summary>
  
*主界面*
<img width="2560" alt="image" src="https://github.com/user-attachments/assets/c6a1a811-7071-4587-8652-b4a4b73451ef" />

*字典输出*
<img width-="1278" height="764" alt="1753530718668" src="https://github.com/user-attachments/assets/004770a0-24d1-486f-a3b3-ceb44cc093b2" />

*路径扩展*
<img width="1278" height="764" alt="Sprawl Demo" src="https://github.com/user-attachments/assets/f8833066-b7f3-4dfc-b64d-c64c42b21bfd" />

*js面板*
<img width="2560" height="1522" alt="image" src="https://github.com/user-attachments/assets/7cdcba3e-7af6-4f8e-acf2-d5e4f788f494" />

</details>

---

### 🚀 核心功能 (Core Features)

| ⭐ 提取能力 (Extraction) | 交互界面 (UI) | 📖 字典生成 (Dictionary) |
| :--- | :--- | :--- |
| **被动提取**：自动监听HTTP响应，识别JS文件并深度分析。 | **双格显示**：清晰展示JS文件URL与提取到的路径。 | **路径分解**：将完整路径拆分为所有子路径组合。 |
| **主动分析**：右键菜单 `go bro` 可手动触发对选中流量的分析。 | **右键菜单**：集成发送到Repeater、复制、清除等常用功能。 | **内存缓存**：实时在内存中对所有路径进行高效去重。 |
| **终极规则**：融合三大知名工具 (`BurpJSLinkFinder`, `jslink`, `FindSomething`) 的优点并加以优化。 | **实时更新**：被动扫描结果实时添加，无需刷新。 | **智能去重**：确保最终输出到文件的字典条目绝对唯一。 |
| **智能过滤**：精准识别并过滤W3C命名空间、JS框架属性、模板语法等噪音。 | **文件管理**：提供“设置保存文件”按钮，由用户指定字典输出路径。 | **文件持久化**：实时将纯净的字典条目追加到指定的.txt文件中。 |


---

### 🎯 使用场景 (Use Cases)

1.  **API发现**：从前端JS代码中发现API端点。
2.  **字典生成**：针对目标站点，自动生成一份高命中率的目录字典，用于后续的渗透工作。
---

### 🛠️ 使用说明 (Usage)

1.  **加载插件**：将编译好的 `WenChen.jar` 文件添加到Burp Suite的扩展中。
2.  **设置路径**：在插件的UI界面，点击 **"Set Save File..."** 按钮，选择或创建一个`.txt`文件作为字典的保存位置。
3.  **开启扫描**：确保 **"Enable Passive Extraction"** 复选框被勾选。
4.  **开始浏览**：正常使用浏览器通过Burp代理访问目标网站。插件会自动监听流经Proxy和Repeater的流量，分析其中的JS文件和请求URI，并将净化、扩展后的结果实时写入您指定的字典文件中。
5.  **切换项目**：如需测试新项目，建议先点击 **"Clear All"** 清空UI数据，然后再次点击 **"Set Save File..."** 设置一个新的字典文件即可。

---

此工具适合渗透测试人员和安全研究人员使用，能够高效地从JavaScript文件中提取有价值的攻击面信息！
