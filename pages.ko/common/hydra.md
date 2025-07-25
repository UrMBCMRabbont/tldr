# hydra

> 온라인 비밀번호 추측 도구.
> 지원되는 프로토콜에는 FTP, HTTP(S), SMTP, SNMP, XMPP, SSH 등이 포함됨.
> 더 많은 정보: <https://manned.org/hydra>.

- Hydra의 마법사를 시작:

`hydra-wizard`

- 주어진 사용자 이름과 비밀번호 목록을 사용하여 SSH 자격 증명을 추측:

`hydra -l {{사용자명}} -P {{경로/대상/단어목록.txt}} {{호스트_ip}} {{ssh}}`

- 두 개의 특정 사용자명 및 비밀번호 목록을 사용하여 HTTPS 웹 양식 자격 증명을 추측 ("https_post_request"는 "사용자명=^USER^&password=^PASS^"와 유사할 수 있음):

`hydra -L {{경로/대상/사용자명.txt}} -P {{경로/대상/단어목록.txt}} {{호스트_ip}} {{https-post-form}} "{{호스트_없는_url}}:{{https_post_요청}}:{{로그인_실패_문자열}}"`

- 사용자명과 비밀번호 목록을 사용하여 FTP 자격 증명을 추측하고, 스레드 수를 지정:

`hydra -L {{경로/대상/사용자명.txt}} -P {{경로/대상/단어목록.txt}} -t {{n_tasks}} {{호스트_ip}} {{ftp}}`

- 사용자명과 비밀번호 목록을 사용하여 MySQL 자격 증명을 추측하고, 사용자명/비밀번호 쌍이 발견되면 종료됨:

`hydra -l {{사용자명}} -P {{경로/대상/단어목록.txt}} -f {{호스트_ip}} {{mysql}}`

- 각 시도를 보여주는 사용자명과 비밀번호 목록을 사용하여, RDP 자격 증명을 추측:

`hydra -l {{사용자명}} -P {{경로/대상/단어목록.txt}} -V {{rdp://호스트_ip}}`

- 콜론으로 구분된 사용자명/비밀번호 쌍 목록을 사용하여, 다양한 호스트의 IMAP 자격 증명을 추측:

`hydra -C {{경로/대상/사용자명_비밀번호_쌍.txt}} {{imap://[호스트_범위_cidr]}}`

- 사용자명과 비밀번호 목록을 사용하여 호스트 목록에서 POP3 자격 증명을 추측하고, 사용자명/비밀번호 쌍이 발견되면 종료됨:

`hydra -L {{경로/대상/사용자명.txt}} -P {{경로/대상/단어목록.txt}} -M {{경로/대상/호스트.txt}} -F {{pop3}}`
