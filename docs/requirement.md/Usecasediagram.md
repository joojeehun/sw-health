@startuml
left to right direction

actor "사용자" as User
actor "관리자" as Admin

rectangle "AI 건강 피드백 시스템" {
  usecase "생활 패턴 입력하기" as UC1
  usecase "생활 패턴 저장하기" as UC1_1

  usecase "생활 패턴 분석하기" as UC2
  usecase "피드백 제공하기" as UC2_1

  usecase "알림 받기" as UC3
  usecase "식사 시간 알림" as UC3_1
  usecase "수면 시간 알림" as UC3_2

  usecase "이전 생활 패턴 불러오기" as UC4
  usecase "이전 생활 패턴 저장하기" as UC4_1

  usecase "인터페이스 설정하기" as UC5
  usecase "글씨 크기 조정하기" as UC5_1
  usecase "UI 조정하기" as UC5_2

  usecase "전체 알림 현황 조회하기" as UC6
}

User --> UC1
User --> UC2
User --> UC3
User --> UC4
User --> UC5

Admin --> UC6

UC1 ..> UC1_1 : <<include>>
UC2 ..> UC2_1 : <<include>>
UC3 ..> UC3_1 : <<include>>
UC3 ..> UC3_2 : <<include>>
UC4 ..> UC4_1 : <<extend>>
UC5 ..> UC5_1 : <<include>>
UC5 ..> UC5_2 : <<include>>

@enduml
