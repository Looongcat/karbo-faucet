# Karbo cryptocurrency faucet
This is set of docker scripts for running cryptocurrency faucet. It's suited for Karbo cryptocurrency, but would be suitable for any currency with karbo-compatible wallet (it's basically most of cryptonote-based currencies which have simplewallet app)

## How to setup (default .env settings)
- Create wallet file and place it in ./services/wallet with name faucet.wallet
- Open .env file with any editor you're comfortable with.
- Change next settings:
1. FEE_ADDRESS - replace it with your faucet's address
2. WALLET_PASS - specify password for yours wallet file
3. DB_PASS, DB_ROOT_PASS - specify some good passwords for the database
- Open ./services/caddy/caddyfile
- Replace awesomekarbofaucet.com domain with your one, replace owner@awesomekarbofaucet.com with your contact email (required by Let's encrypt cert enrolling service)
- If you're using default frontend for the faucet - open ./frontend/config.php and carefully fill up all necessary variables

Now you're ready to run your server with a single command: `docker-compose up -d`

## How to use server
###### (Important!) Every operation must be run from ./
1. Stop a single service
`docker-compose stop <service name>`

2. Start a single service
`docker-compose stop <service name>`

3. Stop the whole server
`docker-compose up -d <service name>`

4. Start the whole server
`docker-compose up -d`

5. Show logs from the whole server
`docker-compose logs`

6. Show logs from a single service
`docker-compose logs <service name>`

7. Restart a single service
`docker-compose restart <service name>`

## Credits
© 2018 [Looongcat](https://github.com/Looongcat)