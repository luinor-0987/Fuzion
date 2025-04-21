# ⚡ Fuzion 1.0

> **A Lightweight and Fast Web Fuzzer written in Lua**  
> Created by **luinor-0987**

---

## 🚀 Overview

**Fuzion 1.0** is a simple, efficient, and scriptable web fuzzer built using pure Lua.  
It's tailored for brute-forcing directories, files, or endpoints on web servers using a wordlist and supports real-time progress tracking with clean, color-coded output.

---

## 🎯 Features

- 🔍 **Customizable Fuzzing**: Use the placeholder `FUZION` in the URL to inject payloads.
- 🎨 **Color-Coded Output**:
  - 🟢 Green → 200 OK
  - 🟡 Yellow → 3xx Redirects
  - 🔴 Red → 4xx/5xx Errors
- ⏱️ **Request Timing**: Shows how long each request takes (in milliseconds).
- 🎯 **Match Specific Status Codes**: Only show results for codes you want (e.g., `200,403`).
- 🧠 **Custom HTTP Headers**: Add headers like `User-Agent` or `Authorization`.
- 🧵 **Threading Placeholder**: Multithreading planned for future versions.
- 📄 **Output Logging**: Save all valid results to a file.
- 📊 **Live Progress Tracker**:
  ```
  :: Progress: [1578/5000]
  ```

---

## 🛠️ Usage

```
fuzion -u http://target.com/FUZION -w wordlist.txt [options]
```

### 🔧 Options
---------------------------------------------------------------------------------------
| Option        | Description                                                         |
|---------------|---------------------------------------------------------------------|
| `-u`          | Target URL (use `FUZION` where fuzzing should occur)                |
| `-w`          | Path to your wordlist file                                          |
| `-t`          | Number of threads (currently unused, default: 30)                   |
| `-mc`         | Match specific HTTP status codes (comma-separated, e.g., `200,403`) |
| `-o`          | Output file to save results                                         |
| `-H`          | Add a custom HTTP header (e.g., `'User-Agent: Fuzion'`)             |
| `-h`          | Show help message                                                   |
---------------------------------------------------------------------------------------

---

## 🔄 Example

```
fuzion -u http://example.com/FUZION -w common.txt -mc 200,403 -o results.txt
```

---


## 🧠 Author

**luinor-0987**  
> *From ping to pwn — one line of Lua at a time.*
