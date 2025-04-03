# Setup
```bash
docker-compose up

docker exec -it user_data bash
```
```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123';

ALTER USER 'users_service' IDENTIFIED WITH mysql_native_password BY '123';

flush privileges;
```
```bash
curl -L http://localhost/?username=alice | json_pp
```