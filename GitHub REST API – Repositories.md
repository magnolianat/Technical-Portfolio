# GitHub REST API – Repositories Endpoint Documentation

**Base URL:** `https://api.github.com`  
**Authentication:** Personal access token (via headers)  
**Format:** JSON  
**Version:** v3 (Latest)

---

## 🔐 Authentication

All requests must include an `Authorization` header with a valid GitHub token:

```
Authorization: Bearer YOUR_GITHUB_TOKEN
Accept: application/vnd.github+json
```

---

## 📘 Endpoint: List User Repositories

**GET** `/users/{username}/repos`

### Description  
Returns a list of public repositories for the specified user.

### Parameters  
| Name     | Type   | Required | Description                          |
|----------|--------|----------|--------------------------------------|
| username | string | Yes      | The GitHub username                  |
| type     | string | No       | all, owner, member (default: owner)  |
| sort     | string | No       | created, updated, pushed, full_name  |
| per_page | int    | No       | Number of results per page (max 100) |

### Example Request  
```
GET /users/octocat/repos
```

### Example Response  
```json
[
  {
    "id": 1296269,
    "name": "Hello-World",
    "full_name": "octocat/Hello-World",
    "private": false,
    "owner": {
      "login": "octocat"
    },
    "html_url": "https://github.com/octocat/Hello-World",
    "description": "This your first repo!",
    "fork": false
  }
]
```

---

## 📘 Endpoint: Create a Repository

**POST** `/user/repos`

### Description  
Creates a new repository for the authenticated user.

### Request Body  
| Name        | Type    | Required | Description                       |
|-------------|---------|----------|-----------------------------------|
| name        | string  | Yes      | Name of the repository            |
| description | string  | No       | Description of the repository     |
| private     | boolean | No       | true for a private repository     |

### Example Request  
```json
POST /user/repos
{
  "name": "my-new-repo",
  "description": "API-created repo",
  "private": false
}
```

### Example Response  
```json
{
  "id": 123456789,
  "name": "my-new-repo",
  "full_name": "your-username/my-new-repo",
  "private": false,
  "html_url": "https://github.com/your-username/my-new-repo"
}
```

---

## 📘 Endpoint: Delete a Repository

**DELETE** `/repos/{owner}/{repo}`

### Description  
Deletes a repository owned by the authenticated user.

### Example Request  
```
DELETE /repos/your-username/my-old-repo
```

### Response  
- **204 No Content** if successful  
- **404 Not Found** if the repository does not exist

---

## 📚 Additional Resources
- [GitHub REST API Docs](https://docs.github.com/en/rest)


[Back to Index](https://github.com/magnolianat/Technical-Portfolio/blob/main/Technical%20Writing%20Portfolio%20Index.md)
- [Personal Access Tokens](https://github.com/settings/tokens)

