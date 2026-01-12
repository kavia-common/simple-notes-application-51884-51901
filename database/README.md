# Database container (SQLite)

This container provides a SQLite database file:

- `myapp.db`

Connection instructions are kept in:

- `db_connection.txt`

## Initialize / verify database (idempotent)

```bash
python3 init_db.py
```

## Interactive shell

```bash
python3 db_shell.py
```

## Backend wiring expectation

The backend should connect using a file path, typically via an env var, e.g.:

- `SQLITE_DB_PATH=../database/myapp.db` (monorepo relative)
- or the absolute path described in `db_connection.txt` when running across separate workspaces.
