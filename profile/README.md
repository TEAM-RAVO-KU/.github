## RAVO
Robust And Versatile Open-source spring batch based backup solution
</br>

**RAVO** 프로젝트는 Spring Batch를 활용하여 RDB의 데이터를 주기적이며 자동적으로 Hot Standby DB 서버와 동기화하고 Cold Standby 형태로 백업하고 시스템을 구축하고 이를 Helm을 통해 배포 가능한 프로젝트를 구현하는 것을 목표로 합니다.</br></br>

특히, 대용량 데이터를 안정적이고 효율적으로 처리하기 위해 Chunk 기반 처리, 트랜잭션 관리, 체크포인트, 오류 복구 등을 도입하고자 합니다. 이와 함께 자동화된 실시간 덤핑 및 전환 기능을 통해 서비스의 연속성을 보장하고자 합니다.</br></br>

장애 발생 시에는 Host Standby DB Server로 신속하게 전환되어 다운타임을 최소화할 수 있도록 구성하였습니다. </br></br>

또한, 자체적으로 배포 및 관리가 가능한 오픈소스 백업 솔루션을 도입하여 운영 부담을 경감하였으며, 개발자들이 익숙한 JPA 엔티티 기반으로 백업 및 복구 프로세스를 구성함으로써 사용 편의성 또한 향상시켰습니다. </br></br>
