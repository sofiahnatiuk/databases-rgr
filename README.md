# databases-rgr
Розрахунково-графічна робота

Створення додатку бази даних, орієнтованого на взаємодію з СУБД PostgreSQL

Опис сутностей та зв’язків між ними

Сутність User - користувач, який бронює квитки. Має char атрибути name (ім’я), surname (прізвище), phone (номер телефону) та key attribute user_id (атрибут, значення якого не може повторюватися, оскільки він використовується для ідентифікації).

Сутність Vehicle - транспорт, на якому здійснюється поїздка. Має char атрибут vehicle_type (тип транспорту, наприклад, автобус, поїзд тощо) та key attribute vehicle_id. 

Сутність Booking - бронювання. Має integer атрибут price (ціна поїздки), атрибут time типу time without timezone  (час бронювання), key attribute booking_id. Дана сутність пов’язана з двома іншими сутностями зв’язками 1:N, тобто один до багатьох. Один користувач може здійснювати багато бронювань, а один транспортний засіб можна бронювати багато разів. З іншого боку, одне бронювання може бути здійснене лише одним користувачем, і може стосуватися лише одного транспортного засобу.

Сутність staff – це працівник. Має ключовий атрибут staff_id, character varying атрибути name (ім’я) та position (посада). Має 1:N зв’язок з сутністю Vehicle (транспорт), оскільки на одному транспортному засобі можуть працювати кілька людей (наприклад, водій, провідник тощо), але один працівник працює лише на 1 транспортному засобі.
