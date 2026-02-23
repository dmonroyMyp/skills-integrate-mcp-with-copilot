# Database Storage

## Problem

All data is currently stored in memory, which means everything is lost when the server restarts. This is not suitable for production use.

## Recommended Solution

Implement persistent database storage:

- Replace in-memory storage with a database (SQLite recommended for simplicity)
- Create database schema for:
  - Activities
  - Users
  - Events
  - Committees
  - Registrations
  - Feedback
- Add database migration system
- Implement proper database connection handling
- Add database initialization script
- Include sample data seeding for development

## Context

Using SQLite is ideal because:
- No separate database server needed
- File-based and easy to set up
- Perfect for small to medium applications
- Can be easily backed up
- If the application grows, migration to PostgreSQL or MySQL is straightforward

The database file should be excluded from version control (.gitignore) but a schema file should be included.
