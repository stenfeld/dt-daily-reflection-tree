# Tree Diagram

```mermaid
flowchart TD
    START --> Q_OPEN_1
    Q_OPEN_1 --> D_OPEN
    D_OPEN --> R_OPEN_STABLE
    D_OPEN --> R_OPEN_HEAVY

    R_OPEN_STABLE --> Q_A1_1
    R_OPEN_HEAVY --> Q_A1_1

    Q_A1_1 --> Q_A1_2
    Q_A1_2 --> Q_A1_3
    Q_A1_3 --> D_A1
    D_A1 --> R_A1_HIGH
    D_A1 --> R_A1_LOW

    R_A1_HIGH --> B_A1_A2
    R_A1_LOW --> B_A1_A2
    B_A1_A2 --> Q_A2_1

    Q_A2_1 --> Q_A2_2
    Q_A2_2 --> Q_A2_3
    Q_A2_3 --> D_A2
    D_A2 --> R_A2_HIGH
    D_A2 --> R_A2_LOW

    R_A2_HIGH --> B_A2_A3
    R_A2_LOW --> B_A2_A3
    B_A2_A3 --> Q_A3_1

    Q_A3_1 --> Q_A3_2
    Q_A3_2 --> Q_A3_3
    Q_A3_3 --> D_A3
    D_A3 --> R_A3_HIGH
    D_A3 --> R_A3_LOW

    R_A3_HIGH --> SUMMARY
    R_A3_LOW --> SUMMARY
    SUMMARY --> END
