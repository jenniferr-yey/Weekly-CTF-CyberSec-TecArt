# TecArt Week 0 - Reverse Engineering

NIM: 260530911059
Nama: Jennifer
Divisi: Reverse Engineering dan Binary Exploitation

## Tools

- WSL
- Ubuntu
- Python
- Git
- Binary Ninja

## Python Test
![Python Test] (images/pythontest.png)

Program:
test.py

![Python Test] (images/pythontest_run.png)

Output:
Hello TecArt
Jenni

## CYLAB UNDO CHALLENGE

Kategori: General Skills
Difficulty: Easy

![CYLAB UNDO] (images/UNDO_CHALLENGE.png)

Challenge ini meminta kita membalik beberapa transformasi teks menggunakan command Linux.

![CYLAB UNDO] (images/UNDO_STEP.png)

Step 1 — Base64
Hint menunjukkan bahwa data perlu dibalik menggunakan Base64.

Step 2 — Reverse Text
Teks dibalik menggunakan: rev

Step 3 — Dash menjadi Underscore
Underscore diganti menjadi dash menggunakan: tr '-' '_'

Step 4 — Parentheses menjadi Curly Braces
Parentheses diganti menjadi curly braces: tr '()' '{}'

Step 5 — ROT13
Transformasi ROT13 dibalik menggunakan: tr 'A-Za-z' 'N-ZA-Mn-za-m'

![CYLAB UNDO] (images/UNDO_FLAG.png)

Flag yang berhasil ditemukan:
picoCTF{Revers1ng_t3xt_Tr4nsf0rm@t10ns_fa04039f}


## Icibos Tekart 0

Tool: Binary Ninja

!(images/binaryninja.png)

Hasil:
Binary dianalisis menggunakan Binary Ninja.
Fungsi main() diperiksa untuk memahami alur program dan menemukan flag.

Flag:
tecart{1ntr0_to_R3vEr1n9}

## Icibos Tekart 1

Tool: Binary Ninja + WSL

![Analisis Binary Ninja] (images/binary_main.png)

Hasil:
1. Fungsi main() dianalisis untuk menemukan password.
2. Password dibandingkan dengan string "bukanString".
3. Jika password benar, program memanggil fungsi win().
4. Fungsi win() menggandakan input.
5. Data input kemudian di-XOR dengan byte yang disimpan dalam array.
6. Hasil XOR ditulis menggunakan fwrite().
7. Hasil transformasi digunakan untuk mendapatkan flag.

Flag:
tecart{*ptr_vS_5tr1ng}

## Kesimpulan

Saya mempelajari dasar penggunaan Linux/WSL, Python, Git, Binary Ninja, serta dasar Reverse Engineering dengan menganalisis alur program dan operasi XOR pada binary.
