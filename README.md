
# Cypress E2E Testing Project

This project contains end-to-end (E2E) tests for a web application using [Cypress](https://www.cypress.io/), the Page Object Model (POM) design pattern, and [Mochawesome](https://www.npmjs.com/package/mochawesome) as the test reporter.

---

## 📂 **Project Structure**

```
├── cypress/
│   ├── e2e/                # Test cases
│   ├── fixtures/           # Test data (e.g., JSON files)
│   ├── pages/              # Page Object Model (POM) files
│   ├── support/            # Cypress custom commands and configurations
│   └── reports/            # Generated Mochawesome reports
├── node_modules/           # Project dependencies
├── .gitignore              # Files and folders to ignore in version control
├── cypress.config.js       # Cypress configuration
├── package.json            # Project metadata and dependencies
├── README.md               # Project documentation
└── package-lock.json       # Dependency lock file
```

---

## 🚀 **Getting Started**

### **1. Prerequisites**
- Node.js (v14 or later)
- npm or yarn
- A modern web browser (Chrome or Edge)

### **2. Installation**
1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd <project-directory>
   ```
2. Install dependencies:
   ```bash
   npm install
   ```

### **3. Running Tests**
- To run all tests in headless mode:
  ```bash
  npx cypress run
  ```
- To run tests in the Cypress Test Runner:
  ```bash
  npx cypress open
  ```

### **4. Generating Reports**
- After running the tests, Mochawesome reports will be generated in the `cypress/reports/` directory.

---

## 🛠️ **Configuration**

### **Cypress Configuration (cypress.config.js)**
You can modify test configurations in the `cypress.config.js` file. Key settings include:
- Base URL
- Default timeouts
- Integration folder for test cases

### **Mochawesome Reporter**
The Mochawesome configuration is included in the `package.json`:
```json
"mocha": {
  "reporter": "mochawesome",
  "reporterOptions": {
    "reportDir": "cypress/reports",
    "overwrite": false,
    "html": true,
    "json": true
  }
}
```

---

## 🔍 **Test Reporting**

### **Viewing Mochawesome Reports**
1. After running tests, reports are generated in `cypress/reports/`.
2. Open the `mochawesome.html` file in your browser to view the detailed test results.

---

## ✅ **Best Practices**
- Use descriptive test names.
- Keep page objects simple and reusable.
- Utilize Cypress's built-in commands like `cy.intercept()` for mocking API calls.
- Organize test data in the `fixtures/` folder.

---
