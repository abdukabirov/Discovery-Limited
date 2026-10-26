<h1 align="center">Discoveria</h1>

<p align="center">
  A web app for managing team projects: scrum board, deadlines and Gantt chart in one place.
</p>

<p align="center">
  <img alt="PHP" src="https://img.shields.io/badge/-PHP-777BB4?style=flat-square&logo=php&logoColor=white" />
  <img alt="MySQL" src="https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
  <img alt="JavaScript" src="https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
  <img alt="HTML5" src="https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
  <img alt="CSS3" src="https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
  <img alt="PHPUnit" src="https://img.shields.io/badge/-PHPUnit-3776AB?style=flat-square&logo=php&logoColor=white" />
  <img alt="Playwright" src="https://img.shields.io/badge/-Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" />
</p>

## Features

- **Accounts:** register, sign in and view your profile.
- **Projects:** create a project, join it or leave it, and delete it.
- **Scrum board:** tasks move between **Backlog**, **To Do**, **In Progress** and **Done** by drag and drop. Each task has a title, description, deadline and a coloured tag. You can add, edit and delete tasks.
- **Deadlines:** a list of project deadlines that you can finish or leave.
- **Gantt chart:** the project timeline at a glance.

## Built with

- PHP with PDO and a MySQL database
- HTML, CSS and JavaScript (no framework), [Handlebars](https://handlebarsjs.com) templates
- [PHPUnit](https://phpunit.de) for PHP tests and [Playwright](https://playwright.dev) for JavaScript tests

## Getting started

You need PHP 8.2 or newer, [Composer](https://getcomposer.org) and a MySQL or MariaDB server.

1. Clone the repository:

   ```bash
   git clone https://github.com/abdukabirov/Discovery-Limited.git
   cd Discovery-Limited
   ```

2. Create an empty database and a user for it, then put your own details in `webpages/config.php`:

   ```php
   'db' => [
       'host'    => 'localhost',
       'dbname'  => 'your_database',
       'user'    => 'your_user',
       'pass'    => 'your_password',
       'charset' => 'utf8mb4'
   ],
   ```

   The repository does not include the SQL file for the tables yet, so you need to create them yourself or add the schema first.

3. Start a local server and open <http://localhost:8000>:

   ```bash
   php -S localhost:8000 -t webpages
   ```

## Tests

PHP tests:

```bash
composer install
vendor/bin/phpunit
```

JavaScript tests:

```bash
cd unitTestJS
npm install
npx playwright install
npx playwright test
```

## Project structure

```
webpages/        Pages, PHP endpoints and the frontend
  src/css/       Styles
  src/static/    JavaScript for each page
phpUnitTests/    PHP tests
unitTestJS/      Playwright tests
```
