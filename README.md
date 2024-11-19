<a name="readme-top"></a>

# Track your Transactions

![Monitor your earnings and spending effortlessly with Finance_dash.](qiraayah.png "Track your income and expenses with Finance.")




## :bangbang: Folder Structure

Here is the folder structure of this app.

```bash
finance-dashboard/
  |- app/
    |-- (auth)/
    |-- (dashboard)/
    |-- api/
    |-- apple-icon.png
    |-- favicon.ico
    |-- globals.css
    |-- icon1.png
    |-- icon2.png
    |-- layout.tsx
  |- components/
    |-- ui/
  |- config/
    |-- index.ts
  |- db/
    |-- drizzle.ts
    |-- schema.ts
  |- drizzle/
  |- features/
    |-- accounts/
    |-- categories/
    |-- summary/
    |-- transactions/
  |- hooks/
    |-- use-confirm.tsx
  |- lib/
    |-- hono.ts
    |-- utils.ts
  |- providers/
    |-- query-provider.tsx
    |-- sheet-provider.tsx
  |- public/
    |-- data.csv
    |-- github.svg
    |-- logo.svg
  |- scripts/
    |-- seed.ts
  |- .env.example
  |- .env.local
  |- .eslintrc.json
  |- .gitignore
  |- .prettierrc
  |- bun.lockb
  |- components.json
  |- drizzle.config.ts
  |- environment.d.ts
  |- middleware.ts
  |- next.config.mjs
  |- package-lock.json
  |- package.json
  |- postcss.config.js
  |- tailwind.config.ts
  |- tsconfig.json
```

<br />

## :toolbox: Getting Started

1. Make sure **Git** and **NodeJS** is installed.
2. Clone this repository to your local computer.
3. Create `.env.local` file in **root** directory.
4. Contents of `.env.local`:

```env
# .env.local

# disabled next.js telemetry
NEXT_TELEMETRY_DISABLED=1

# clerk auth keys
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
CLERK_PUBLISHABLE_KEY=pk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
CLERK_SECRET_KEY=sk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

# clerk redirect url
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

# neon db url
DATABASE_URL=postgresql://<username>:<password>@<hostname>/<database>?sslmode=require

# app base url
NEXT_PUBLIC_APP_URL=http://localhost:3000

```



# Project Setup Guide

Follow these steps to configure and run the project successfully:

---

## 1. Obtain Clerk Authentication Keys

1. Log in to your Clerk account.
2. Navigate to the **Dashboard** or **Settings** page.
3. Locate the section for authentication keys.
4. Copy the following keys:
   - `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY`
   - `CLERK_SECRET_KEY`

---

## 2. Retrieve Neon Database URI

1. Access your database provider’s platform (e.g., Neon or PostgreSQL).
2. Locate the database connection details.
3. Replace placeholders in the URI (`<username>`, `<password>`, `<hostname>`, and `<database>`) with your credentials.
4. Append `?sslmode=require` to the URI to enable SSL.

---

## 3. Specify the Public App URL

Update the `.env.local` file, replacing `http://localhost:3000` with your deployed application’s URL.

---

## 4. Save and Secure Environment Variables

Ensure all environment variables are saved in the `.env.local` file.

---

## 5. Install Project Dependencies

Run one of the following commands to install dependencies:

```bash
npm install --legacy-peer-deps

OR

bash
Copy code
yarn install --legacy-peer-deps
6. Migrate the Database
Generate the database client and apply migrations by running:
bash
Copy code
npm run db:generate
npm run db:migrate
7. Run the Seed Script
Seed the database with initial data using:

bash
Copy code
npm run db:seed
This script executes the scripts/seed.ts file and populates your database with transaction data.

8. Verify Data in the Database
After completing the seed process, check your database to confirm that the data has been successfully added.





