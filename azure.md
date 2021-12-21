The backend application is on serverless framework and the functions are deployed to azure
On 3rd December, deleted the database, which was not intended, the intention was to clear storage account and other dummy data they have created in the database, but deleted everything by mistake, but restored the database to a point of day before the crash, but the functions were not reachable. Checked out the end-point in the flutter application and for login found out to be this, 

http://sls-wus2-dev-career-guru.azurewebsites.net/api/userLogin

Reaching out the the api, it shows 502 gateway error, 

If running the command
```sls offline```
![image](https://user-images.githubusercontent.com/42163313/146928612-5d509ff2-1bcb-44b6-b0dc-1d1831a06a4a.png)
The output in getRequest, it means that the functions are accessible
![image](https://user-images.githubusercontent.com/42163313/146928751-74c8ee8c-ca42-43e9-a77f-45160d17ec46.png)

------------------
```sls offline start```
![image](https://user-images.githubusercontent.com/42163313/146930510-a01299d6-6ef0-4a22-b539-d10b5e092ca9.png)
![image](https://user-images.githubusercontent.com/42163313/146930536-b6f47955-d68a-4880-ade3-18589b25f4e9.png)


------------------

This is the case locally, but during 3rd december the backend was not deployed locally.. so, sure that backend has nothing much to do with functions failure

----

The main motive is to anyhow make the functions workable(http endpoints) and the application would work normally

I have also deleted the storage bucket, which was intended to be deleted, and the developer who made this also said that the storage is automatically created

---------

