# 4. Testing ProWriterSite API with Postman

This section walks you through testing the ProWriterSite API using **Postman**, a popular API client.

---

## 🧾 Setup Instructions

1. **Install Postman:**  
   Download from [https://www.postman.com/downloads/](https://www.postman.com/downloads/)

2. **Set Base URL:**  

https://api.prowritersites.dev/v1


3. **Authentication:**  
Go to the "Authorization" tab and select:
- **Type:** Bearer Token  
- **Token:** `YOUR_ACCESS_TOKEN`

---

##   Testing Endpoints

###  GET /writers

- **Method:** GET  
- **URL:** `https://api.prowritersites.dev/v1/writers`  
- **Auth:** Bearer Token  
- **Expected Result:** List of writer profiles in JSON format.

---

###  GET /writers/{id}

- **Method:** GET  
- **URL:** `https://api.prowritersites.dev/v1/writers/w123`  
- **Expected Result:** JSON response with writer details.

---

###  POST /clients/requests

- **Method:** POST  
- **URL:** `https://api.prowritersites.dev/v1/clients/requests`  
- **Body (raw, JSON):**

```json
{
"title": "Blog Writing for Tech Product",
"description": "Need a technical blog on AI-powered tools",
"budget": 150,
"deadline": "2025-06-10"
}

Expected Result:
HTTP 201 with a success message or request ID.

Tips:
- Use Collections to group and save requests.
- Use Environment Variables for token and base URL reuse.
- Explore Tests tab to write simple scripts to validate responses.


