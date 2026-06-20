# API Documentation

## Overview

KnowledgeForge AI provides document ingestion, semantic retrieval, and context-aware response generation through Django-based endpoints.

---

## Home Page

| Property    | Value        |
| ----------- | ------------ |
| Endpoint    | `/`          |
| Method      | GET          |
| Description | Landing page |

---

## User Registration

| Property    | Value              |
| ----------- | ------------------ |
| Endpoint    | `/Register.html`   |
| Method      | GET / POST         |
| Description | Register new users |

---

## User Login

| Property    | Value              |
| ----------- | ------------------ |
| Endpoint    | `/UserLogin.html`  |
| Method      | GET / POST         |
| Description | Authenticate users |

---

## Document Upload

| Property    | Value                             |
| ----------- | --------------------------------- |
| Endpoint    | `/UploadDocument.html`            |
| Method      | POST                              |
| Description | Upload PDF documents for indexing |

### Request

```text
PDF Document
```

### Response

```json
{
  "status": "success",
  "message": "Document uploaded successfully"
}
```

---

## Document Retrieval

| Property    | Value                       |
| ----------- | --------------------------- |
| Endpoint    | `/Retrieval.html`           |
| Method      | POST                        |
| Description | Semantic document retrieval |

### Request

```json
{
  "query": "stop algorithm"
}
```

---

## Text Generation

| Property    | Value                                     |
| ----------- | ----------------------------------------- |
| Endpoint    | `/Generation.html`                        |
| Method      | POST                                      |
| Description | Generate contextual answers using Llama 2 |

### Request

```json
{
  "query": "What is Task Decomposition?"
}
```

### Response

```json
{
  "answer": "Generated response based on retrieved context."
}
```

---

## Error Handling

| Code | Meaning               |
| ---- | --------------------- |
| 200  | Success               |
| 400  | Invalid Request       |
| 401  | Unauthorized          |
| 404  | Resource Not Found    |
| 500  | Internal Server Error |

---

## Future API Enhancements

* REST API Support
* JWT Authentication
* OpenAPI Specification
* Swagger Documentation
* API Gateway Integration

