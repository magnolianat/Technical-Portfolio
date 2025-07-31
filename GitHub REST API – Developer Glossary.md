# 📘 GitHub REST API – Developer Glossary

## 📑 Table of Contents
- [🔍 Access Token](#access-token)
- [🌐 API Endpoint](#api-endpoint)
- [🧩 Authentication](#authentication)
- [🗂️ Content-Type](#content-type)
- [🛠️ Curl](#curl)
- [🔐 OAuth App](#oauth-app)
- [📁 Repository](#repository)
- [🧾 Request](#request)
- [📦 Response](#response)
- [🧠 REST](#rest)
- [⏱️ Rate Limiting](#rate-limiting)
- [📬 Webhook](#webhook)

---

## 🔍 Access Token
A credential used to authenticate API requests on behalf of a user or an application. It can be a **Personal Access Token (PAT)** or an **OAuth token**.

---

## 🌐 API Endpoint
A specific URL path used to interact with GitHub resources.  
Example: `GET /repos/{owner}/{repo}` retrieves repository metadata.

---

## 🧩 Authentication
The process of verifying the identity of a user or app.  
GitHub supports Basic Auth, OAuth, and fine-grained Personal Access Tokens.

---

## 🗂️ Content-Type
An HTTP header specifying the data format being sent or expected.  
Example: `application/vnd.github+json`

---

## 🛠️ Curl
A command-line tool used to make HTTP requests.  
Commonly used to test API calls:  
```bash
curl -H "Authorization: Bearer <token>" https://api.github.com/user
