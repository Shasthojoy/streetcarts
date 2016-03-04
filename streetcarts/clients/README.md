# StreetCarts Clients

Once you've set up StreetCarts, you can use a client to try out its APIs. The [installation guide](https://github.com/apigee/docs-sandbox/wiki/Deploying-and-Running-StreetCarts#add-data) ends with a brief introduction to using cURL to add a food cart.

The repository also includes collection and environment files for [Postman support](https://github.com/apigee/docs-sandbox/tree/master/apps/streetcarts/clients/postman). You can use included collection and environment files for the [Postman application](https://www.getpostman.com/) to call StreetCarts APIs.

## Using OAuth

Most POST, PUT, and DELETE operation require an OAuth token. If you're using the Postman collection, you get tokens like this:

1. Call the `Register user` API. This API creates a new user with a username and password.
2. Call the `Authenticate user` API to generate an access token. 
    1. Set the Basic Auth with username/password as the client key/secret for one of the provisioned developer apps.
    2. Be sure to pass the scope header. Scopes set what the user can do. 

    If the user is a cart owner, pass these scopes:

    ```
    owner.create owner.update owner.read owner.delete
    ```

    If the user is a cart manager, pass these scopes:

    ```
    manager.update manager.read
    ```




