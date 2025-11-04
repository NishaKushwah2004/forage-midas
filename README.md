# Midas Core — J.P. Morgan Software Engineering Simulation

## Overview  
- This repository is the codebase for the J.P. Morgan Software Engineering simulation. It demonstrates a small Spring Boot application that ingests transaction feeds (via Kafka), updates user balances (SQL-backed), and exposes a REST endpoint to query balances.
- This simulation gave me hands-on experience with real-world tasks in a financial tech setting. Despite being new to debugging, Spring Boot, Kafka, H2 database, and Maven, I challenged myself to complete the project and learned a lot along the way.


## Tech Stack & Tools  
- Spring Framework (Spring Boot)
- Java (Java 17)
- Build tools: Maven
- Message queueing: Apache Kafka (embedded for tests)
- REST API (balance endpoint)
- SQL database (JPA entities / in-memory DB for tests)
- Testing with JUnit and Embedded Kafka


## Completion date
- 29 Sept


## How to run (quick)
- Build and run tests with the Maven wrapper:
  - ./mvnw test
  - On Windows: mvnw.cmd test
- The verification tests are under src/test/java and include interactive tests that publish transactions and expect you to inspect results via the REST endpoint or debugger.


## What I Built  
- Set up a local dev environment  
- Parsed and processed financial data feeds  
- Built a dynamic dashboard using JPMorgan’s Perspective library  
- Worked with API contracts and data visualization  
- Navigated unfamiliar tools and debugging challenges


## What I Learned  
- How to troubleshoot and debug with limited prior experience  
- Importance of clean architecture and decoupling  
- Basics of backend orchestration and endpoint reliability  
- Confidence in learning new tools under pressure


## Important files & entry points
- **Application entry**: [`com.jpmc.midascore.MidasCoreApplication`](src/main/java/com/jpmc/midascore/MidasCoreApplication.java) — [src/main/java/com/jpmc/midascore/MidasCoreApplication.java](src/main/java/com/jpmc/midascore/MidasCoreApplication.java)
- **Kafka producer (test helper)**: [`com.jpmc.midascore.KafkaProducer`](src/test/java/com/jpmc/midascore/KafkaProducer.java) — [src/test/java/com/jpmc/midascore/KafkaProducer.java](src/test/java/com/jpmc/midascore/KafkaProducer.java)
- **Domain models:**
  - [`com.jpmc.midascore.foundation.Transaction`](src/main/java/com/jpmc/midascore/foundation/Transaction.java) — [src/main/java/com/jpmc/midascore/foundation/Transaction.java](src/main/java/com/jpmc/midascore/foundation/Transaction.java)
  - [`com.jpmc.midascore.foundation.Balance`](src/main/java/com/jpmc/midascore/foundation/Balance.java) — [src/main/java/com/jpmc/midascore/foundation/Balance.java](src/main/java/com/jpmc/midascore/foundation/Balance.java)
- **Persistence:**
  - Entity: [`com.jpmc.midascore.entity.UserRecord`](src/main/java/com/jpmc/midascore/entity/UserRecord.java) — [src/main/java/com/jpmc/midascore/entity/UserRecord.java](src/main/java/com/jpmc/midascore/entity/UserRecord.java)
  - Repository: [`com.jpmc.midascore.repository.UserRepository`](src/main/java/com/jpmc/midascore/repository/UserRepository.java) — [src/main/java/com/jpmc/midascore/repository/UserRepository.java](src/main/java/com/jpmc/midascore/repository/UserRepository.java)
  - DB conduit: [`com.jpmc.midascore.component.DatabaseConduit`](src/main/java/com/jpmc/midascore/component/DatabaseConduit.java) — [src/main/java/com/jpmc/midascore/component/DatabaseConduit.java](src/main/java/com/jpmc/midascore/component/DatabaseConduit.java)
- **Test utilities:**
  - [`com.jpmc.midascore.FileLoader`](src/test/java/com/jpmc/midascore/FileLoader.java) — [src/test/java/com/jpmc/midascore/FileLoader.java](src/test/java/com/jpmc/midascore/FileLoader.java)
  - [`com.jpmc.midascore.UserPopulator`](src/test/java/com/jpmc/midascore/UserPopulator.java) — [src/test/java/com/jpmc/midascore/UserPopulator.java](src/test/java/com/jpmc/midascore/UserPopulator.java)
  - [`com.jpmc.midascore.BalanceQuerier`](src/test/java/com/jpmc/midascore/BalanceQuerier.java) — [src/test/java/com/jpmc/midascore/BalanceQuerier.java](src/test/java/com/jpmc/midascore/BalanceQuerier.java)
- **Verification / tasks:**
  - [`TaskOneTests`](src/test/java/com/jpmc/midascore/TaskOneTests.java) — [src/test/java/com/jpmc/midascore/TaskOneTests.java](src/test/java/com/jpmc/midascore/TaskOneTests.java)
  - [`TaskTwoTests`](src/test/java/com/jpmc/midascore/TaskTwoTests.java) — [src/test/java/com/jpmc/midascore/TaskTwoTests.java](src/test/java/com/jpmc/midascore/TaskTwoTests.java)
  - [`TaskThreeTests`](src/test/java/com/jpmc/midascore/TaskThreeTests.java) — [src/test/java/com/jpmc/midascore/TaskThreeTests.java](src/test/java/com/jpmc/midascore/TaskThreeTests.java)
  - [`TaskFourTests`](src/test/java/com/jpmc/midascore/TaskFourTests.java) — [src/test/java/com/jpmc/midascore/TaskFourTests.java](src/test/java/com/jpmc/midascore/TaskFourTests.java)
  - [`TaskFiveTests`](src/test/java/com/jpmc/midascore/TaskFiveTests.java) — [src/test/java/com/jpmc/midascore/TaskFiveTests.java](src/test/java/com/jpmc/midascore/TaskFiveTests.java)
- **Project build:** [pom.xml](pom.xml)
- **Test data:** [src/test/resources/test_data](src/test/resources/test_data)

Notes
- Some tests intentionally pause and require using a debugger or the REST endpoint to retrieve answers; check the task test classes above.
- The repository is small and intended for learning/debugging Spring, Kafka, JPA, and REST interactions.


## 👩‍💻 Author
**Nisha Kushwah**  
B.Tech in Computer Science & Engineering  
Jabalpur Engineering College  
📧 [2004nishakushwah@gmail.com](mailto:2004nishakushwah@gmail.com)  
🌐 [GitHub Profile](https://github.com/NishaKushwah2004)
