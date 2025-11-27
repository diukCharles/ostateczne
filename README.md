1. **Sklonuj projekt i wejdź do katalogu:**

   ```bash
   git clone git@github.com:diukCharles/ostateczne.git
   cd ostateczne
   docker-compose build
   docker-compose up -d


2. **Utwórz bazę danych:**

   ```bash
   sudo docker-compose exec db psql -U demo -d demo

   CREATE TABLE "Todos" (
        "Id" SERIAL PRIMARY KEY,
        "Title" TEXT NOT NULL,
        "IsDone" BOOLEAN NOT NULL,
        "CreatedAt" TIMESTAMPTZ NOT NULL
    );
   ALTER TABLE "Todos" ADD COLUMN "Priority" INT DEFAULT 1;
