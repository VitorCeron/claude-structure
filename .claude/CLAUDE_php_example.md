# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

This project is an CRUD of users to enable the admin to manage users data.

## Stack

- PHP 8+
- Laravel 13+
- Postgres
- PHPUnit

## Commands

```bash
docker-compose up -d                                    # Run the project
docker-compose stop                                     # Stop the project
docker exec -ti container_name bash                     # Enter in project container
php artisan queue:work --queue=queue_name               # Run queue
php artisan schedule:work                               # Run schedule jobs
./vendor/bin/phpunit                                    # Run all tests
./vendor/bin/phpunit path_to_test --testdox             # Run specific class of test and show test dox
./vendor/bin/phpunit path_to_test --filter=method_name  # Run specific test method in a class
./vendor/bin/phpunit --coverage-html tests/reports      # Run coverage report
```

## Architecture

```
- app
    - Console
        - Commands
        - Kernel.php
    - Domains
        - [Module]
            - Services
                - Interfaces
                    - ModuleServiceInterface.php
                - ModuleService.php
            - Repositories
                - Interfaces
                    - ModuleRepositoryInterface.php
                - ModuleRepository.php
    - Enums
    - Exceptions
    - Http
        - Controllers
        - Middleware
        - Requests
        - Resources
        - Kernel.php
    - Jobs
    - Mail
    - Models
    - Notifications
    - Providers
    - Utils
- config
- database
    - factories
    - migrations
    - seeders
- tests
    - Feature
    - Unit
```

### app/Console
- **Responsability:** Schedule commands from application.
- **Rules:**
  - Shouldn't have business rules
  - Must have settings for schedule

### app/Domains/[Module]/Services
- **Responsability:** Application modules and business core.
- **Rules:**
  - Must have business rules
  - Shouldn't have implementation details, like database configs
  - Shouldn't access model directly

### app/Domains/[Module]/Repositories
- **Responsability:** Layer database access.
- **Rules:**
  - Shouldn't have business rules
  - Must have related model

### app/Enums
- **Responsability:** Use for items which has finite options.
- **Rules:**
  - Must have enums settings

### app/Exceptions
- **Responsability:** Custom exceptions for application.
- **Rules:**
  - Must have custom exceptions
  - Must have exception http code

### app/Http/Controllers
- **Responsability:** Handle application data, redirect request to correct service.
- **Rules:**
  - Must have try catch with exceptions handled
  - Must have return correct response for user
  - Must be simple with few lines of code
  - Shouldn't have business rules
  - Shouldn't have conditionals or loops

### app/Http/Middleware
- **Responsability:** Control general validations, authorizations.
- **Rules:**
  - Shouldn't have business rules, call service if is need
  - Must have early returns

### app/Http/Requesters
- **Responsability:** Validate and sanitize data.
- **Rules:**
  - Shouldn't have business rules, call service if is need
  - Must have correct validations
  - Must have sanitize data if need
  - Must correct response messages

### app/Http/Resources
- **Responsability:** Format data to return.
- **Rules:**
  - Shouldn't have business rules, call service if is need
  - Must have correct response data

### app/Jobs
- **Responsability:** Proccess can be running on background.
- **Rules:**
  - Shouldn't have business rules, call service if is need
  - Must have queue implementation and correct settings
  - Must have failed method implemented
  - Must have algoritm to not break all the queue

### app/Models
- **Responsability:** Application models.
- **Rules:**
  - Shouldn't have business rules, call service if is need
  - Must have correct data mapper to database

## Agents

- [PHP Specialist](.claude\agents\php-specialist.md)
- [Laravel Specialist](.claude\agents\laravel-specialist.md)

## Skills

- [Commit Helper](.claude\skills\commit-helper\skill.md)

## Rules

- [Code Styles](.claude\rules\php-code-style.md)
- [Security](.claude\rules\php-security.md)
- [Testing](.claude\rules\php-testing.md)
