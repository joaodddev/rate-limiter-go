# Distributed Rate Limiter in Go

Este é um projeto de microserviço de infraestrutura que implementa um **Rate Limiter distribuído** utilizando Go e Redis. O objetivo é proteger APIs contra picos de tráfego e abusos (DoS/Brute Force).

## 🚀 Tecnologias
- **Go 1.2x**
- **Redis** (Armazenamento distribuído de contadores)
- **Docker & Docker Compose**
- **Algorithm:** Fixed Window Counter

## 🛠️ Como Funciona
O middleware intercepta as requisições HTTP e utiliza o Redis para rastrear o número de solicitações por IP dentro de uma janela de tempo definida. Se o limite for excedido, o serviço retorna um status `429 Too Many Requests`.

## 📋 Pré-requisitos
- Docker instalado
- Go instalado (opcional, se rodar via Docker)
