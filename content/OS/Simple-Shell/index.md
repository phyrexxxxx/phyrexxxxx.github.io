---
title: "Single Process Command"
date: 2025-08-12T00:51:07+08:00
draft: true
description: "A comprehensive guide for implementing and testing a simple shell with single process command execution, including automated testing procedures and manual verification steps."
tags: ["Firmware", "OS", "Shell"]
categories: ["OS"]
showTableOfContents: true
showComments: true
showHero: true
heroStyle: "basic"
---

## 下載專案
首先，從 GitHub 下載專案：

```bash
git clone https://github.com/phyrexxxxx/OS-Simple-Shell.git
```
本專案實作了一個簡單的 shell，支援基本的單一進程命令 (Single Process Command) 執行功能，包括命令解析、執行和錯誤處理。


## 執行測試
步驟如下：
```bash
$ cd OS-Simple-Shell
$ make
```
預期輸出:
```
正在連結 my_shell...
編譯完成！
```
```bash
# 進入測試腳本目錄
$ cd simple_tests/01_single_command/scripts
```
預期輸出:
```
=== 單一進程命令測試開始 ===
[INFO] Testing shell binary: /home/yucskr/OS-Simple-Shell/my_shell
[INFO] Test data directory: ../test_data

=== 環境檢查 ===
[PASS] Shell binary found and executable

=== 測試 1: 基本命令執行 ===
[INFO] Testing command: ls
[PASS] ls command executed successfully
[INFO] Output preview: commands.txt text.txt :/home/yucskr/OS-Simple-Shell/simple_tests/01_single_command/test_data >>> $ :/home/yucskr/OS-Simple-Shell/simple_tests/01_single_command/test_data >>> $ ...
[INFO] Testing command: pwd
[PASS] pwd command executed successfully
[INFO] Output preview: /home/yucskr/OS-Simple-Shell/simple_tests/01_single_command/test_data :/home/yucskr/OS-Simple-Shell/simple_tests/01_single_command/test_data >>> $ :/home/yucskr/OS-Simple-Shell/simple_tests/01_single_command/test_data >>> $ ...
[INFO] Testing command: whoami
[PASS] whoami command executed successfully
[INFO] Output preview: yucskr :/home/yucskr/OS-Simple-Shell/simple_tests/01_single_command/test_data >>> $ :/home/yucskr/OS-Simple-Shell/simple_tests/01_single_command/test_data >>> $ ...
[INFO] Testing command: cat text.txt
[PASS] cat command executed successfully
[INFO] Output preview: Hello world A shell interprets user commands into system calls The shell parses input using tokenization ...
[PASS] Basic commands test PASSED

=== 測試 2: 空行處理 (只有空格/Tab的行) ===
[INFO] Testing empty line handling...
[PASS] Shell correctly handles empty lines and continues execution

=== 測試 3: Exit 命令 ===
[INFO] Testing exit command...
[PASS] Exit command works correctly

=== 測試結果總結 ===
通過測試: 3/3
[PASS] 所有單一進程命令測試通過！
```

## 手動測試
```bash
$ cd OS-Simple-Shell
$ make && ./my_shell
正在連結 my_shell...
編譯完成！
:/home/yucskr/OS-Simple-Shell >>> 
```
然後手動輸入以下命令進行驗證：

```bash
# 測試基本命令
ls
pwd
whoami
cat simple_tests/01_single_command/test_data/text.txt

# 測試空行處理 (輸入幾個只有空格或是 tab 的行)
   
	

# 測試退出
exit
```
預期 (參考) 輸出:
```
:/home/yucskr/OS-Simple-Shell >>> $ ls
 README.md    my_shell   src    my_shell.c    Makefile    include    simple_tests
:/home/yucskr/OS-Simple-Shell >>> $ pwd
/home/yucskr/OS-Simple-Shell
:/home/yucskr/OS-Simple-Shell >>> $ whoami
yucskr
:/home/yucskr/OS-Simple-Shell >>> $ cat simple_tests/01_single_command/test_data/text.txt
Hello world
A shell interprets user commands into system calls
The shell parses input using tokenization
Custom shells often rely on `fork()` and `exec()` for execution
I/O redirection lets users manage data streams
Shells often support pipelines for command chaining
:/home/yucskr/OS-Simple-Shell >>> $    
:/home/yucskr/OS-Simple-Shell >>> $ 
:/home/yucskr/OS-Simple-Shell >>> $ exit
$ 
```
