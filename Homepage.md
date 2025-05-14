# Selamat datang di Vault-ku 👏

> [!quote]
> _"Setiap ide kecil bisa menjadi sesuatu yang besar."_ 

---

## Fleeting Note
```dataview
LIST
FROM #fleeting AND !"99_Templates" AND !"98_Archives"
SORT file.name asc
LIMIT 5
```

## Catatan Harian
```dataviewjs
dv.table(["Hari"], 
  dv.pages('"04_Daily_Journals"')
    .sort(p => p.file.name, 'desc')
    .limit(5)
    .map(p => [
      p.file.link
    ])
)
```
