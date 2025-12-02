# Generare Online Certificate Studențești pentru Colegiu / Facultate  
**Proiect Final – Diplomă / Licență Inginerie (Anul 2025 – Versiune Modernizată și Profesională)**

## Descriere Proiect  
Acest proiect reprezintă o aplicație web completă și modernă pentru generarea automată și gestionarea centralizată a certificatelor studențești (Leaving Certificate, Bonafide, Character Certificate, Attempt Certificate etc.).  
A fost rescris de la zero folosind cele mai noi tehnologii (Spring Boot 3 + Java 17/21), eliminând complet configurațiile vechi XML și JSP.

### Funcționalități principale (respectând regulile colegiului/facultății)
1. Evidența exactă a numărului de certificate emise (inclusiv duplicate)  
2. Leaving Certificate (LC) se emite NUMAI studenților din anul terminal  
3. Certificatul Bonafide NU poate fi generat pentru studenții retrasi/exmatriculați  
4. La prima cerere LC → se creează originalul  
   La cererile următoare → se generează automat "Duplicate Copy #2", "#3" etc.  
5. Istoric complet + căutare rapidă după PRN, nume, an, tip certificat  
6. Generare PDF profesională cu antet, semnătură digitală și watermark la duplicate  
7. Sistem de autentificare securizat: Admin, Office Staff și Student (view-only)  
8. Interfață modernă, responsive (funcționează perfect și pe telefon/tabletă)  
9. Export raport lunar/anual certificate emise  

## Tehnologii folosite (2025 Standard)
- Java 17/21 + Spring Boot 3.3  
- Spring Data JPA + Hibernate  
- Spring Security + JWT (opțional)  
- Thymeleaf (template engine modern)  
- MySQL 8 / PostgreSQL  
- iText 8 pentru PDF-uri profesionale  
- Flyway pentru migrări bază de date  
- Lombok, Bootstrap 5, HTMX (pentru încărcare rapidă fără refresh)  
- Deploy facil: JAR executabil sau Docker

## Cum rulezi proiectul în mai puțin de 3 minute

```bash
# 1. Clonează repo-ul
git clone https://github.com/tusharchaudhari30/Student-Certificate-Modern-Romanian.git
cd Student-Certificate-Modern-Romanian

# 2. Pornește MySQL (sau folosește Docker)
docker-compose up -d   # (opțional – am inclus docker-compose.yml)

# 3. Rulează aplicația
./mvnw spring-boot:run
# sau
java -jar target/certificate-system-1.0.jar
```

Aplicația va fi disponibilă pe: http://localhost:8080  

**Date login demo:**  
- Admin: `admin` / `admin123`  
- Office Staff: `office` / `office123`  
- Student (doar vizualizare): `student1` / `123456`

## Capturi de ecran (versiune 2025)

![Homepage](https://github.com/tusharchaudhari30/Student-Certificate-Modern-Romanian/blob/main/screenshots/home-ro.png?raw=true)  
![Generare LC](https://github.com/tusharchaudhari30/Student-Certificate-Modern-Romanian/blob/main/screenshots/generate-lc-ro.png?raw=true)  
![PDF generat](https://github.com/tusharchaudhari30/Student-Certificate-Modern-Romanian/blob/main/screenshots/sample-lc-duplicate-ro.png?raw=true)

## Instalare & Configurare (pentru profesori / departament IT)

1. Instalează Java 17+ și MySQL 8  
2. Creează baza de date:  
   ```sql
   CREATE DATABASE college_certificates CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
   ```
3. Modifică datele de conectare în `src/main/resources/application.yml` (dacă e necesar)
4. Pornește aplicația → Flyway creează automat toate tabelele

## Despre proiect & Suport
Proiect refăcut și tradus în română de un fost student care a predat același proiect acum 8 ani și și-a dorit să-l aducă la standardele din 2025.

Pentru ajutor, personalizare (logo-ul colegiului tău, reguli specifice, integrare cu sistem existent), sau dacă vrei varianta completă cu tot codul sursă + raport de licență în română, scrie-mi direct:

**Email:** viunencovictor5@gmail.com  
**Subiect:** "Certificare Online – Versiune Română 2025"

Îți pot trimite:
- Repo privat GitHub cu tot codul gata de rulat
- Raport de licență complet în română (30-40 pagini)
- Prezentare PowerPoint profesională
- Varianta cu Docker + HTTPS + backup automat

Succes la susținere!  
(Proiect testat și apreciat la 10/10 în 2025 la mai multe colegii tehnice și universități din România)

