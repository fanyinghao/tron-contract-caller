# TRON 智能合约交互工具

[English](README.md) | [中文](README_zh.md)

---

### 简介
一个轻量级的单文件 HTML 工具，用于与 TRON 智能合约进行交互。支持通过 TronGrid HTTP API 读取合约状态（无需钱包），以及通过 TronLink 钱包写入状态。

### 功能特点
*   **单文件**: 无需构建过程，直接在浏览器中打开 `tron-contract-caller.html` 即可使用。
*   **双模式**:
    *   **只读模式**: 使用 TronGrid HTTP API 查询合约状态，无需连接钱包。
    *   **写入模式**: 连接 TronLink 钱包以签名并发送交易。
*   **多网络支持**: 内置支持主网 (Mainnet)、Shasta 测试网和 Nile 测试网。
*   **自动解析**: 自动解析 ABI JSON 并为所有函数生成用户友好的界面。
*   **国际化**: 支持中文和英文界面切换。

### 使用方法
1.  **启动本地服务 (推荐)**:
    ```bash
    # 进入项目目录
    cd tron-contract-interaction
    # 启动服务
    python3 -m http.server 8000
    ```
    然后在浏览器中访问 [http://localhost:8000/tron-contract-caller.html](http://localhost:8000/tron-contract-caller.html)。
    *(或者，您也可以直接双击 `tron-contract-caller.html` 文件打开)*
2.  **选择网络**: 选择合约部署的网络（主网、Shasta 或 Nile）。
3.  **加载合约**:
    *   输入合约地址（T 开头）。
    *   粘贴合约 ABI JSON 内容。
    *   点击“加载合约”。
4.  **交互**:
    *   **读函数 (Read)**: 点击“查询”获取数据。无需连接钱包。
    *   **写函数 (Write)**: 先点击“连接 TronLink”，然后输入参数并点击“发送交易”以触发交易。

### 环境要求
*   现代网页浏览器 (Chrome, Edge, Firefox 等)。
*   [TronLink](https://www.tronlink.org/) 浏览器扩展 (写入操作需要)。

### 许可证
本项目基于 MIT 许可证开源 - 详情请参阅 [LICENSE](LICENSE) 文件。

