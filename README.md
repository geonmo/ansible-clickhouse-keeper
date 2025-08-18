# Ansible Role: ClickHouse Keeper

이 Ansible Role은 [ClickHouse Keeper](https://clickhouse.com/docs/en/guides/sre/keeper/)를 설치하고 설정합니다.

## 요구사항

- Ansible 2.1 이상
- Red Hat Enterprise Linux 9 또는 호환되는 배포판

## 역할 변수

- `keeper_port`: Keeper가 수신 대기할 포트 (기본값: `2181`)
- `keeper_secured_port`: SSL을 사용하여 Keeper가 수신 대기할 포트 (기본값: `3181`)
- `enable_ssl`: SSL 활성화 여부 (기본값: `false`)
- `ssl_server_cert`: SSL 서버 인증서 경로 (기본값: `/etc/clickhouse-keeper/tls/server.crt`)
- `ssl_server_key`: SSL 서버 키 경로 (기본값: `/etc/clickhouse-keeper/tls/server.key`)
- `ssl_ca_cert`: SSL CA 인증서 경로 (기본값: `/etc/clickhouse-keeper/ca/ca.crt`)
- `negotiator_port`: Keeper 노드 간 협상 포트 (기본값: `9234`)
- `firewall_zone`: 방화벽 영역 (기본값: `internal`)

## 종속성

이 역할에는 종속성이 없습니다.

## 예제 플레이북

```yaml
- hosts: keeper
  roles:
    - geonmo.clickhousekeeper
```

## 라이선스

MIT

## 작성자 정보

- Geonmo Ryu
- KISTI (한국과학기술정보연구원)