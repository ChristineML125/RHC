# Document Management System

This project implements the four requested functions:

1. Upload PDF, Word, and report files.
2. Organize documents by department, category, and branch.
3. Search quickly by keyword and filters.
4. Keep version history with `v1`, `v2`, and one latest version.

## Stack

- Frontend: React + Vite
- Backend: Node.js + Express
- Database: SQL Server
- File upload: Multer local storage

## Run In VS Code

1. Open this folder in VS Code:

   `C:\Users\USER\Desktop\RHC\DocumentManagement`

2. Create the SQL Server database:

   Open `database/schema.sql` in SQL Server Management Studio or Azure Data Studio, then run it.

3. Configure the API:

   Copy `server/.env.example` to `server/.env`, then update your SQL Server username and password.

4. Install dependencies:

   ```bash
   npm install
   npm run install:all
   ```

5. Start the system:

   ```bash
   npm run dev
   ```

6. Open:

   - Frontend: `http://localhost:5173`
   - API: `http://localhost:5000/api/health`

## Database Tables

- `Departments`: HR, IT, Finance
- `Categories`: SOP, Policy, Report
- `Branches`: Sibu, Kuching, Miri
- `Documents`: document title, description, department, category, branch
- `DocumentVersions`: uploaded file versions, original filename, stored filename, latest flag

## Notes

- For a new document, choose `New document`.
- To upload `v2`, select an existing document under `Add as new version`.
- Search supports title, description, original filename, department, category, and branch.
