# Study Compass

Study Compass - a PHP-based web application to discover and manage universities, scholarships, events, and community discussions.

## Key Features
- Browse and search universities and scholarships
- Event listings and management
- User dashboard and application tracker
- Bookmarking and admin management panels
- Forum and posts (community discussion)
- Contract / messaging and contact forms
- Budget estimator and utilities

## Tech stack
- PHP (plain PHP MVC-style organization)
- MySQL (SQL dumps are provided)
- Composer for dependency/autoload
- Front-end assets in `assets/` (CSS, images)

## Quick setup
1. Requirements: PHP 7.4+ (or later), MySQL, Composer, a webserver (Apache/IIS) or PHP built-in server.
2. Clone the repository.
3. Install dependencies (if needed):

```
composer install
```

4. Create a MySQL database and import SQL dumps from the `assets/db/` folder (e.g., `study_compass_final.sql`).
5. Update database configuration in `model/database.php` to set your DB host, name, username, and password.
6. Ensure `vendor/autoload.php` is loadable (Composer creates this).
7. Configure your webserver document root to the project root or run PHP built-in server for quick local testing:

```
php -S localhost:8000
```

Open `http://localhost:8000` (or your configured host) and use the provided pages.

## Project structure (high level)
- `controller/` : Request handlers and controllers (form checks, actions)
- `model/` : Database and data-access models (e.g., `uniModel.php`, `scholarshipModel.php`)
- `view/` : Page templates and UI (e.g., `home.php`, `forum.php`, `userDashboard.php`)
- `assets/` : Styles and SQL dumps (`assets/db/`)
- `vendor/` : Composer dependencies and autoload files

## Important files
- `model/database.php` : DB connection settings — edit this for your environment
- `assets/db/study_compass_final.sql` : Main database schema / seed data
- `controller/loginCheck.php` and `controller/registerCheck.php` : Authentication handlers
- `view/adminDashboard.php` and `view/userDashboard.php` : Admin / user entry points

## Usage notes
- This is a server-side rendered PHP app; pages under `view/` expect PHP execution and DB connectivity.
- Back up your database before importing sample data into an existing database.

## Contributing
- Fork the repo, create a branch, make changes, and open a pull request.
- Add brief notes in PR describing the change and any DB migrations.

## Tests
No automated tests are included. Consider adding PHPUnit tests for models and controllers.

## License
Add a license file (for example MIT) or update this README to state the chosen license.

## Contact
For questions, open an issue or contact the maintainer via the repository issue tracker.
# Study_Compass
