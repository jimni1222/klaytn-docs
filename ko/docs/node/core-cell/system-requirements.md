# 시스템 요구사항 <a id="system-requirements"></a>

## 하드웨어 사양 <a id="h-w-specification"></a>

네트워크 성능은 네트워크 내 가장 성능이 떨어지는 하드웨어 사양에 따라 측정됩니다. 블록체인 네트워크 구조에서는 수직적 확장\(하드웨어 용량 증가\)만 가능합니다. 따라서 네트워크 내의 모든 노드는 적어도 최상 수준의 서로 비슷한 사양을 가진 하드웨어로 구성하는 것을 추천합니다.

다음 장에서는 CN 및 PN 권장 사양을 보여줍니다.

### 베어메탈 서버 <a id="bare-metal-server"></a>

| 카테고리          | 사양                                                                                       |
|:------------- |:---------------------------------------------------------------------------------------- |
| 서버            | Intel® Server System R2312WFTZS                                                          |
| CPU           | Intel® Xeon 6148 2.40 GHz \(20-core/40-thread\) \* 2EA \(total 40-core/80-thread\) |
| 메모리           | 256GB \(32GB \* 8\)                                                                  |
| 스토리지(Storage) | 12TB \(1.92TB SSD \* 6, RAID 5\)                                                     |

이는 CN 및 PN에 권장되는 하드웨어 사양이며, 정확히 필요한 요구 사항은 아닙니다. 하드웨어 환경설정이 비슷하면 어떤 물리적 시스템이라도 CN 또는 PN을 작동시키기에 충분합니다.

### 클라우드 VM <a id="cloud-vm"></a>

#### AWS 권장 사양 <a id="recommended-specification-based-on-aws"></a>

| 모델명                           | vCPU 수 | 메모리 \(GiB\) | 스토리지 \(GiB\)   | EBS 대역폭 \(Mbps\) | 네트워크 대역폭 \(Gbps\) | 가격 \(서울 지역, USD/h\) |
|:----------------------------- |:------ |:------------- |:---------------- |:------------------ |:------------------- |:--------------------- |
| c5.18xlarge \(recommended\) | 72     | 144           | 500 (최소, EBS 전용) | 14,000             | 25                  | 3.456                 |

위 정보의 출처는 [https://aws.amazon.com/ec2/instance-types/](https://aws.amazon.com/ec2/instance-types/)과 [https://aws.amazon.com/ec2/pricing/on-demand/](https://aws.amazon.com/ec2/pricing/on-demand/)이며, AWS에 의해 변경될 수도 있습니다.

## 스토리지 요구사항 <a id="storage-requirements"></a>

평균 100 TPS, 평균 트랜잭션 크기 300 바이트, 그리고 1초의 블록 생성 시간을 가정 할 때 예상되는 스토리지 요구 사항은 2.5GB/1일 \(= 300x100x86400\) 입니다.

## 운영 체제 <a id="operating-system"></a>

[Amazon Linux 2](https://aws.amazon.com/ko/about-aws/whats-new/2017/12/introducing-amazon-linux-2/) 환경을 권장합니다. Klaytn 바이너리는 Amazon Linux 2에서 충분히 테스트 되었고, 리눅스 기반의 다른 환경에서도 가능합니다. 또한 개발 지원을 위해 macOS 용 바이너리도 제공하고 있습니다.