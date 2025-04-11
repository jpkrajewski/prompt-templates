
# ⚙️ AI-Assisted Prompt Guide for Engineers
*Standardized prompts to streamline code generation, refactoring, and test writing across the engineering org.*

---

## 🔧 Refactoring Prompt Template

Use this to improve legacy code, increase maintainability, or prep for feature extension.

### ✅ Prompt Template
> "Refactor the following code to improve **readability**, **performance**, and **maintainability**. Preserve the existing logic and functionality. Follow best practices for **[language/framework]** and adhere to our internal coding guidelines.  
>  
> Make the code:  
> - Modular  
> - Testable  
> - Scalable  
> - Secure (if applicable)  
>  
> Also, provide a summary of the changes made and why."

```
[Insert code block here]
```

### 🛠 Optional Contextual Parameters:
- Type of system: [e.g., microservice, data pipeline, monolith, mobile app]
- Target environment: [e.g., serverless, containerized, edge computing]
- Constraints:
  - Avoid external libraries
  - Optimize for time/space complexity
  - Stick to ES6/Java 11/etc.
  - Ensure thread safety (for concurrent systems)
  - Comply with company security standards (e.g., input validation, sanitization)

---

## 🧱 Code Generation Prompt (Generic Feature/Task)

Use this to create new functions, services, modules, or logic blocks.

### ✅ Prompt Template
> "Write a clean, reusable, and well-documented code block to implement the following feature/task:  
>  
> **[Describe task clearly: inputs, outputs, behavior, edge cases]**  
>  
> Use **[language/framework]** and follow industry best practices and our team’s internal conventions. The code must be:  
> - Scalable  
> - Secure  
> - Performant  
> - Maintainable  
>  
> Add inline comments for clarity, handle edge cases, and include error handling."

```
[Insert task/feature description here]
```

### 🛠 Optional Contextual Parameters:
- Execution environment (e.g., frontend browser, backend API, AWS Lambda)
- Target platform (e.g., mobile, web, CLI, embedded)
- Expected usage volume (e.g., high traffic, batch job, one-off)
- Performance requirements (e.g., O(n), low-latency)
- Compatibility constraints (e.g., Node 18+, Android SDK 32)
- Expected integration points (e.g., Redis, Kafka, S3)

---

## ✅ Test Generation Prompt

Use this to write tests for new or legacy code. Can be used for unit, integration, or edge testing.

### ✅ Prompt Template
> "Generate comprehensive unit tests for the following code using **[testing framework]**.  
> Ensure the tests cover:  
> - Positive scenarios  
> - Negative scenarios  
> - Edge cases  
>  
> Include setup/teardown (if needed). Follow clear naming conventions and ensure each test has meaningful assertions and comments. Assume this is part of a CI pipeline for a production service."

```
[Insert code block here]
```

### 🛠 Optional Enhancements:
- Add mocking/stubbing using [mocking lib]
- Include test coverage targets (e.g., 90%+ line coverage)
- Make the test data realistic
- Flag potential integration dependencies (e.g., DB, external API)
- Ensure test idempotency and isolation

---

## 🔁 Refactor + Test Combo Prompt

Use this for full-cycle improvement of existing modules: clean it, test it, and ship confidently.

### ✅ Prompt Template
> "Refactor the following code to improve readability, modularity, and performance. Follow best practices for **[language/framework]** and ensure the code is production-ready.  
>  
> Then, generate a comprehensive suite of unit tests using **[testing framework]**. Include edge cases, mocks where needed, and explain the rationale for changes."

```
[Insert code block here]
```

### 🛠 Optional Parameters:
- Indicate if the code is legacy, experimental, or high-priority production
- Specify architectural goals (e.g., break monolith, enable parallelism)
- Include relevant performance benchmarks (if replacing a slow implementation)
- Security flags (e.g., sanitize input/output, protect against injection)

---

## 🧩 Pro Tips for Using These Prompts

- **Always include context**: AI performs better when it knows what the code is *for*.
- **Include constraints**: Language version, platform, style guide — the more, the better.
- **Review and validate**: AI is an assistant, not a replacement for engineering judgment.
- **Iterate**: Don’t be afraid to refine the prompt, rerun, and compare outcomes.

---

## 📄 Sample Usage (Markdown / Notion Snippet)

```markdown
#### Feature: Generate a pagination helper
Prompt:
Write a clean, reusable function to generate pagination metadata (current page, total pages, hasNext, hasPrev) based on the current offset, limit, and total count. Use JavaScript (ES6). No external libraries. Must handle edge cases like 0 results or very large datasets.

Expected:
- Pure function
- No side effects
- Well-commented
```
