# React Book Management App

A modern, responsive book management dashboard built with React and Material-UI. This application allows users to browse book collections and categories through a clean, administrative interface.

## 🚀 Features

- **Dynamic Data Fetching:** Integrates with a REST API to retrieve and display books and categories.
- **Material Design:** Built using `material-ui` for a professional and consistent user experience.
- **Client-Side Routing:** Powered by `react-router-dom` for seamless transitions between Books and Categories views.
- **Modular Architecture:** Structured with reusable layout components including SideBar, Header, and Content Area.
- **Dashboard Utilities:** Prepared with a suite of plugins (Bootstrap, Chart.js, DataTables) for future administrative expansions.

## 🛠️ Tech Stack

- **Frontend:** React 16
- **Styling/UI:** Material-UI (v0.19)
- **Routing:** React Router 4
- **Build Tool:** React Scripts (Create React App)
- **External Dependencies:** Managed via npm and bower

## 📥 Getting Started

AI coding assistants can use [AGENTS.md](AGENTS.md) for quick setup and workflow guidance.

### Prerequisites

- Node.js (v8+ recommended for React 16 compatibility)
- npm or yarn
- A backend API server running at `http://localhost:4000` (e.g., `json-server`)

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd react-books-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the application:
   ```bash
   npm start
   ```

The app will be available at `http://localhost:3000`.

## 📂 Project Structure

```text
src/
├── layouts/            # Reusable UI layout components
│   ├── Header.js
│   ├── SideBar.js
│   ├── ContentArea.js
│   └── Footer.js
├── App.js              # Main application container
├── index.js            # Entry point and routing configuration
├── Item.js             # Data fetching container component
└── ItemList.js         # Presentation component for data tables
```

## 📡 API Integration

The application expects a RESTful backend. By default, it attempts to fetch data from:
- `http://localhost:4000/books`
- `http://localhost:4000/categories`

Ensure your backend provides JSON responses with the following structure for books:
```json
[
  {
    "id": 1,
    "title": "Example Book",
    "author": "John Doe"
  }
]
```

## 📄 License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.
