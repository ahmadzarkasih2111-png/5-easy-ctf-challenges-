# 5-easy-ctf-challenges-

# 5 Easy Challenges 

Dokumentasi lengkap 5 easy challenges tambahan  dengan penjelasan super detail untuk pemula!

---

---

# Challenge 7: Warmed Up (Easy - 50 Points)

## 📝 Penjelasan Sederhana

**Apa ini?** Challenge paling dasar - convert satu byte dari decimal ke flag format.

**Contoh:**
```
Anda diberikan number: 49
Convert ke character: '1'
Flag format: picoCTF{1}
```

---

## 🔍 Step-by-Step

### Step 1: Download File

1. Login PicoCTF
2. Cari "Warmed Up"
3. Download file atau lihat number yang diberikan

Contoh:
```
Number: 49
```

---

### Step 2: Convert Decimal ke Character

**Cara paling simple - pakai Python:**

```python
# Buka Python interpreter
python3

# Ketik ini:
>>> chr(49)
'1'

# Done!
```

**Atau pakai online tool:**
- Buka: https://www.rapidtables.com/convert/number/decimal-to-ascii.html
- Input: 49
- Output: '1'

---

### Step 3: Format Flag

```
Result: '1'
Flag format: picoCTF{1}
```

---

### Step 4: Submit

- Copy: picoCTF{1}
- Paste di PicoCTF
- Submit!

---

## 💡 Tips

```
Shortcut: Buka Python, ketik chr(NUMBER)
Replace NUMBER dengan angka yang diberikan
Instant result!
```

---

---

# Challenge 8: 2Warm (Easy - 50 Points)

## 📝 Penjelasan Sederhana

**Apa ini?** Convert multiple decimal values ke characters dan format sebagai flag.

**Contoh:**
```
Numbers: 50 100 51 49 46 103 111
Convert each: '2' 'd' '3' '1' '.' 'g' 'o'
Result: 2d31.go
Flag: picoCTF{2d31.go}
```

---

## 🔍 Step-by-Step

### Step 1: Download & Lihat Numbers

```
File berisi: 50 100 51 49 46 103 111
```

---

### Step 2: Convert Dengan Python Script

```python
#!/usr/bin/env python3
"""Convert multiple decimals to ASCII"""

# List of decimal numbers
numbers = [50, 100, 51, 49, 46, 103, 111]

# Convert each to character
result = ""
for num in numbers:
    result += chr(num)

print(f"Result: {result}")
print(f"Flag: picoCTF{{{result}}}")
```

**Jalankan:**
```bash
python3 convert.py

# Output:
# Result: 2d31.go
# Flag: picoCTF{2d31.go}
```

---

### Step 3: Submit Flag

Copy dan submit!

---

---

# Challenge 9: Lets Warm Up (Easy - 50 Points)

## 📝 Penjelasan Sederhana

**Apa ini?** Convert hexadecimal value ke decimal, lalu ke character.

**Contoh:**
```
Hex: 0x3d
Convert to decimal: 61
Convert to character: '='
Flag: picoCTF{=}
```

---

## 🔍 Step-by-Step

### Step 1: Lihat Hex Value

```
File/Description: 0x3d
```

---

### Step 2: Convert Hex ke Decimal

**Method 1 - Python:**
```python
>>> hex_value = 0x3d
>>> decimal = int(hex_value)
>>> print(decimal)
61
```

**Method 2 - Online:**
- Buka: https://www.rapidtables.com/convert/number/hex-to-decimal.html
- Input: 3d (atau 0x3d)
- Output: 61

---

### Step 3: Convert Decimal ke Character

```python
>>> chr(61)
'='
```

---

### Step 4: Format & Submit

```
Flag: picoCTF{=}
```

---

---

# Challenge 10: What's a Net Cat? (Easy - 100 Points)

## 📝 Penjelasan Sederhana

**Apa ini?** Connect ke network service menggunakan netcat command dan capture output/flag.

**Contoh:**
```
Server: jupiter.challenges.picoctf.org
Port: 1234

Anda connect dengan netcat
Server mengirim flag
Anda capture flag
Submit!
```

---

## 🔍 Step-by-Step

### Step 1: Install Netcat

**Linux/Mac:**
```bash
# Usually already installed
# Verify:
nc -h
```

**Windows:**
```
Download: https://eternallybored.org/misc/netcat/
Extract dan gunakan
```

---

### Step 2: Download Challenge Info

Challenge akan memberikan:
```
Server: jupiter.challenges.picoctf.org
Port: 1234
```

---

### Step 3: Connect dengan Netcat

```bash
# Linux/Mac:
nc jupiter.challenges.picoctf.org 1234

# Windows:
nc.exe jupiter.challenges.picoctf.org 1234
```

---

### Step 4: Capture Output

Server akan mengirim text/flag. Contoh:
```
$ nc jupiter.challenges.picoctf.org 1234
picoCTF{n3t_c4t_1s_c00l_12345}
```

---

### Step 5: Submit Flag

Copy dan submit!

---

## 💡 Tips

```
✓ Netcat just connects to server
✓ Wait untuk server kirim data
✓ Bisa screenshot output
✓ Bisa redirect ke file: nc ... > output.txt
```

---

---

# Challenge 11: Strings It (Easy - 100 Points)

## 📝 Penjelasan Sederhana

**Apa ini?** Extract readable strings dari binary file dan cari flag.

**Sama seperti Challenge 6, tapi lebih simple!**

---

## 🔍 Step-by-Step

### Step 1: Download File

Binary executable file akan di-download.

---

### Step 2: Gunakan Strings Command

**Linux/Mac:**
```bash
strings strings_file | grep "picoCTF"

# Output:
# picoCTF{strings_are_n1ce_abcd1234}
```

**Windows:**
```powershell
# Gunakan Python:
python3 -c "
with open('strings_file', 'rb') as f:
    data = f.read()
    text = ''.join(chr(b) for b in data if 32 <= b <= 126)
    if 'picoCTF' in text:
        print(text[text.find('picoCTF'):text.find('}')+1])
"
```

---

### Step 3: Copy Flag

Flag dari output:
```
picoCTF{strings_are_n1ce_abcd1234}
```

---

### Step 4: Submit

Paste dan submit!

---

## 💡 Tips

```
✓ strings command sangat cepat untuk this
✓ Sering kali flag langsung ditemukan
✓ Jika tidak ada, coba dengan grep/findstr
```

---

---

## 📊 Summary - 5 Easy Challenges Baru

| # | Challenge | Category | Points | Time | Difficulty |
|---|-----------|----------|--------|------|------------|
| 7 | Warmed Up | General | 50 | 2min | Very Easy |
| 8 | 2Warm | General | 50 | 5min | Very Easy |
| 9 | Lets Warm Up | General | 50 | 5min | Very Easy |
| 10 | What's a Net Cat | General | 100 | 10min | Easy |
| 11 | Strings It | Reverse Eng | 100 | 5min | Easy |

**Total: 350 points**

---

## 🎯 Quick Checklist - Challenge 7-11

### Challenge 7 (Warmed Up):
```
✅ Get number dari challenge
✅ Use: chr(number)
✅ Format sebagai flag: picoCTF{result}
✅ Submit
```

### Challenge 8 (2Warm):
```
✅ Get list of numbers
✅ Convert each dengan chr()
✅ Combine semua characters
✅ Format flag
✅ Submit
```

### Challenge 9 (Lets Warm Up):
```
✅ Get hex value (0x...)
✅ Convert to decimal: int(0x...)
✅ Convert to char: chr(decimal)
✅ Format flag
✅ Submit
```

### Challenge 10 (What's a Net Cat):
```
✅ Get server info (host, port)
✅ Install netcat (jika belum)
✅ Connect: nc host port
✅ Capture output
✅ Submit flag
```

### Challenge 11 (Strings It):
```
✅ Download binary file
✅ Run: strings file | grep "picoCTF"
✅ Copy flag dari output
✅ Submit
```
Happy Hacking and Hunting 
