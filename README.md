# Práctica 5 — Servicio TCP de la Capa de Transporte en Node.js

Este repositorio contiene el desarrollo correspondiente a la **Práctica 5+** de la asignatura **Aplicaciones para Comunicaciones en Red (6CV2)**, impartida en la **Escuela Superior de Cómputo (ESCOM)** del **Instituto Politécnico Nacional (IPN)**.  
El trabajo tiene como objetivo implementar un **servicio TCP** en la capa de transporte mediante un **servidor** y un **cliente** programados en **Node.js**, analizando su funcionamiento, la comunicación bidireccional y el flujo de datos utilizando **Wireshark**.

---

## Objetivo

Comprender el funcionamiento del **Protocolo de Control de Transmisión (TCP)** en la capa de transporte del modelo TCP/IP, mediante la creación de aplicaciones cliente-servidor que permitan:
- Establecer una conexión confiable entre dos extremos.  
- Intercambiar mensajes en tiempo real.  
- Analizar el flujo de datos y el control de la comunicación utilizando **Wireshark**:contentReference[oaicite:0]{index=0}.  

---

## Fundamento teórico

El **Protocolo TCP (Transmission Control Protocol)** es un protocolo **orientado a conexión** que garantiza una transmisión **fiable, ordenada y libre de errores** entre dos dispositivos.  
A diferencia de **UDP**, TCP requiere un proceso de conexión previo (3-way handshake) antes de transferir datos, asegurando así que los segmentos lleguen completos y en el orden correcto.  

**Características principales de TCP:**
- Control de flujo mediante ventana deslizante.  
- Confirmación de recepción (`ACK`).  
- Retransmisión en caso de pérdida de paquetes.  
- Cierre controlado de conexión (`FIN/ACK`).  

En esta práctica se utiliza **Node.js** por su capacidad de manejar **E/S asíncrona**, ideal para gestionar múltiples conexiones TCP de manera eficiente:contentReference[oaicite:1]{index=1}.

---

## Desarrollo

La práctica consta de dos componentes: **servidor** y **cliente**, ambos implementados en Node.js usando el módulo **`net`**.  
El servidor escucha conexiones en el puerto **8080** y el cliente se conecta a él para intercambiar mensajes en tiempo real.
