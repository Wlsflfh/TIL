---
id: "980BED9A-A216-4F27-9D9D-C57BA44F7F4E"
date: "2026-06-22"
title: "MySQL의 트랜잭션 격리 수준"
---

## MySQL 트랜잭션 격리 수준을 설명해주세요

MySQL의 트랜잭션 격리 수준은 동시에 여러 트랜잭션이 실행될 때 서로의 작업을 어느 정도까지 볼 수 있는지를 정하는 기준입니다.

격리 수준은 낮은 순서대로 Read Uncommitted, Read Committed, Repeatable Read, Serializable이 있습니다. Read Uncommitted는 커밋되지 않은 데이터도 읽을 수 있고, Read Committed는 커밋된 데이터만 읽습니다. Repeatable Read는 같은 트랜잭션 안에서 같은 데이터를 반복 조회해도 동일한 결과를 보장합니다. Serializable은 가장 강한 격리 수준으로 트랜잭션을 거의 순차적으로 실행하는 것처럼 처리하지만 성능 부담이 큽니다.

MySQL InnoDB의 기본 격리 수준은 Repeatable Read입니다.