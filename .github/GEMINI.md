# Repository AI Instructions

## 🏗 Tech Stack
- **Backend:** Java 21, Spring Boot 3.2+
- **Database:** Spring Data JPA, PostgreSQL
- **Infrastructure:** Docker, GitHub Actions

## 📏 Coding Standards
- Use Java `record` types for DTOs.
- Constructor injection via Lombok `@RequiredArgsConstructor`.
- Adhere to `jakarta.validation` constraints for input.
- Use `FetchType.LAZY` for JPA relationships.

## 🔍 AI Reviewer Responsibilities
- **Implementation:** Verify logic against PR descriptions and Java 21 idioms.
- **Testing:** Check for JUnit 5/AssertJ and appropriate test slices (e.g., `@DataJpaTest`).
- **Architecture:** Ensure strict Controller -> Service -> Repository separation.
- **Security:** Scan for SQL injection in JPQL and proper Spring Security usage.
- **DevOps:** Review Dockerfile and Workflow efficiency.
- **Final Review:** Provide a summary of merge readiness.

## 📝 Review Output Format
- Provide clear, actionable feedback with code suggestions.
- **Severities:**
  - `🔴 Critical`: Bugs/Security issues.
  - `🟠 High`: Performance/Architecture issues.
  - `🟡 Medium`: Missing tests/Standard violations.
  - `🟢 Low`: Style/Typos.