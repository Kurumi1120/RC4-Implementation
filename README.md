# RC4-Implementation
此專案使用Python語言進行簡易的RC4加密演算法演示。

# 功能介紹
- **金鑰初始化**：根據使用者輸入的金鑰生成加密狀態陣列。
- **加密過程**：
  - KSA（Key Scheduling Algorithm）：初始化置換陣列 S。
  - PRGA（Pseudo-Random Generation Algorithm）：生成偽隨機密鑰流。
  - XOR 操作：將明文與密鑰流進行位元級異或，生成密文。
- **輸出格式**：加密結果以十六進位字串顯示。

# 需求
- **Python 3.x**：此專案使用 Python 標準庫，無須額外安裝內容。
