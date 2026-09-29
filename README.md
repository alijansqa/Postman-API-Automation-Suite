# Postman API Automation Suite - Library API

A comprehensive REST API automation test suite created in Postman to validate end-to-end CRUD workflows, schema assertions, query/path parameters, and environment variable chaining against `library-api.postmanlabs.com`.


## 🎯 Key Test Coverage

- **CRUD Operations**: Complete lifecycle testing covering resource creation (`POST`), retrieval (`GET`), partial update (`PATCH`), and cleanup (`DELETE`).
- **Query & Path Parameters**: Validated request filtering via single and multiple query parameters as well as dynamic path variables (`:id`).
- **Dynamic Variable Chaining**: Environment variable pass-through (`pm.environment.set` / `pm.environment.get`) to pass generated IDs between dependent endpoints seamlessly.
- **JavaScript Assertions**:
  - **Status Code Checks**: Verified `200 OK`, `201 Created`, and error routes.
  - **Data Structure Validation**: Handled distinct schema shapes (JSON Objects vs. JSON Arrays).
  - **Array & Object Verification**: Iterative property checks (`.forEach()`) and conditional presence checks (`.some()`).
  - **Performance Benchmarks**: Response time assertions evaluating server processing limits (`pm.response.responseTime`).
- **Negative Testing**: Included unsupported HTTP methods (`PUT`) to verify proper error responses and API routing stability.

## 📁 Collection Breakdown

1. **Base & Parameterized Filtering**: `GET Base API`, Single/Multi Query Params, Path Variables.
2. **Resource Creation & State Management**: `POST` endpoints saving dynamic properties (`id2`) into environment scope.
3. **Resource Manipulation & Validation**: `PATCH` updates and verification fetches on created records.
4. **Teardown & Specialized Assertions**: `DELETE` verification, array-level data integrity tests, and response speed benchmarks.

## 🚀 How to Run

1. Clone or download this repository.
2. Open **Postman**.
3. Import `Books API Collection.json` into Collections.
4. Import `Postman Practices.json` into Environments.
5. Select the **Postman Practices** environment in the top-right environment selector.
6. Open **Collection Runner**, select the `Books` collection, and click **Run Books**.






