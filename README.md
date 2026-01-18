# ckanext-template

**ckanext-template** adalah ekstensi CKAN yang dirancang khusus untuk kustomisasi tampilan (theming). Ekstensi ini memungkinkan modifikasi antarmuka pengguna, penambahan aset CSS/JS kustom, dan perombakan struktur template standar CKAN agar sesuai dengan identitas visual organisasi Anda.

## ✨ Fitur Utama

* **Custom Templates:** Override template inti CKAN dengan mudah.
* **Asset Management:** Integrasi CSS dan JavaScript kustom.
* **Responsive Design:** Optimasi tampilan untuk berbagai perangkat.
* **Easy Integration:** Kompatibel dengan plugin CKAN standar lainnya.

---

## 📋 Requirements

Ekstensi ini telah diuji dan berjalan optimal pada versi CKAN berikut:

| CKAN Version | Compatible? |
| --- | --- |
| 2.8 and earlier | Not Tested |
| 2.9 | Yes |
| 2.10 | **Tested (Recommended)** |

---

## 🚀 Installation

Ikuti langkah-langkah berikut untuk menginstal **ckanext-temabaru**:

1. **Aktifkan Virtual Environment CKAN Anda:**
```bash
. /usr/lib/ckan/default/bin/activate

```


2. **Clone dan Instal Ekstensi:**
```bash
git clone https://github.com/mostjaww/ckanext-template.git
cd ckanext-temabaru
pip install -e .
pip install -r requirements.txt

```


3. **Konfigurasi CKAN:**
Buka file konfigurasi CKAN Anda (biasanya `/etc/ckan/default/ckan.ini`) dan tambahkan `temabaru` ke daftar plugin:
```ini
ckan.plugins = ... temabaru

```


4. **Restart CKAN:**
```bash
sudo service apache2 reload
# Atau jika menggunakan supervisor:
# sudo supervisorctl restart ckan-uwsgi

```



---

## ⚙️ Config Settings

Saat ini tidak ada pengaturan tambahan yang wajib diisi. Namun, Anda dapat menyiapkan *placeholder* berikut jika diperlukan di masa mendatang:

```ini
# Contoh pengaturan opsional (saat ini belum digunakan)
# ckanext.temabaru.custom_logo = path/to/logo.png

```

---

## 👨‍💻 Developer Installation

Untuk melakukan pengembangan (development), gunakan langkah berikut:

```bash
git clone https://github.com/mostjaww/ckanext-template.git
cd ckanext-temabaru
pip install -e .
pip install -r dev-requirements.txt

```

---

## 🧪 Tests

Untuk menjalankan pengujian (automated tests), gunakan perintah:

```bash
pytest --ckan-ini=test.ini

```

---

## 📦 Releasing a New Version

Langkah-langkah untuk mempublikasikan versi baru ke PyPI:

1. Update nomor versi di `pyproject.toml` atau `setup.py`.
2. Pastikan *build tools* sudah terbaru:
```bash
pip install --upgrade setuptools wheel twine build

```


3. Build distribusi:
```bash
python -m build && twine check dist/*

```


4. Upload ke PyPI:
```bash
twine upload dist/*

```


5. Tag versi di GitHub:
```bash
git tag 0.0.1
git push --tags

```



---

## 📄 License

Ekstensi ini dilisensikan di bawah [AGPL v3.0](https://www.gnu.org/licenses/agpl-3.0.en.html).

---
