# blue-grouse-migrator
The blue grouse is the shortest migrating bird in the according to [guinness world records](https://www.guinnessworldrecords.com/world-records/shortest-bird-migration).

Why go far when you can go not so far! So I built this simple migrator.

It just runs all `*.sql` files under `migrations` folder and remembers which ones has been run. 

Database url is supplied through either env variable or `.env` file containing `DATABASE_URL="postgres://postgres:postgres@localhost/realworld"`.

##### Commands
- `add <name>` - add new migration to your migrations folder named `<timestamp>_<name>.sql` 
- `run` - Runs all migrations in your migrations folder


##### Limitations
- No down migrations! If you need down migrations, there are other more feature complete migrators to use.
- Only support postgres. Could be convinced to add other databases if there is need and easy to use database connection libs.

