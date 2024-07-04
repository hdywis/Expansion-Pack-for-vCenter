NSX - Power Up Kit 는 기존 NSX 의 추가 데이터 수집을 위해 개발되었습니다. NSX 버전 변경으로 API 가 변경된다면 의도한 대로 작동하지 않을 수 있습니다.
사전에 API Request Limit 및 현재 호출되고 있는 API Request 를 확인하고, 예상 API Request 수를 확인 후 적용이 필요합니다.
NSX API Request Counts = 4 + (Load Balancer Service * 1) + (Load Balancer Virtual Server * 1) + (Load Balancer Pool * 3)

Release Note - Version number : 24.5.21 Tested Aira Operations Version: 8.17.1.23642243, NSX Version: 4.1.2.3.0.23382408

Requests
GET /policy/api/v1/transport-nodes
GET /policy/api/v1/infra/lb-services
GET /policy/api/v1/infra/lb-virtual-servers
GET /policy/api/v1/infra/lb-virtual-servers/{lb-virtual-server-id}
GET /policy/api/v1/infra/lb-pools
GET /policy/api/v1/infra/lb-services/{lb-service-id}
GET /policy/api/v1/infra/lb-pools/{lb-pool-id}
GET /policy/api/v1/infra/lb-services/{lb-service-id}/lb-pools/{lb-pool-id}/statistics
GET /policy/api/v1/infra/lb-services/{lb-service-id}/lb-pools/{lb-pool-id}/detailed-status

Objects
[ARIA_OPS] NSX Transport Node: Node Size
[ARIA_OPS] Load Balancer Service: Size
[ARIA_OPS] Load Balancer Virtual Server: IP Address, Access Log Enabled, Application Profile Path
[ARIA_OPS] Load Balancer Pool: Algorithm, SNAT Translation Type, TCP Multiplexing Enabled, TCP Multiplexing Number, Min Active Members, Path
[INTERNAL] Load Balancer Pool Member: IP Address, Port, Status, Last State Change Time, LB Service ID, LB POOL ID, Pool Path, Current Sessions, Max Sessions, Total Sessions, Current Session Rate, Bytes In, Bytes Out, Bytes In Rate, Bytes Out Rate, HTTP Request Rate, HTTP Requests
[INTERNAL] Load Balancer Virtual Server Port: Port

Relationships
Load Balancer Virtual Server -> Load Balancer Virtual Server Port
Load Balancer Pool -> Load Balancer Pool Member
Load Balancer Pool Member -> Virtual Machine

Content
[SUPER_METRIC] EDGE Cluster - Tier-0 Count
[SUPER_METRIC] EDGE Cluster - Tier-1 Count
[SUPER_METRIC] EDGE Cluster - Peak Edge Node CPU Highest Usage
[SUPER_METRIC] EDGE Cluster - Peak Edge Node Memory Usage
[SUPER_METRIC] EDGE Cluster - LB CPU Usage
[SUPER_METRIC] EDGE Cluster - LB Memory Usage
[SUPER_METRIC] EDGE Cluster - LB Count
[SUPER_METRIC] EDGE - Node Memory Usage
[SUPER_METRIC] EDGE - LB Capacity Usage
[SUPER_METRIC] LB - Pool Member Count
