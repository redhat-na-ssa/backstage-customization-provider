# backstage-customization-provider

This is an example Express server, which serves an API.

To run:

    npm install
    npm start

The app will now start on <http://localhost:8080>

If you hit <http://localhost:8080> you'll get a sample data for home:

If you hit <http://localhost:8080/tech-radar> you'll get a sample data for tech radar:

## Build locally using Podman

```sh
podman build . -t quay.io/your_org/backstage-customization-provider
podmn run -it -p 8080:8080 quay.io/your_org/backstage-customization-provider

curl -s localhost:8080/ | jq .
```

## Build and Deploy using Nodeshift

```sh
npx nodeshift --strictSSL=false --expose
```

## Deploy it on OpenShift

Can use oc CLI as below or use import from git flow from OpenShift Developer Console

    oc new-app https://github.com/janus-idp/backstage-customization-provider
    oc expose svc/backstage-customization-provider

## Acknowledgements

This app was created using the [Express application generator][expressgen].

[express]: https://expressjs.com/
[expressgen]: https://expressjs.com/en/starter/generator.html
