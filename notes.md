---
type: Activity
Status: Active
product: APS
Date: 2026-06-10
---
# NOTES

## Infrastructure and Securities

- [ ] Secure `username`, `password`, and others credentials on auth service
- [ ] Change host database to alias for auth service
- [ ] Secure env on laravel backend APS

```shellscript
php artisan config:clear
php artisan config:cache
rm .env
```
