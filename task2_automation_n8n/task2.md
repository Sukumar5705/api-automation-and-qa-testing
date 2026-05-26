# Task 2 – n8n API Integration Workflow

## Overview
This workflow was built using n8n to automate cryptocurrency market monitoring using CoinGecko APIs and Telegram notifications.

## APIs Used
- CoinGecko API
- Telegram Bot API

## Workflow Logic
1. Schedule Trigger runs every hour.
2. Workflow fetches cryptocurrency market data from CoinGecko.
3. Top 5 cryptocurrency data is filtered using a Code node.
4. A second API request fetches detailed Bitcoin market data.
5. IF condition checks whether Bitcoin price dropped more than 5% in the last 24 hours.
6. If condition is true, a Telegram alert message is sent automatically.

## Error Handling
HTTP Request nodes use “Continue On Fail” to prevent workflow crashes and improve reliability.

## Technologies Used
- n8n
- CoinGecko API
- Telegram Bot
