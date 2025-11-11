# AWS Lambda vs Lambda@Edge: Edge Computing Performance Analysis
# Overview

This project investigates the performance differences between AWS Lambda (centralised) and Lambda@Edge (edge-based) by integrating the OpenWeather API. It analyses how serverless functions perform when executed in a single AWS region versus distributed global edge locations via Amazon CloudFront.

The aim is to provide practical insights into latency, scalability, and responsiveness, highlighting how edge computing improves performance for globally distributed users.

# Objectives

Build two serverless systems:

Centralised Lambda via Amazon API Gateway

Lambda@Edge via Amazon CloudFront

Integrate the OpenWeather API for dynamic, location-aware responses.

Test latency, cold starts, and scalability using Postman.

Monitor execution behaviour and performance metrics via Amazon CloudWatch.

Analyse and compare the results through tables, charts, and discussion.

# Architecture
# Centralised Lambda

# Flow:
Client → API Gateway → Lambda → OpenWeather API → Response

Executes in a single AWS region.

Metrics monitored through Amazon CloudWatch.

# Lambda@Edge

# Flow:
Client → CloudFront → Lambda@Edge → OpenWeather API → Response

Executes at the nearest AWS edge location.

Enables low-latency, location-aware responses.

# Tools and Technologies

AWS Lambda – serverless compute for regional execution

Lambda@Edge – serverless functions deployed globally at the edge

Amazon CloudFront – content delivery and edge function distribution

Amazon API Gateway – API entry point for regional Lambda

Amazon CloudWatch – monitoring execution, latency, and cold starts

Postman – request simulation and latency testing

OpenWeather API – external data source for real-time weather data

Python – function development and integration logic

GitHub – version control and project publishing

Testing and Methodology

Simulated multiple regional requests via Postman.

Measured latency, execution times, and cold starts under controlled conditions.

Used CloudWatch Logs to monitor execution time, memory usage, and scalability.

Compared Lambda and Lambda@Edge responses using identical payloads for fairness.

# Expected Outcomes

Lambda@Edge expected to achieve lower latency due to execution proximity to users.

CloudFront caching anticipated to reduce repeated request times.

Overall execution time expected to remain similar, with edge-based requests showing significantly reduced network latency.

# References

Amazon Web Services (2011) Shared Responsibility Model. Available at: https://aws.amazon.com/compliance/shared-responsibility-model/
 (Accessed: 20 October 2025).

Amazon Web Services (2015) API Gateway – REST API Developer Guide. Available at: https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-rest-api.html
 (Accessed: 14 October 2025).

Amazon Web Services (2017) Amazon CloudWatch Overview. Available at: https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html
 (Accessed: 09 October 2025).

Amazon Web Services (2018a) Amazon CloudFront – Developer Guide. Available at: https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/lambda-at-the-edge.html
 (Accessed: 11 October 2025).

Amazon Web Services (2018b) Amazon CloudFront – Developer Guide: Lambda@Edge Function Restrictions. Available at: https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/lambda-at-edge-function-restrictions.html
 (Accessed: 11 October 2025).

Amazon Web Services (2025) Lambda Documentation – Best Practices. Available at: https://docs.aws.amazon.com/lambda/latest/dg/best-practices.html
 (Accessed: 25 October 2025).

Cloudflare (2017) What is Serverless? – Serverless Definition. Available at: https://www.cloudflare.com/en-gb/learning/serverless/what-is-serverless/
 (Accessed: 12 October 2025).

Cloudflare (2018) What is Edge Computing?. Available at: https://www.cloudflare.com/en-gb/learning/serverless/glossary/what-is-edge-computing/
 (Accessed: 12 October 2025).

Cloudflare (2025) Cloudflare Workers Documentation – Overview. Available at: https://developers.cloudflare.com/workers/
 (Accessed: 29 October 2025).

Serverless Inc. (2015) AWS Lambda Overview. Available at: https://www.serverless.com/aws-lambda
 (Accessed: 09 October 2025).

SLS Guru (2016) AWS Lambda vs Lambda@Edge. Available at: https://www.sls.guru/tips/aws-lambda-vs-lambda-edge
 (Accessed: 10 October 2025).

Johnston, P. (2018) Reducing Latency and Shifting Compute to the Edge with Lambda@Edge. AWS Blog. Available at: https://aws.amazon.com/blogs/networking-and-content-delivery/reducing-latency-and-shifting-compute-to-the-edge-with-lambdaedge/
 (Accessed: 13 October 2025).

Souk, A. (2019) Leveraging External Data in Lambda@Edge. AWS Blog. Available at: https://aws.amazon.com/blogs/networking-and-content-delivery/leveraging-external-data-in-lambdaedge/
 (Accessed: 10 October 2025).

McGrath, G. and Brenner, P. (2017) Serverless Computing: Design, Implementation, and Performance. IEEE ICDCSW.

Satyanarayanan, M. (2017) The Emergence of Edge Computing. IEEE Computer.

OpenWeather (2011) OpenWeather API Documentation. Available at: https://openweathermap.org/api
 (Accessed: 26 October 2025).

Postman (2015) Postman Tools Overview. Available at: https://learning.postman.com/docs/introduction/overview/
 (Accessed: 09 October 2025).

# Author

Hamza Hassan
Final-year Computer Science student | Cloud and DevOps enthusiast | Focused on designing scalable, efficient, and globally distributed cloud systems
