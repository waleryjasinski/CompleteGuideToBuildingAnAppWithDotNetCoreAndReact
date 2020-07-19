dotnet new -h  
dotnet new sln                     
dotnet new classlib -n Domain      
dotnet new classlib -n Application 
dotnet new classlib -n Persistence 
dotnet new webapi -n API

 dotnet sln h
 dotnet sln add .\Domain\Domain.csproj
 ...
 dotnet sln list 

 cd .\Application\ 
 dotnet add reference ..\Domain\  
...

dotnet tool install --global dotnet-ef


dotnet ef migrations add InitialCreate -p .\Persistence\ -s .\API\

dotnet ef database update

dotnet watch run