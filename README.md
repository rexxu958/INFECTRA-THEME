# INFECTRA PANEL

<p align="center">
  <img src="INFECTRA.png" alt="INFECTRA Logo" width="520">
</p>

<h3 align="center">A Dark Interface. A Powerful Identity.</h3>

<p align="center">
  A dark Pterodactyl panel theme with bold purple accents and a distinctive INFECTRA identity.
</p>

<p align="center">
  <strong>Dark UI · Purple Accent · Modern Design</strong>
</p>

---

## Overview

**INFECTRA** is a panel theme project built around a dark, mysterious aesthetic. Deep black surfaces and vivid purple accents create a recognizable visual identity while keeping the interface focused and uncluttered.

## Features

- **Dark interface** with a black foundation
- **Purple accents** inspired by the INFECTRA brand
- **Consistent visual identity** for your panel
- **Installation guide** for compatible Pterodactyl Panel environments

## Installation

> **Important:** Back up your panel files and database before updating. Replacing panel files can break compatibility if the archive does not match your installed Pterodactyl version. Verify the archive contents and compatibility before proceeding.

### 1. Enter the panel directory

```bash
cd /var/www/pterodactyl
```

### 2. Enable maintenance mode

```bash
php artisan down
```

### 3. Download and extract INFECTRA

The release archive is named `panel-infectra-saas.tar.gz`.

```bash
curl -fL https://github.com/rexxu958/INFECTRA-THEME/releases/latest/download/panel-infectra-saas.tar.gz | tar -xzv
```

### 4. Set permissions

```bash
chmod -R 755 storage/ bootstrap/cache
```

### 5. Update dependencies (only if required)

Run this only if the release requires dependency changes and you have verified the package configuration.

```bash
composer install --no-dev --optimize-autoloader
```

### 6. Clear cached files

```bash
php artisan view:clear
php artisan config:clear
php artisan cache:clear
```

### 7. Run database migrations only if required

Back up your database first. Do not run migrations blindly when updating a theme-only package.

```bash
php artisan migrate --seed --force
```

### 8. Set ownership

For a typical Ubuntu installation using Nginx:

```bash
chown -R www-data:www-data /var/www/pterodactyl
```

Use the correct web-server account for your operating system and configuration.

### 9. Restart queue workers

```bash
php artisan queue:restart
```

### 10. Exit maintenance mode

```bash
php artisan up
```

Open your panel and verify that it works correctly. If an error occurs, inspect the application logs before trying additional changes.

## Compatibility

- **Platform:** Pterodactyl Panel
- **Theme package:** INFECTRA
- **Archive:** `panel-infectra-saas.tar.gz`
- **Compatibility:** Depends on the archive contents and installed panel version

## License

Check the license terms of Pterodactyl and all bundled components before redistributing this package.

---

<p align="center">
  <strong>INFECTRA</strong><br>
  <em>Dark by design. Distinct by nature.</em>
</p>
