---
tags:
  - experience
  - programming
  - javascript
created: 2025-05-12
---

# new Set() Struktur Data Javascript

## Cerita & Konteks

Saat saya sedang mengerjakan coding challenge di codewars pada soal isogram saya cukup kesulitan, dan berakhir dengan mencarinya di internet dan saya menemukannya dimana menggunakan looping
```javascript
function isogram(str)
let word=str.toLowerCase()
for(let i = 0;i < word.length;i++) {
  for(let j= i+1;j < word.length;j++ {
  if(word[i] == word[j]) {
    return false
  }
  }
  return true
}
```
Dan berhasil membuat fungsi isogram tetapi saya penasaran jika looping for nya diganti dengan forEach dan saya pun mencobanya
```javascript
function iso(str){
  return str.toLowerCase().split("").forEach((e,i) => {
    for(let j=i+1; j < str.length; j++) {
      if(e == str[j]) {
        return false
      }
    }
    return true
  })
}
```
Dan saya test ternyata tidak bisa, saya pun cek di Chatgpt apa yang salah dan ternyata forEach tidak bisa mengembalikan nilai (return) dan menampilkan dua cara yang benar dengan looping dan `set` dimana hanya membutuhkan dua baris saja
```javascript
function isogram(str) {
  str=str.toLowerCase()
  return new Set(str).size === str.length;
}
```
Bahkan bisa satu baris saja jika lowercase nya langsung di `Set` nya langsung 

## Hasil

Mengetahui struktur data baru yaitu Set dimana kegunaannya menyimpan nilai-nilai unik jadi huruf yang sama atau array yang sama hanya akan disimpan satu kali saja

## Refleksi

Struktur data ini akan sangat berguna bagi saya karena biasanya say masih kebingungan untuk mengambil nilai unik saja dari string mauoun array

## Terkait
- [[...]]