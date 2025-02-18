# Kurşun Maruziyeti Risk Değerlendirmesi

```mermaid
graph TD
    A[Başla] --> B{Risk Değerlendirmesi};
    B -- Kurşuna maruziyet var mı? --> C{Biyolojik İzleme};
    B -- Kurşuna maruziyet yok -->  Son;
    C -- BLL >= 50 µg/dl --> D{Tıbbi Değerlendirme};
    C -- BLL < 50 µg/dl --> E --> Son;
    D -- Kurşun zehirlenmesi var --> F{Tedavi ve Takip};
    D -- Kurşun zehirlenmesi yok --> Son;
    F --> Son;
    
    classDef default fill:#f9f,stroke:#333,stroke-width:2px;
    class A,B,C,D,E,F default;
