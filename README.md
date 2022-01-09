Creating certifactes after creating user secrets guid's for each api.
* cd CoffeeApi
* dotnet dev-certs https -ep $env:USERPROFILE\.aspnet\https\CoffeeAPI.pfx -p Pa55w0rd!* 
* dotnet dev-certs https --trust
* dotnet dev-certs https -ep $env:USERPROFILE\.aspnet\https\TeaAPI.pfx -p Pa55w0rd!
* dotnet dev-certs https --trust
* cd ../TeaAPI
* dotnet user-secrets set "Kestrel:Certificates:Development:Password" "Pa55w0rd!"
* cd ../CoffeeApi
* dotnet user-secrets set "Kestrel:Certificates:Development:Password" "Pa55w0rd!"
* docker-compose up --build
