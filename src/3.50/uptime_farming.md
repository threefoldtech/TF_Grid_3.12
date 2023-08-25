<h1> Farming Rewards Based on Uptime </h1>

<h2> Table of Contents </h2>

- [Introduction](#introduction)
- [Simple Uptime Level](#simple-uptime-level)
- [Different Uptime Levels](#different-uptime-levels)

## Introduction

Here are two propositions for TFGrid 3.50 farming rewards based on uptime. We welcome the community to give their input.

Note that the first proposition would be way easier to implement.

## Simple Uptime Level

We propose a simple system based on only one level:

* As a general consideration, low uptime nodes won't be selected for utilization
* We propose that any nodes with less than 70% uptime do not farm any token
* Nodes with more than 70% utilization farm tokens proportional to their time online
* The logic is that nodes with high uptime will be more in demand and thus generate more revenues

## Different Uptime Levels

We propose a system based on different levels:

* Rewards based on uptime:
  * Below 95%
    * You do not farm any token 
  * Between 95 and 98%
    * You get proportional rewards with a rewards factor of 0.9
  * Over 98%
    * You get proportional rewards
  * Over 99.8%
    * You get full period rewards
    * After 3 consecutive months, your node is 
      * Certified as HA bandwidth node on the TF Dashboard 
      * The next months, you farm more TFT (factor 1.1)

| **Uptime Window (%)** | **Receive Rewards** | **Rewards Quantity** | **Rewards factor** | **3-Months Mention** |
| --------------------- | ------------------- | -------------------- | ------------------ | -------------------- |
| 99.8 >                | Yes                 | Full Period Rewards  | 1                  | HA Bandwidth         |
| 98 >                  | Yes                 | Proportional Rewards | 1                  |                      |
| 95 >                  | Yes                 | Proportional Rewards | 0.9                |                      |
| < 95                  | No                  | No rewards           | 0                  |                      |