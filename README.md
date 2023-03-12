# Experiment with Terraform plugin framework

Instead of managing servers and networks with terraform,  
the project is about experementing terraform with a simple REST API.

## Computer Database REST API

*requires [node](https://nodejs.org) (developed with v14.18.1)*

`./computer_database_rest_api/server.js`

```sh
Server running at http://127.0.0.1:8080/api/v1

```

`curl -s http://127.0.0.1:8080/api/v1/companies | jq`

```json
[
  {
    "id": "co00",
    "name": "Cresus",
    "location": "global",
    "computerModels": [
      "http://127.0.0.1:8080/api/v1/companies/co00/computer-models/co00cm00",
      "http://127.0.0.1:8080/api/v1/companies/co00/computer-models/co00cm01"
    ],
    "uri": "http://127.0.0.1:8080/api/v1/companies/co00"
  },
  {
    "id": "co01",
    "name": "Syrup",
    "location": "NA",
    "computerModels": [
      "http://127.0.0.1:8080/api/v1/companies/co01/computer-models/co01cm00"
    ],
    "uri": "http://127.0.0.1:8080/api/v1/companies/co01"
  }
]
```

## Custom terraform provider

<https://developer.hashicorp.com/terraform/plugin/framework/getting-started/code-walkthrough>