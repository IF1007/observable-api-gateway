# observable-api-gateway

This project consists of an API Gateway for a microservices with high observability. It uses Envoy, Prometheus and Grafana to achieve this.

The microservice used as base to our tests was an [exemple of a cinema management ecosystem develop by Cristian Ramirez.](https://github.com/Crizstian/cinema-microservice)

## Prerequisites

This project assumes you have docker installed. To use the setup of this project your microservices must be ready to use an API Gateway, configure the envoy and our dockerfile yamls with their routes and addresses.

## How To Run
To set this project up, you need to execute a `docker-compose up -d mongo` and, after mongo is up and running, execute `docker-compose up`command on your terminal and let docker works.

#### Grafana
A Grafana service is automatically built on port 3000. It already contains a standard dashboard with all the detected microservices.

#### Envoy
A Envoy service is automatically built on port 8081. There you can perform the requests to the API routes.
Each service has it's own routes, you can check it [here](https://github.com/microservice-2020-3/cinema-microservice/tree/6cdf6ff2f5fb6526b511d3e344e0dff1d768a4f6/raml-spec)

#### Jaegger
A Jaegger dashboard will be up on port 16686.


### LICENSE
The MIT License (MIT)

Copyright (c) 2020 

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
