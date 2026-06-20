# Torrent Downloader Awesome

A powerful collection of GitHub Actions workflows to download torrents directly into your GitHub releases or S3-compatible cloud storage (like ArvanCloud). Bypass local bandwidth limitations and leverage GitHub's fast network to download and archive large files!

---

## 🇬🇧 English

### Features
- **Direct Download**: Fetches files via magnet link or torrent URL using `qBittorrent-nox`.
- **Flexible Compression**: Compresses downloaded files (ZIP, TAR, RAR, TAR.GZ) with split-archive support (e.g., splitting a large file into 1GB RAR parts).
- **GitHub Releases Integration**: Automatically uploads the downloaded/compressed files directly to GitHub Releases.
- **ArvanCloud S3 Upload**: Includes a specialized workflow (`arvan.yml`) to upload the output to ArvanCloud Object Storage.
- **Disk Space Management**: Option to free up GitHub runner disk space before downloading large torrents.

### How to Use
1. Fork or clone this repository.
2. Go to the **Actions** tab of your repository.
3. Select the desired workflow from the left sidebar (e.g., *Download Torrent to GitHub Release* or *Download Torrent and Upload to ArvanCloud*).
4. Click on **Run workflow**.
5. Fill in the required inputs:
   - `magnet_link`: Your torrent magnet link.
   - `compression`: Choose between `none`, `zip`, `tar`, `tar.gz`, or `rar`.
   - `rar_split_size`: For RAR compression, you can specify split sizes like `1000m` or leave empty for a single file.
6. Click **Run workflow** and wait for the magic to happen! The files will appear in the Releases section or your Cloud Storage once completed.

### Requirements
- A GitHub account.
- If using the ArvanCloud workflow, you must add `ARVAN_ACCESS_KEY` and `ARVAN_SECRET_KEY` to your repository's **Secrets**.

---

## 🇮🇷 فارسی (Persian)

### ویژگی‌ها
- **دانلود مستقیم**: دریافت فایل‌ها از طریق لینک مگنت یا آدرس تورنت با استفاده از `qBittorrent-nox`.
- **فشرده‌سازی منعطف**: فشرده‌سازی فایل‌های دانلود شده با فرمت‌های (ZIP, TAR, RAR, TAR.GZ) به همراه قابلیت تکه‌تکه کردن (مثلاً تقسیم یک فایل حجیم به پارت‌های یک گیگابایتی RAR).
- **آپلود در گیت‌هاب**: آپلود خودکار فایل‌های نهایی به صورت مستقیم در بخش GitHub Releases.
- **آپلود در آروان‌کلود**: شامل یک ورک‌فلوی اختصاصی (`arvan.yml`) برای آپلود فایل‌ها در فضای ابری (Object Storage) آروان‌کلود.
- **مدیریت فضای دیسک**: امکان آزادسازی فضای سرورهای گیت‌هاب پیش از شروع دانلود تورنت‌های حجیم.

### نحوه استفاده
۱. این مخزن را Fork کنید یا به اکانت خود منتقل نمایید.
۲. به تب **Actions** در مخزن خود بروید.
۳. ورک‌فلوی مورد نظر خود را از منوی سمت چپ انتخاب کنید (مثلاً *Download Torrent to GitHub Release* یا *Download Torrent and Upload to ArvanCloud*).
۴. روی دکمه **Run workflow** کلیک کنید.
۵. اطلاعات خواسته‌شده را وارد کنید:
   - `magnet_link`: لینک مگنت فایل تورنت شما.
   - `compression`: انتخاب نوع فشرده‌سازی (none, zip, tar, tar.gz, rar).
   - `rar_split_size`: تعیین حجم هر پارت در صورت استفاده از فرمت RAR (مثلاً `1000m`).
۶. روی **Run workflow** کلیک کنید و منتظر بمانید. فایل‌ها پس از اتمام فرآیند در بخش Releases یا فضای ابری شما قرار خواهند گرفت.

### پیش‌نیازها
- یک حساب کاربری گیت‌هاب.
- در صورت استفاده از ورک‌فلوی آروان‌کلود، باید `ARVAN_ACCESS_KEY` و `ARVAN_SECRET_KEY` را در بخش **Secrets** مخزن خود ذخیره کنید.
