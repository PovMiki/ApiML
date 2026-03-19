<img width="609" height="168" alt="image" src="https://github.com/user-attachments/assets/579128a4-3c32-4554-9fc2-6739c9339595" />

**Cel ćwiczenia :**

Celem ćwiczenia jest praktyczne tworzenia API do serwowania modelu ML (FastAPI/Flask), testowania endpointów (Postman, cURL) i zwracanie predykcji.

**Przebieg :** 

**Zadanie 1**

Zainstalowałem FastApi oraz zaimplementowałem podstawową aplikację serwerową zwracającą Hello World w jsonie. Przetestowałem API w przeglądarce
<img width="945" height="197" alt="image" src="https://github.com/user-attachments/assets/014ecaa1-8b8a-495d-a5c2-4c05e476cf64" />
<img width="813" height="575" alt="image" src="https://github.com/user-attachments/assets/a9c2a0b1-3dc3-493c-b3f3-813a00bc3ed1" />
<img width="803" height="170" alt="image" src="https://github.com/user-attachments/assets/532a1c4a-eb81-46a3-b921-75ca6c5e4be4" />
**Zadanie 2**

Zaimportowałem model LogicRegression i wytrenowałem model na sztucznie stworzonych przeze mnie danych. Dodałem nowy endpoint który przyjmuje dane wejściowe JSON i dokonuje predykcji za pomocą modelu
<img width="775" height="866" alt="image" src="https://github.com/user-attachments/assets/f38d0933-366a-42a7-9545-75735fa6c644" />
Do przetestowania użyłem cURL czy zapytanie działa
<img width="945" height="86" alt="image" src="https://github.com/user-attachments/assets/198651b5-a3ad-447a-96c3-b636b9b26db9" />
**Zadanie 3**

Uzylem pydantic który automatycznie waliduje typy danych wejściowych 
W przypadku błędnych danych np. string zamiast float FastAPI zwraca błąd JSON z kodem 422
Zaimplementowałem obsługę błędów nielogicznych godzin wykorzystując HTTPException
<img width="945" height="382" alt="image" src="https://github.com/user-attachments/assets/09fe4214-09b8-42b1-9dad-4e18deee1aca" />
<img width="945" height="205" alt="image" src="https://github.com/user-attachments/assets/4ea7cc07-efb8-4a5c-b667-5d5e217a2ef7" />
**Zadanie 4** 

Dodałem endpointy Health i Info które zwracają informacje o modelu
<img width="697" height="569" alt="image" src="https://github.com/user-attachments/assets/0f4b95c5-cdab-49dd-a03f-1c2715422510" />
<img width="945" height="135" alt="image" src="https://github.com/user-attachments/assets/63ee9988-55da-4e97-b104-e31100fa07d4" />
**Zadanie 5** 

Tryb deweloperski używa wieloprocesowości –workers stworzył kilka procesów python działających jednocześnie dla tej jednej aplikacji. –host z zerami sprawia że serwer jest widoczny nie tylko na localhost ale w całej sieci lokalnej. –workers 4 uruchamia 4 procesy dzięki czemu gdy jeden zajmie się obliczaniem ML to pozostali mogą odbierać inne zapytania co jest ważne w trybie deweloperskim
<img width="945" height="340" alt="image" src="https://github.com/user-attachments/assets/f228e5c9-ffda-4382-aaf0-30196ee025af" />
<img width="945" height="99" alt="image" src="https://github.com/user-attachments/assets/8d85aaad-2b99-4c6b-9215-5e9670bb1087" />
