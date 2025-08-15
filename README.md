# Deskripsi GreyAI

**GreyAI** adalah MVP yang memadukan **kumpulan model AI** untuk dua kebutuhan paling praktis hari ini:
**(1)** generasi gambar berkualitas cepat, **(2)** pembuatan website satu-klik dari prompt. Semuanya dalam satu antarmuka sederhana yang berjalan lokal/privat.

## Ringkas (elevator pitch)

**GreyAI = “Studio kreatif & dev web instan berbasis multi-model.”** Tulis ide, pilih model, dapatkan gambar siap pakai atau halaman web siap preview dalam hitungan detik.

## Apa yang membuat GreyAI beda

* **Multi-model hub**: SDXL Turbo, RealVisXL, Playground v2.5, PixArt, SD3 Medium/Large, FLUX (dev), hingga SDXL Base+Refiner—pilih sesuai gaya/kecepatan.
* **Prompt panjang aman**: Otomatis memecah prompt SDXL/SD3 (CLIP 77 token) dan mengalihkan sisa ke encoder T5 (SD3) agar tidak terpotong.
* **Kontrol kreatif**: Dukungan **negative prompt** dan **CFG/guidance** (termasuk mapping otomatis `guidance_scale`↔`guidance` untuk model seperti FLUX).
* **Ramah sumber daya**: Offload CPU, attention/vae slicing & tiling, auto clamp resolusi—meminimalkan OOM di GPU T4/P100 sekalipun.
* **Web code generator**: Minta “landing page SaaS warna gelap dengan hero & CTA”—GreyAI mengalirkan HTML siap preview di browser.
* **Satu panel, workflow lengkap**: pilih model, atur ukuran, steps, CFG, seed; klik generate; simpan file hasil di folder `static/outputs`.

## Fitur utama

* **Image Generation**

  * Mode cepat (Turbo) & mode kualitas (Base+Refiner).
  * Pengaturan: resolusi (kelipatan 64), steps, CFG/guidance, negative prompt, seed.
  * Preset cerdas per model (mis. Turbo: steps 6–12, cfg 0–1; SD3: steps 24–32, cfg 3–5).
* **Web Code Generation**

  * Output HTML tunggal, langsung preview & copy.
  * Streaming token real-time untuk pengalaman “coding live”.
* **Manajemen Model**

  * Daftar cache HF, hapus model dari disk via UI, auto-unload dari memori.
* **Observabilitas**

  * Panel statistik CPU/RAM/GPU/Disk.
  * Log debug opsional untuk panjang token per segmen prompt.

## Siapa yang cocok

* **Desainer & marketer**: moodboard, hero image, variasi visual cepat.
* **Founder & PM**: prototipe landing page/feature page tanpa dev cycle panjang.
* **Engineer R\&D**: eksperimen lintas model dan baseline evaluasi gaya/kecepatan.

## Alur kerja singkat

1. Pilih **Image** atau **Web Code**.
2. Tulis **prompt** (+ **negative prompt** opsional).
3. Pilih **model** & set **CFG/steps** (preset otomatis menyesuaikan).
4. **Generate** → simpan/unduh hasil atau langsung **preview** HTML.

## Nilai utama

* **Cepat memulai**: tanpa vendor lock-in; berjalan lokal dengan token HF.
* **Fleksibel**: gonta-ganti model sesuai gaya & kebutuhan performa.
* **Aman**: data tetap di lingkungan Anda.

> **Tagline:** *“GreyAI — dari ide ke gambar & situs, dalam hitungan detik.”*
