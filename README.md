# 🧪 API Tests with Newman (GitHub Actions CI/CD)

This project shows how to automate **API testing** using **Newman** (Postman’s CLI tool) and **GitHub Actions** for a simple CI/CD setup.
Whenever new code is pushed or a pull request is made to the `main` branch, this workflow automatically runs the API tests and creates a detailed **HTML report**.

---

## 🚀 What This Workflow Does

1. **Checks out the repository** – gets the latest version of the project.
2. **Sets up Node.js** – installs version 18 (required for Newman).
3. **Installs Newman and HTML reporter** – tools used for running and reporting API tests.
4. **Runs the tests** – executes the Postman collection using an environment file.
5. **Generates a report** – creates a visual HTML test report.
6. **Uploads the report** – saves the report as an artifact in GitHub Actions.

---

## ⚙️ When It Runs

The workflow triggers automatically:

* On every **push** to the `main` branch
* On every **pull request** to the `main` branch

This helps ensure all APIs are tested before merging or deploying new changes.

---

## 🧩 Folder Structure

```
project-root/
│
├── api-tests/
│   ├── collection.json          # Postman collection file
│   └── environment.json         # Postman environment file
│
├── .github/
│   └── workflows/
│       └── api-tests.yml        # CI/CD workflow file
│
└── README.md
```

---

## 📊 What You’ll Get After Each Run

* **Console log** – test summary directly inside GitHub Actions
* **HTML report** – detailed test results available for download as an artifact

---

## 🧠 Why It’s Useful

* Automates API testing in the CI/CD pipeline
* Catches issues early during development
* Saves time on manual test execution
* Generates a clear, shareable report of all test results

---

## 🛠️ Tools Used

* **Postman / Newman** – for API testing
* **GitHub Actions** – for automation and CI/CD
* **Node.js** – required runtime for Newman
* **HTML Extra Reporter** – for better test visualization

---

## 💡 How to Run Locally

You can also run the same tests manually with:

```bash
npm install -g newman newman-reporter-htmlextra
newman run ./api-tests/collection.json \
  -e ./api-tests/environment.json \
  -r cli,htmlextra \
  --reporter-htmlextra-export ./newman/newman-report.html
```

This will create an HTML report in the `/newman` folder.

---

## 📚 Summary

This project is a simple example of **how to integrate API testing with CI/CD** using GitHub Actions.
It helps maintain API reliability, gives faster feedback to developers, and adds automation skills to your QA or DevOps portfolio.

---

**Created by:** Dilruba Khanam Jesey
**Focus:** API Testing | Automation | GitHub Actions | CI/CD | Newman

---
