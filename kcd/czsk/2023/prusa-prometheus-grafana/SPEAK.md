# How to not use Prometheus and Grafana with Prusa printers

## Beggining // not spoken heading

Good afternoon, I'm here to tell you about how I created Prometheus Exporter for Prusa printers

## Who am I?

My name is Pavel Strobl and I work at Prusa Research as DevOps engineer. My main goal is to make sure that our web services like eshop, knowledgebase or Printables works. I'm in charge of observability and infrastructure and I at least try to not to destroy our cluster. And I make pretty dashboards with cute panels.

I also enjoy making hardware devices even tho it is long time ago when I've made one. I like cars, driving them and going for trackdays. As a bonus, I can make my own beer, in the future with monitoring.

## What is Prometheus exporter?

Prometheus first. Prometheus is a tool for collecting data, metrics. You want to store these data effectively and there is a lot of ways how to do that. Prometheus is one kind of solution. And exporter is something that provides these data for Prometheus to scrape. It uses a pull model so there is not much of overhead for device and that was my goal.

You can expose /metrics at any device, Django application, standalone exporter that scrapes targets, even on something like ESP32, Raspberry Pi Pico or something like that. Because it is just "text file" that is chillin at /metrics endpoint.

## But why?

I have multiple printers, in my living room. And my wife also has a 3D printer so I wanted to collect data from every single printer we have. And when I had these data I wanted to visualized them. And why not save them for alerting? Something like MMU faults?

What I like about Grafana and Prometheus is freedom, you can use data for creation of dashboards. Beeing alerted by slack bot, email, phone or discord bot. I only miss being able to get notice by letter. For funsies there is also possibility of machine learning like Tamland by Gitlab or you can get Grafana Cloud.

## How it works?

It just works. Somehow? I guess. I used Golang for implementation, it is my first project in Golang and I've never been a great programmer but I can write line or two, maybe three. I used Prometheus library and implemented three handlers for different type of boards and firmwares that Prusa Research use. Currently I support only FDM printers and not the SLA ones.

## Demo!

It's Demo time! I use Grafana Cloud and I'm in free tier but you can certainly pay for Pro tier or deploy your own Grafana instance.

## Current status

Well it works. I like messing with code so my code is kinda messy. There is lot of to do, I have few more thing in my mind, I want log more information I want have my dashboards better. I want to drop support for Legacy firmware, I want CD pipeline for my cluster, I want to shrink my Docker image etc. Only future can tell how it will look.

## Thanks! // not spoken heading

Well thanks, if you have any question then hola if you need me. You can also scan this QR code to get my slides.

See ya later.