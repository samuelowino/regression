# Regression
A Spring Boot server for collecting, storing, and analyzing error logs with REST APIs and AI-powered log analysis

### **Regression – Requirements Specification**

**Overview:**
**Regression** is a Spring Boot-based server for collecting, storing, and analyzing application error logs. It provides RESTful APIs for log ingestion and retrieval, with AI-driven analysis to detect anomalies, trends, and root causes.

### **Functional Requirements:**

1. **Log Ingestion API**

   * Accept error logs in JSON format via HTTP POST.
   * Support metadata: timestamp, severity, application ID, source, etc.

2. **Log Storage**

   * Persist logs in a scalable database (e.g., PostgreSQL, MongoDB).
   * Index logs for fast search and filtering.

3. **Log Retrieval API**

   * Fetch logs via GET endpoints with filters (time range, severity, keyword).

4. **AI-Powered Analysis**

   * Analyze logs using machine learning models to:

     * Detect anomalies and outliers.
     * Group similar error patterns.
     * Suggest probable root causes.

5. **Authentication & Authorization**

   * Secure API endpoints using JWT or OAuth2.
   * Role-based access control (e.g., viewer, admin).

6. **Monitoring & Metrics**

   * Expose system metrics (e.g., log rate, error types) via an endpoint (e.g., `/metrics`).

---

### **Non-Functional Requirements:**

* **Performance:** Handle high log volumes with minimal latency.
* **Scalability:** Support containerized deployment and clustering.
* **Extensibility:** Pluggable architecture for custom AI models or storage backends.
* **Reliability:** Fault-tolerant with retries and backup mechanisms.





<!-- coverage start -->
## 📊 Code Coverage Report

**Overall Coverage: 100.00% ✅**

| Metric      | Covered | Missed | Total | Coverage  |
|-------------|---------|--------|-------|-----------|
| INSTRUCTION | 20      | 0      | 20    | 100.00% ✅ |
| LINE        | 5       | 0      | 5     | 100.00% ✅ |
| BRANCH      |         |        | 0     | 0% ⚠️     |
| METHOD      | 4       | 0      | 4     | 100.00% ✅ |
| CLASS       | 2       | 0      | 2     | 100.00% ✅ |
| COMPLEXITY  | 4       | 0      | 4     | 100.00% ✅ |

### 🚨 Least Tested Elements (coverage below 50%)
- BRANCH: 0%
<!-- coverage end -->
