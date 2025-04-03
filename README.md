# Setup
```bash
# 1. run docker-compose
docker-compose up

# 2. setup database container
docker exec -it user_data bash
mysql -u root -p
```
```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123';

ALTER USER 'users_service' IDENTIFIED WITH mysql_native_password BY '123';

flush privileges;
```
```bash
# 3. check mongodb has been seeded correctly
docker exec -it asset_mapping mongosh
use user
db.userProfile.find() 
```


```bash
curl -L http://localhost/?username=alice | json_pp
```