```mermaid
graph TD
    A[Начало] --> B[Ввод данных о продавце]
    B --> C[Ввод данных о покупателе]
    C --> D[Ввод данных о товаре/услуге]
    D --> E[Ввод номера и даты счет-фактуры]
    E --> F[Ввод условий оплаты и поставки]
    F --> G[Создание заголовка "Счет-фактура"]
    G --> H[Добавление данных о продавце и покупателе]
    H --> I[Создание таблицы с товарными позициями]
    I --> J[Для каждой позиции: расчет общей стоимости и добавление строки в таблицу]
    J --> K[Подсчет итоговой суммы (без НДС)]
    K --> L[Расчет суммы НДС (если применимо)]
    L --> M[Вычисление общей суммы с учетом НДС]
    M --> N[Проверка правильности данных и расчетов]
    N --> O[Добавление подписей и печатей]
    O --> P[Сохранение и отправка счет-фактуры покупателю]
    P --> Q[Архивирование копии счет-фактуры]
    Q --> R[Конец]

    subgraph "Подготовка данных"
        B
        C
        D
        E
        F
    end

    subgraph "Формирование документа"
        G
        H
        I
        J
        K
        L
        M
    end

    subgraph "Завершающие действия"
        N
        O
        P
        Q
    end