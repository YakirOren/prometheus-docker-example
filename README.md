# run prometheus in docker 
## and connect to it using the api


## configuration

1. run the provided python script or use an online tool to create a bcrypt hash of your password

2. add the hash and the user name to the web.yml file

```yml
basic_auth_users:
  alice: <your bcrypt hash>
  bob: $2b$12$D5lgvKt7gvbvVUkP2gUlJe/0bdwLi6S5fRQnD0x1MMRehTeOTAkjm
```

## running
1. start the services
``` 
docker compose up
```

3. to simulate a real deployment use ngrok, to create a fake url to our service.

``` ngrok http 9090```

