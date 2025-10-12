 RAVO는 금융권과 같이 비즈니스 연속성이 필수적인 K-PaaS 기반 Kubernetes 클러스터 환경에서, RDB를 사용하는 서비스의 가용성을 극대화하는 솔루션입니다. </br>
 Debezium과 Kafka를 활용한 CDC 기술을 기반으로 Active DB 서버의 데이터 변경 사항을 실시간으로 Standby DB 서버에 반영하여 라이브 동기화를 유지하며, 별도의 콜드 백업을 통해 데이터 안정성을 강화합니다.</br>
 특히 장애가 발생하면 자체적으로 구현한 'Failover Watcher'가 이를 즉시 감지하여 Standby DB로 서비스를 자동 전환함으로써 다운타임을 최소화합니다.</br>
 더 나아가, 기존 Active DB가 복구된 이후에는 GTID가 적용된 Standby DB의 binlog를 추적하여 장애 발생 시점 이후의 모든 데이터 변경분을 다시 Active DB와 동기화함으로써 데이터의 정합성을 보장합니다.
 </br></br>
