# AI-Powered Onboarding Buddy System (IBM Bob Capstone Project)

Repositori/paket proyek ini berisi konfigurasi lengkap, *system prompt*, serta dokumen *knowledge base* untuk **AI-Powered Onboarding Buddy System** yang dibangun di atas platform **IBM Bob**.

## Struktur Direktori
- `agent_config.json`: File konfigurasi ekspor agen IBM Bob (berisi parameter model, pengaturan *knowledge base*, dan *system prompt*).
- `system_prompt.txt`: Teks lengkap *Prompt Layering* yang digunakan pada instruksi sistem agen.
- `knowledge_base/`:
  - `Handbook_Karyawan_Baru.pdf`: Dokumen panduan orientasi karyawan baru.
  - `FAQ_SOP_Perusahaan.docx`: Dokumen tanya-jawab prosedur operasional standar (jam kerja, cuti, klaim kesehatan, fasilitas).
- `evaluation_logs.json`: Catatan hasil pengujian interaksi pengguna di *Playground* IBM Bob.

## Arsitektur Prompt (Prompt Layering)
1. **System Persona & Role Layer**: Menetapkan identitas sebagai *Onboarding Buddy* yang ramah, suportif, dan profesional.
2. **Context & Knowledge Boundary Layer**: Membatasi referensi hanya pada dokumen internal (`Handbook_Karyawan_Baru.pdf` dan `FAQ_SOP_Perusahaan.docx`) untuk mencegah halusinasi.
3. **Behavior & Tone of Voice Layer**: Mengatur gaya bahasa yang menyambut (*welcoming*), sabar, dan terstruktur.
4. **Task & Response Formatting Layer**: Memastikan jawaban prosedural disajikan dengan *bullet points* dan diakhiri kalimat penyemangat.

## Cara Menggunakan / Import ke IBM Bob
1. Masuk ke dashboard **IBM Bob**.
2. Buat project baru dengan nama `Onboarding Buddy System`.
3. Salin isi dari `system_prompt.txt` ke kolom **System Prompt**.
4. Unggah seluruh file di dalam folder `knowledge_base/` ke bagian **Knowledge Base**.
5. Uji coba menggunakan skenario pada bagian **Playground / Chat Preview**.
