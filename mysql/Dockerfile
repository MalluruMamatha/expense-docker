FROM mysql:8.0
ENV mysql_root_password=ExpenseApp@1\
    MYSQL_USER=expense\
    MYSQL_PASSWORD=ExpenseApp@1\
    MYSQL_DATABASE=transactions
COPY scripts/*.sql /docker-entrypoint-initdb.d/
