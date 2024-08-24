FROM mysql:8.0
## here we are creating system user not human user
RUN adduser -r expense 
ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1\
    MYSQL_USER=expense\
    MYSQL_PASSWORD=ExpenseApp@1\
    MYSQL_DATABASE=transactions
COPY scripts/*.sql /docker-entrypoint-initdb.d/
### given ownership to the below paths for the user
RUN chown -R expense:expense /var/lib/mysql /var/run/mysqld

### at finally we are running the container with syatem user
# USER expense