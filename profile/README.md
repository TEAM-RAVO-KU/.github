### **RAVO: Robust And Versatile Operation for RDB**

R&D 서비스 안정성 및 가용성 혁신을 위한 자동화된 DB Distaster Recovery 솔루션

### **Key Features**

- Live Sync
  - Debezium과 Kafka 기반의 CDC 기술을 활용하여 Active DB의 변경 내역을 Standby DB로 실시간 복제합니다.
  - 이를 통해 장애 발생 시점의 RPO을 최소화하고 두 DB 간의 Live Sync를 보장합니다.

- Auto-Failover
  - 자체 구현한 RAVO-AGENT가 Active DB의 장애를 즉각적으로 감지하여 서비스 트래픽을 Standby DB로 자동 전환합니다.
  - Kubernetes Service 리소스를 자동으로 제어하여 RTO를 최소화합니다.

- Auto-Recover
  - 기존 Active DB가 복구되면, 장애 동안 Standby DB에 쌓인 변경 내역을 GTID 기반으로 추적하여 역방향 동기화를 수행합니다.
  - 데이터 정합성을 보장한 후, 서비스 트래픽을 다시 Active DB로 자동 복구시킵니다.

- Dispersion Backup
  - Active DB가 위치한 클러스터와 물리적/논리적으로 분리된 위치에 정기적으로 데이터 덤프 백업을 수행합니다.
  - IDC 전체 재해와 같은 상황에서도 데이터를 안전하게 보존하고 복구할 수 있습니다.
