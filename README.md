# Dockerized Wordpress
- Start the project using `docker-compose up -d`
- Connect to `http://localhost:8080`

## Database setup
```
host: db
database: wordpress
username: wordpress
password: wordpress
```

# Restore duplicator backup
- Download from production site the `installer` package and the `*.daf` archive
- Move the `installer.php` and the `*.daf` archive inside `./html` folder (clear everything if needed)
- Navigate to `http://localhost:8080/installer.php` and follow restore wizard

**WARNING**: Ensure rules to redirect requests to HTTPS are not enabled in the `.htaccss` file. In case delete them. 
