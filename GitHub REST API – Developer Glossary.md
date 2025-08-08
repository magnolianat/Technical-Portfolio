# 📘 GitHub REST API – Developer Glossary #

## 📑 Table of Contents

- [🔍 Access Token](#-access-token)
- [🌐 API Endpoint](#-api-endpoint)
- [🧩 Authentication](#-authentication)
- [🗂️ Content-Type](#-content-type)
- [🛠️ Curl](#-curl)
- [🔐 OAuth App](#-oauth-app)
- [📁 Repository](#-repository)
- [🧾 Request](#-request)
- [📦 Response](#-response)
- [🧠 REST](#-rest)
- [⏱️ Rate Limiting](#-rate-limiting)
- [📬 Webhook](#-webhook)
- [📚 References](#-references)

---

## 🔍 Access Token

A credential used to authenticate API requests on behalf of a user or an application.  
It can be a **Personal Access Token (PAT)** or an **OAuth token**.

---

## 🌐 API Endpoint

A specific URL path used to interact with GitHub resources.  
Example:  
`GET /repos/{owner}/{repo}` retrieves repository metadata.

---

## 🧩 Authentication

The process of verifying the identity of a user or app.  
GitHub supports Basic Auth, OAuth, and Personal Access Tokens.

---

## 🗂️ Content-Type

An HTTP header specifying the data format being sent or expected.  
Example:  
`application/vnd.github+json`

---

## 🛠️ Curl

A command-line tool used to make HTTP requests.  
Commonly used to test API calls:

```bash
curl -H "Authorization: Bearer <token>" https://api.github.com/user
```
---

## 🔐 OAuth App

An app that authenticates users via GitHub’s OAuth 2.0 flow.  
Enables scoped, user-consented access to GitHub APIs.

---

## 📁 Repository

A GitHub repository contains all of a project's files and revision history.  
Core resource used in most API interactions.

---

## 🧾 Request

An API operation made by the client, defined by:

- **Method**: GET, POST, PUT, DELETE  
- **Headers**: e.g., Authorization  
- **Body**: JSON payload (optional)

---

## 📦 Response

The server’s reply to a request. Includes:

- **Status code** (e.g., 200, 404, 403)  
- **Response body** (typically in JSON)  
- **Headers** (e.g., RateLimit info)

---

## 🧠 REST

**Representational State Transfer**: an architecture style that defines constraints for building web services via standard HTTP methods.

---

## ⏱️ Rate Limiting

GitHub limits the number of API requests per hour:

- **Authenticated**: up to 5,000/hour  
- **Unauthenticated**: 60/hour  

Check headers like `X-RateLimit-Remaining`.

---

## 📬 Webhook

An HTTP callback triggered by GitHub events (e.g., pushes, pull requests).  
Used for automation, CI/CD, notifications, etc.

Example payload:

```json
{
  "action": "push",
  "repository": {
    "name": "my-repo"
  }
}
```
## 📚 References

- [GitHub REST API Docs](https://docs.github.com/en/rest)  
- [Personal Access Tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/personal-access-tokens)  
- [GitHub Webhooks](https://docs.github.com/en/webhooks)

[Back to Index](https://github.com/magnolianat/Technical-Portfolio/blob/main/Technical%20Writing%20Portfolio%20Index.md)

