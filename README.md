# Manifest Integration Platform
## Airport Operations System

### System Requirements
- PHP 8.2+
- MySQL 8.0+
- Redis 7.0+
- Composer 2+
- Node.js 18+

### Installation Steps

1. Clone repository
2. Run `composer install`
3. Run `npm install && npm run build`
4. Copy `.env.example` to `.env`
5. Configure database, redis, and mail settings
6. Run `php artisan key:generate`
7. Run `php artisan jwt:secret`
8. Run `php artisan migrate --seed`
9. Run `php artisan storage:link`
10. Run `php artisan horizon:install`
11. Start queue worker: `php artisan horizon`
12. Start scheduler: `php artisan schedule:work`

### Security Configuration
- Set strong passwords in .env
- Configure IP whitelist
- Set up SSL certificates
- Enable request signing for API
- Configure CORS properly

### Monitoring
- Access Horizon dashboard at /horizon
- View logs in storage/logs
- Monitor sync jobs in admin panel
- Check health at /api/v1/health

### Backup Strategy
- Daily database backups
- Redis persistence enabled
- Log rotation configured
- Audit logs archived monthly
