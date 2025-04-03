# Setup
```bash
# 1. run docker-compose
docker-compose up

# 2. setup database container
docker exec -it user_data bash
mysql -u root -p # password is 123
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
# 4. test the asset service
curl -L http://localhost:8008/?username=alice | json_pp

# 5. test the user service
curl -L http://localhost/?username=alice | json_pp
```