- Dashboard, Studio Token 오류 발생 시 확인 사항  
    Brick, IWP : 시간 확인  

- 인터넷 연결 불가능 상태  
    CoreDNS에서 외부 DNS 서버를 모르는 상태인 경우  
    /etc/resolve.conf 변경 후 CoreDNS 재 시작  

- NBP 환경(네이버 비즈니스 파트너스)  
	K8S 환경 구축 시 Calico VXLAN으로 환경을 구성해야 한다.  
	IPinIP 환경으로 구성하는 경우 서로 다른 노드의 POD 간 통신이 불가능하다.  
	
- 업로드 1메가 이상 불가  
	k8s환경에서 도메인 접속을 위해 ingress를 사용하는 경우  
	* 조치
	아래와 같이 annotations에서 설정하는 부분을 변경하고, ingress를 다시 생성한다. 
	```yaml
	...
	metadata:
	  annotations:
		nginx.ingress.kubernetes.io/proxy-body-size: 1g
	...
	```
