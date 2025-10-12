### **RAVO: Robust And Versatile Operation for RDB**

금융권과 같이 비즈니스 연속성이 필수적인 K-PaaS 환경에서, RDB 서비스의 가용성을 극대화하고 데이터 정합성을 보장하는 자동화 솔루션입니다.

### **Key Features**

* **실시간 데이터 동기화 및 백업**
    * **CDC 기반 복제**: `Debezium`과 `Kafka`를 활용하여 Active DB의 모든 데이터 변경 사항을 Standby DB로 실시간 반영합니다.
    * **안정성 강화**: 정기적인 콜드 백업(Cold Backup)을 병행하여 데이터 보존 신뢰도를 높입니다.

* **자동 장애 감지 및 복구**
    * **즉시 감지**: 자체 구현한 **`Failover Watcher`**가 Active DB의 장애를 신속하게 감지합니다.
    * **다운타임 최소화**: 장애 발생 시 자동으로 Standby DB로 서비스를 전환하여 서비스 중단을 최소화합니다.

* **데이터 정합성 보장**
    * **변경 이력 추적**: **`GTID`**가 적용된 Standby DB의 `binlog`를 통해 Failover 중 발생한 모든 데이터 변경분을 추적합니다.
    * **역방향 동기화**: 기존 Active DB 복구 시, 추적된 변경분을 다시 동기화하여 데이터의 정합성을 보장합니다.
