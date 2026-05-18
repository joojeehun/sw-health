usecaseDiagram
actor 사용자 as User
actor 관리자 as Admin

User --> (생활 패턴 입력하기)
User --> (생활 패턴 분석하기)
User --> (알림 받기)
User --> (이전 생활 패턴 불러오기)
User --> (인터페이스 설정하기)

Admin --> (전체 알림 현황 조회하기)

(생활 패턴 입력하기) ..> (생활 패턴 저장하기) : include

(생활 패턴 분석하기) ..> (피드백 제공하기) : include

(알림 받기) ..> (식사 시간 알림) : include
(알림 받기) ..> (수면 시간 알림) : include

(이전 생활 패턴 불러오기) ..> (이전 생활 패턴 저장하기) : extend

(인터페이스 설정하기) ..> (글씨 크기 조정하기) : include
(인터페이스 설정하기) ..> (UI 조정하기) : include
