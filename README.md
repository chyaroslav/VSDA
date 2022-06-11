# VSDA
Запуск БД PostgreSQL скрипты инициализации запускаются из текущего каталога
docker run --name pg -p 5432:5432 -e POSTGRES_USER=vsda -e POSTGRES_PASSWORD=VSDA22pwd -e POSTGRES_DB=vsdadb -d -v "$(pwd)":/docker-entrypoint-initdb.d postgres
