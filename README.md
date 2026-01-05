# interview-cheatsheet
# 📅 KẾ HOẠCH ÔN TẬP 7 NGÀY CHI TIẾT

## 📌 NGÀY 1 --- SPRING BOOT (core bắt buộc cho senior)

### 1. Review các chủ đề:

-   Sự khác nhau giữa:
    -   `@Component` vs `@Service` vs `@Repository`
    -   `@Autowired` vs constructor injection
-   Bean lifecycle --- thực tế interviewer rất thích hỏi
-   Spring MVC core:
    -   Filter vs Interceptor
    -   ExceptionHandler best practice
-   Actuator
-   ConfigurationProperties

### 2. Bài tập tối thiểu:

-   Tự code 1 API CRUD + exception global + interceptor + actuator
-   20 câu hỏi Spring Boot (mình sẽ soạn nếu bạn muốn)

------------------------------------------------------------------------

## 📌 NGÀY 2 --- MICROSERVICES & DISTRIBUTED SYSTEMS

### Concepts phải nắm:

-   API Gateway pattern
-   Saga pattern (chỉ cần hiểu concept + use case)
-   Event-driven vs Request-driven
-   Idempotency (rất hay bị hỏi!)
-   Rate limiting
-   Circuit breaker (Resilience4J)
-   Retry with backoff
-   Distributed lock (Redis / DynamoDB TTL)

### Bài tập:

-   Mô tả 1 use-case event-driven mà bạn từng làm (Kinesis/SQS)
-   Chuẩn bị 3 ví dụ lỗi hệ thống và cách bạn fix.

------------------------------------------------------------------------

## 📌 NGÀY 3 --- AWS (đúng trọng tâm CV của bạn)

### Phải chắc chắn:

-   ECS Fargate vs Lambda -- dùng khi nào?
-   DynamoDB best practices:
    -   Partition key
    -   GSIs
    -   Hot partition
    -   Throttling
-   SQS vs SNS vs Kinesis -- phân biệt thật sắc nét
-   IAM: policy → role → trust

### Real-world question:

-   "Làm sao để scale một service đang chạy trên ECS khi TPS tăng bất
    ngờ?"
-   "Làm sao để tránh DynamoDB hot partition?"

------------------------------------------------------------------------

## 📌 NGÀY 4 --- JAVA & CODING

### Java topics nên ôn:

-   Immutable class
-   ConcurrentHashMap + concurrency levels
-   CompletableFuture (quan trọng!)
-   ThreadPoolExecutor params
-   Stream API pitfalls
-   JVM memory model + GC (G1GC cơ bản)

### Coding tối thiểu:

-   Reverse linked list
-   Two pointer
-   Map/Set problems
-   Basic string manipulation
-   LRU cache (concept)
-   Thread-safe counter

⛔ Bạn không cần leetcode hard, chỉ cần trả lời mượt + code sạch.

------------------------------------------------------------------------

## 📌 NGÀY 5 --- SYSTEM DESIGN (senior bắt buộc)

### Topics chính:

-   Load balancing (round robin vs consistent hashing)
-   Caching strategies:
    -   Cache aside
    -   Write-through
    -   Write-back
-   Message queue
-   Database sharding vs replication
-   Event-driven architecture
-   High availability vs scalability

### Bài tập:

Thiết kế 1 hệ thống đơn giản nhưng chắc: - Notification system - Log
ingestion system - Order service (Saga + timeout)

------------------------------------------------------------------------

## 📌 NGÀY 6 --- BEHAVIORAL (TĂNG TỶ LỆ PASS TUYỆT ĐỐI)

### Dành cho các câu phỏng vấn:

-   "Tell me about yourself"
-   "Dự án khó nhất bạn từng làm?"
-   "Một lần bạn fail?"
-   "Bạn xử lý conflict trong team thế nào?"
-   "Bạn đã leadership như thế nào?"

### Template STAR + Impact:

-   **S (situation):** Microservice đang bị tăng latency lên 600ms\
-   **T (task):** Tôi chịu trách nhiệm phân tích root cause\
-   **A (action):**
    -   Log correlation ID\
    -   Tracing distributed\
    -   Làm heatmap DynamoDB partition\
-   **R (result):** Giảm latency từ 600ms → 120ms, ổn định ở peak 30k
    RPM.

------------------------------------------------------------------------

## 📌 NGÀY 7 --- MOCK INTERVIEW FULL

### Buổi luyện mock sẽ gồm:

-   10 câu Spring Boot\
-   10 câu Distributed Systems\
-   10 câu AWS\
-   1 bài Design nhỏ\
-   2 câu coding cơ bản\
-   5 câu behavioral
