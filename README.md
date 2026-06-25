# Perfect Translate

Perfect Translate is a Laravel-based translation marketplace built for clients and translators.
It combines role-based project posting, translator profiles, applications, chat, sprint-based project management, review workflows, and Filament admin support.

## Key Features

- Client and translator user roles with Jetstream authentication
- Client project posting and management
- Translator profile, portfolio, certificate uploads, and verification
- Project applications with accept/decline workflows
- Chat per project with file upload support
- Sprint progress tracking and client feedback
- Reviews for completed projects
- Notifications for applications, project updates, and verification
- Filament admin panel for managing resources

## Technologies

- PHP 8.2+ and Laravel 11
- Laravel Jetstream with Livewire
- Filament admin panel
- Tailwind CSS, Vite, React, Bootstrap
- Pusher / Laravel Echo for realtime features
- SQLite / MySQL compatible database support

## Installation

1. Clone the repository

```bash
git clone https://github.com/your-repo/Perfect-Translate-main.git
cd Perfect-Translate-main
```

2. Install PHP dependencies

```bash
composer install
```

3. Install Node dependencies

```bash
npm install
```

4. Copy environment variables

```bash
cp .env.example .env
```

5. Generate application key

```bash
php artisan key:generate
```

6. Configure database connection

- Default uses `DB_CONNECTION=sqlite`
- For MySQL, update `DB_CONNECTION`, `DB_HOST`, `DB_DATABASE`, `DB_USERNAME`, and `DB_PASSWORD`

7. Run migrations

```bash
php artisan migrate
```

8. Optionally seed the database if seeders exist

```bash
php artisan db:seed
```

9. Build frontend assets

```bash
npm run dev
```

10. Start the local server

```bash
php artisan serve
```

Then open the application at `http://127.0.0.1:8000`.

## Local Development

- `npm run dev` — start Vite development server
- `npm run build` — compile production assets
- `php artisan serve` — run Laravel locally

## Project Workflow

- Clients can register, post projects, upload documents, manage sprints, and accept translator applications.
- Translators can create profiles, upload certificates, browse open projects, submit applications, and participate in project chat.
- The application includes dedicated routes for:
  - project discovery and filtering
  - translator and client profile viewing
  - application status pages
  - project chat and file uploads
  - sprint progress and feedback

## Admin Panel

If the Filament admin panel is configured, use `/admin` to access the backend interface and manage resources such as:
- Applications
- Clients
- Translators
- Projects
- Portfolios
- Reviews

## Authentication

- Authentication is handled by Laravel Fortify and Jetstream with Livewire.
- User roles are used to separate client and translator functionality.
- Email verification is required for protected routes.

## Environment Notes

The default `.env.example` includes recommended values for:
- `APP_URL`
- `DB_CONNECTION`
- `SESSION_DRIVER`
- `BROADCAST_CONNECTION`
- `MAIL_MAILER`
- `FILESYSTEM_DISK`

For real-time chat and notifications, configure Pusher settings in `.env` if using broadcasting.

## Testing

Run the test suite with:

```bash
php artisan test
```

or with Pest:

```bash
./vendor/bin/pest
```

## License

This project is open source and available under the MIT License.
