# How to not use Prometheus and Grafana with Prusa printers

## Beggining // not spoken heading

Good afternoon, I'm here to tell you about how I created Prometheus Exporter for Prusa printers

## Who am I?

My name is Pavel Strobl and I work at Prusa Research as DevOps engineer and my main goal is to make sure that our web services works. I'm in charge of observability and infrastructure and I at least try to not to destroy our cluster.

Apart of that I enjoy making hardware devices even tho it is far ago when I've made one. I like cars and driving them. And bonus, I can make my own beer.

## What is Prometheus exporter?

Prometheus first. Prometheus is tool for collecting data, metrics. You want to store these data effectively and there is a lot of ways how to do that. Prometheus is one of them. And exporter is something that provides these data for Prometheus to scrape. It uses pull model so there is not much of overhead for device and that was my goal.

You can expose /metrics at any device, Django application, standalone exporter that scrapes targets, even on something like ESP32, Raspberry Pi Pico or something like that. Because it is just "text file" that is chillin at /metrics endpoint.

## But why?

I have multiple printers, in my living room. And my wife has a 3D printer so I wanted to collect data from them. And when I had these data I wanted to visualized them. And why not save them for alerting? Something like MMU faults?

What I like about Grafana and Prometheus is freedom, you can provide dashboards but how about creating your own. And you certainly can. For funsies there is also possibility of machine learning like Tamland by Gitlab.

## How it works?

Somehow? I guess. It just works. I used Golang for implementation, it is my first project in Golang I've never been a great programmer but I can write line or two, maybe more. I used Prometheus library and implemented three handlers for different type of boards that Prusa Research use.

## Demo!

yolo

## Current status

Well it works. Somehow. I like messing with code so my code is kinda messy. There is lot of to do, I have few more thing in my mind, I want log more information I want have my dashboards better. I want to drop support for Legacy firmware etc. Only future can tell how it will look.

## Thanks!

Well thanks, if you have any question then hola if you need me. You can also scan this QR code to get my slides.

See ya later.