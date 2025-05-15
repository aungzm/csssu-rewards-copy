
![Screenshot 2025-04-11 at 20-23-56 Vite React TS](https://github.com/user-attachments/assets/4fdbfb54-b6c6-4b06-9947-c19d068ce79e)
![Screenshot 2025-04-11 at 20-24-16 Vite React TS](https://github.com/user-attachments/assets/ec8f34e0-13bc-44ca-b26f-72fea8a47c11)
![Screenshot 2025-04-11 at 20-24-25 Vite React TS](https://github.com/user-attachments/assets/894372d7-8550-4313-a330-c2b5dcbf3f76)
![Screenshot 2025-04-11 at 20-24-45 Vite React TS](https://github.com/user-attachments/assets/34b8ae51-c367-4b69-8353-750d4246c0c1)
![Screenshot 2025-04-11 at 20-24-53 Vite React TS](https://github.com/user-attachments/assets/da0d76ed-d2d6-4cd7-b5a4-60234707404e)
![Screenshot 2025-04-11 at 20-25-48 Vite React TS](https://github.com/user-attachments/assets/3a46c7b1-6234-457c-8632-7c2968386646)
![Screenshot 2025-04-11 at 20-26-00 Vite React TS](https://github.com/user-attachments/assets/14d1a749-90fb-4f33-ad10-1d0d3a143807)
![Screenshot 2025-04-11 at 20-26-34 Vite React TS](https://github.com/user-attachments/assets/10c3e78b-98cb-4f22-9aac-f52f7401350d)
![Screenshot 2025-04-11 at 20-26-41 Vite React TS](https://github.com/user-attachments/assets/2012ec55-50e3-440b-bdba-7b9c14d41c91)
![Screenshot 2025-04-11 at 20-26-53 Vite React TS](https://github.com/user-attachments/assets/3cefa30e-2ae8-4cf8-a282-a4e94af3d2b8)
![Screenshot 2025-04-11 at 20-27-03 Vite React TS](https://github.com/user-attachments/assets/b4897771-1951-4f2f-a72d-58a4617126a4)
![Screenshot 2025-04-11 at 20-27-24 Vite React TS](https://github.com/user-attachments/assets/13ae5886-848c-44e1-aeb3-6c7a43ca9563)
![Screenshot 2025-04-11 at 20-27-36 Vite React TS](https://github.com/user-attachments/assets/b7bba54b-4550-4744-921a-08500ce80efc)
![Screenshot 2025-04-11 at 20-28-03 Vite React TS](https://github.com/user-attachments/assets/45f6912a-1597-4a82-b800-38f2b675d9e3)
![Screenshot 2025-04-11 at 20-28-16 Vite React TS](https://github.com/user-attachments/assets/81262c47-3a06-4a1f-b950-07917f732af6)
![Screenshot 2025-04-11 at 20-28-25 Vite React TS](https://github.com/user-attachments/assets/54cc91fc-faaa-44e5-aafa-abb3a9d6535d)
![Screenshot 2025-04-11 at 20-28-34 Vite React TS](https://github.com/user-attachments/assets/ab039565-849d-4f96-a0dd-8d3a69b89189)
![Screenshot 2025-04-11 at 20-28-46 Vite React TS](https://github.com/user-attachments/assets/873d9aed-36b3-42a4-a70a-b3654b054691)
![Screenshot 2025-04-11 at 20-28-55 Vite React TS](https://github.com/user-attachments/assets/78c793be-bbae-4cb4-bb91-2b80bf78fb2f)
![Screenshot 2025-04-11 at 20-29-13 Vite React TS](https://github.com/user-attachments/assets/4cd9cd1a-cb56-43ea-bfc7-6ef50de04e65)
![Screenshot 2025-04-11 at 20-29-29 Vite React TS](https://github.com/user-attachments/assets/cba2fbc1-766a-4c1e-a081-ebd8255cf315)
![Screenshot 2025-04-11 201103](https://github.com/user-attachments/assets/3b2c1ce1-2a3d-476d-8298-b77efd9078be)
![Screenshot 2025-04-11 at 20-23-27 Vite React TS](https://github.com/user-attachments/assets/be59e654-50bc-4d48-a1c7-35c4dee5dde5)
![Screenshot 2025-04-11 at 20-23-47 Vite React TS](https://github.com/user-attachments/assets/b8932213-b51d-4a37-a2fc-cfeb5877ac0c)

# csssu-rewards-copy
We only have permission to show the frontend so this is a copy of the project which was in a competition to design U of T's CSSU point system. **

Backend Deployment Instructions
----------------------------------

Follow the steps below to deploy the backend server in a production environment.

### Prerequisites

Ensure the following dependencies are installed on your system:

-   **Node.js** (v18 or higher recommended)

-   **npm** (v9 or higher)

-   **SQLite** (already used via dependency)

-   Optional: `pm2` or another process manager for persistent deployment

* * * * *

### Setup

1.  **Clone the Repository**

    ```
    git clone <your-repo-url>
    cd backend

    ```

2.  **Install Dependencies**

    ```
    npm install

    ```

3.  **Configure Environment Variables**\
    Create a `.env` file in the `backend` directory. At minimum, include:

    ```
    DATABASE_URL="file:./dev.db"
    JWT_SECRET="<your_jwt_secret>"

    ```

4.  **Generate Prisma Client & Push DB Schema**\
    This resets and syncs the database schema:

    ```
    npm run reset

    ```

5.  **Seed the Database (Optional)**\
    If you have seed data, run:

    ```
    npm run seed

    ```

* * * * *

### Build & Start

1.  **Build the Project**\
    Compile TypeScript into JavaScript:

    ```
    npm run build

    ```

2.  **Start the Server**\
    Launch the compiled server:

    ```
    npm start

    ```

    Alternatively, for development:

    ```
    npm run dev

    ```

* * * * *

### Running Tests

To execute the test suite:

```
npm test

```

This includes setup, running, and teardown automatically.

* * * * *

### Useful Scripts

| Command | Description |
| --- | --- |
| `npm run reset` | Regenerate and force-reset Prisma DB schema |
| `npm run seed` | Resets DB and populates it with seed data |
| `npm run dev` | Starts server with live reload (TS) |
| `npm run build` | Compiles TypeScript to `dist/` |
| `npm start` | Starts compiled JavaScript server |
| `npm test` | Runs the complete test suite |

* * * * *

### Notes

-   Make sure to replace `<your_jwt_secret>` with a secure, random string.

-   Production deployments may want to use `pm2` or Docker for managing the backend process.

-   Ensure ports and CORS settings match your frontend configuration.



Frontend Deployment Instructions
-----------------------------------

Follow these steps to set up and deploy the frontend in a production environment.

### 🔧 Prerequisites

Ensure your system has the following installed:

-   **Node.js** (v18 or higher)

-   **npm** (v9 or higher)

-   A modern browser for previewing

* * * * *

### 🛠️ Setup

1.  **Navigate to the Frontend Directory**\
    From the root of your project:

    ```
    cd frontend

    ```

2.  **Install Dependencies**\
    Install all required packages using:

    ```
    npm install

    ```

3.  **Configure Environment Variables (Optional)**\
    If your application relies on any environment variables (e.g., API base URL), create a `.env` file:

    ```
    VITE_API_BASE_URL="http://localhost:3000"

    ```

    > Vite requires all env variables to be prefixed with `VITE_` to be exposed to the client.

* * * * *

### Development

To start the development server with hot module reloading:

```
npm run dev

```

The app should be available at <http://localhost:5173> by default.

* * * * *

### Production Build

To create a production-ready build:

```
npm run build

```

The optimized and minified static assets will be generated in the `dist/` folder.

You can preview the production build locally using:

```
npm run preview

```

* * * * *

### Demo instance

Demo can be found at: [frontend-production-9895.up.railway.app](frontend-production-9895.up.railway.app)

* * * * *
## Installed Packages

###  Frontend Dependencies

The following key packages are used in the frontend (`/frontend`):

- **React** (`react`, `react-dom`) — Core UI library
- **React Router DOM v7** (`react-router-dom`) — Client-side routing
- **Headless UI** (`@headlessui/react`) — Accessible UI primitives
- **Lucide React** (`lucide-react`) — Icon library
- **QR Code Utilities**:
  - `qrcode.react` — Generate QR codes
  - `react-qr-code` — SVG-based QR rendering
  - `jsqr` — QR code decoding
- **Date Picker**: `react-datepicker`
- **Icons**: `react-icons`
- **Type Definitions**: `@types/react`, `@types/react-dom`, `@types/react-router-dom`
- **Development Tools**:
  - `vite` — Fast build tool
  - `eslint` — Linting
  - `tailwindcss` — Utility-first CSS
  - `typescript` — Static typing

### Backend Dependencies

The backend (`/backend`) is built using the following packages:

- **Prisma** (`@prisma/client`, `prisma`) — ORM for database access
- **SQLite** (`sqlite3`) — Lightweight database for development/testing
- **Express** — HTTP server framework
- **Middleware**:
  - `cors` — CORS policy configuration
  - `morgan` — Logging middleware
  - `multer` — File uploads
  - `express-jwt`, `jsonwebtoken` — Authentication with JWT
- **User Authentication**:
  - `bcrypt` — Password hashing
  - `uuid` — Unique identifier generation
- **Validation**: `zod` — Schema validation
- **Environment**: `dotenv` — Load `.env` variables


### Notes

-   Ensure that the API base URL in `.env` matches your backend deployment.

-   For production deployment, serve the contents of the `dist/` folder using a static file server (e.g., Nginx, Vercel, Netlify).

-   Tailwind CSS is used for styling, and React Router (v7) is used for routing.

-   This project uses Vite for fast bundling and optimized builds.
