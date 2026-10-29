# HASIL EVALUASI PERFORMA PACKAGE RECOMMENDATION

---

### 1. Rangkuman Evaluasi

pengujian dilakukan terhadap 590 sampel data.

| Metrik Evaluasi | Nilai |
| :--- | :---: |
| **Akurasi Routing (Penentu Kategori)** | 75.8% |
| **Hit@5 (%)** | 78.1% |
| **Precision@5 (%)** | 74.5% |
| **MRR (Mean Reciprocal Rank)** | 0.727 |
| **Latensi (ms)** | 4,878 ms (4,8 detik) |

*\*Hit : Hanya melihat secara biner apakah setidaknya ada 1 item relevan di Top-$K$ (tidak peduli ada 1 atau 5 item relevan, nilainya tetap dihitung 1 hit).*

*\*Precision : Memperhitungkan banyaknya item relevan yang berhasil ditampilkan dalam daftar 5 rekomendasi teratas.*

*\*MRR : Seberapa baik model memberikan peringkat dari list 5 item rekomendasi teratas*

---

### 2. Tabel Lengkap Kelompok Pengujian (590 Sampel)

Pengujian mencakup seluruh kelompok uji (Katalog 50% murni studio dan Internet High-Resolution in-the-wild). Kriteria pencocokan (*ground truth*):
1. **Botol, Jar, dan Tray**: dinilai relevan jika kategori sesuai dan (`ProductFunction` sesuai sinonim intensi/kebutuhan ATAU nama produk cocok dengan nama kelas/family target).
2. **Cup, Closure, dan Lid**: dinilai relevan jika kategori sesuai dan nama produk cocok dengan nama kelas/family target.

| No | Kelompok Evaluasi | N | Akurasi Route | Hit@1 | Hit@5 | Presisi@1 | Presisi@5 | MRR |
| :-: | :--- | :-: | :---: | :---: | :---: | :---: | :---: | :---: |
| **A** | **KATALOG 50% (STUDIO BERSIH)** | **214** | **85.0%** | **88.8%** | **91.6%** | **88.8%** | **81.5%** | **0.765** |
| **B** | **INTERNET HD (IN-THE-WILD)** | **376** | **70.5%** | **70.5%** | **70.5%** | **70.5%** | **70.5%** | **0.705** |
| **TOTAL** | **OVERALL SELURUH 590 SAMPEL** | **590** | **75.8%** | **77.1%** | **78.1%** | **77.1%** | **74.5%** | **0.727** |

---

DEMO : https://huggingface.co/spaces/Fadhlu/packaging-recommendation
