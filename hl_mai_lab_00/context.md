# Контекст решения
<!-- Окружение системы (роли, участники, внешние системы) и связи системы с ним. Диаграмма контекста C4 и текстовое описание. 
-->
```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

Person(admin, "Администратор")
Person(user, "Пользователь")

System(order_site, "Сайт заказа услуг", "Веб-сайт для заказа услуг")



Rel(admin, order_site, "Просмотр, добавление и редактирование информации о пользователях, услугах и заказах")
Rel(user, order_site, "Регистрация, просмотр/изменение информации о услугах и заказах")



@enduml
```
## Назначение систем
|Система| Описание|
|-------|---------|
| Сайт заказа услуг | Веб-интерфейс, обеспечивающий доступ к информации по услугам и заказам. Бэкенд сервиса реализован в виде микросервисной архитектуры |

