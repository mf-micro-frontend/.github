# MF Micro Frontend

This organization contains a micro frontend architecture for an e-commerce platform focused on selling books. The project uses React, Vite, and Module Federation to create independently deployable applications.

## Features
- **Host App (React):**
  - Provides a shared header and footer.
  - Manages global state via `GlobalContext`.
  - Imports and integrates all micro frontends.
  
- **Books List App (React):**
  - Fetches and displays a list of programming books.
  - Allows users to select a book to view more details or add to a cart.

- **Single Book App (React):**
  - Displays details of a selected book.
  - Allows users to add the book/books to the cart.
 
- **Shared App (React):**
  - Stores and exporters shared components(Button, Search) used by other mfs.

## 🚀 Technologies Used

- **React** - Frontend framework for all micro frontends.
- **Vite** - Build tool for fast development and optimized production builds.
- **Module Federation** - Enables independent deployment and dynamic imports of micro frontends.
- **Context API** - Used for global state management across micro frontends.

## 🛠 Installation & Setup

### Clone the repositories:
```sh
git clone https://github.com/mf-micro-frontend/host-react.git
git clone https://github.com/mf-micro-frontend/book-list-react.git
git clone https://github.com/mf-micro-frontend/single-book-react.git
git clone https://github.com/mf-micro-frontend/shared-react.git
```

### Install dependencies for each repository:
```sh
pnpm install 
```

### Environment Variables
Each micro frontend requires a `.env` file in its root directory. Below is an example `.env` file:
```sh
VITE_HOST_APP_URL=http://localhost:5001
VITE_BOOK_LIST_APP_URL=http://localhost:5002
VITE_SINGLE_BOOK_APP_URL=http://localhost:5003
VITE_SHARED_APP_URL=http://localhost:5099
```
Ensure you configure these appropriately for local development.

### Run each application:
```sh
pnpm run start-mf
```

Ensure all micro frontends are running and available for the host app to load.

## 🤝 Contribution
1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m "Add feature"`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.

## 📜 License

This project is licensed under the [MIT License](LICENSE).

