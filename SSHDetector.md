# 📋 **Note:**

This document provides an overview of the `SSH Failed Login Alert + IP Reputation Check` Python script, designed to enhance security monitoring for Linux systems. It details the script's capabilities, setup instructions, and requirements, aiming to help users detect and respond to brute-force SSH attacks more effectively.

-----

# **🚨 SSH Failed Login Alert + IP Reputation Check**

This Python script enhances security by detecting **multiple failed SSH login attempts** from the same IP address in Linux logs (`/var/log/auth.log`). If a configurable threshold of attempts is exceeded within a short time window, the script queries the **IP reputation** from **AbuseIPDB** and generates an **alert**.

-----

## **🌟 Functionalities**

The script offers the following key features:

  * **Parseo de logs `/var/log/auth.log`**: Efficiently reads and processes SSH authentication logs.
  * **Umbral configurable de intentos fallidos**: Allows users to set a custom threshold for failed login attempts before an alert is triggered.
  * **Consulta de reputación vía API de AbuseIPDB**: Integrates with AbuseIPDB's API to check the reputation score of suspicious IP addresses.
  * **Alertas impresas en consola**: Provides immediate notifications directly in the console.

-----

## **🚀 Usage**

To get the script up and running:

1.  **Agrega tu API key en `config.py`**: Ensure you have an AbuseIPDB API key and add it to the `config.py` file.

2.  **Ejecuta**: Run the script from your terminal:

    ```bash
    python main.py
    ```

-----

## **⚙️ Requirements**

Before running the script, make sure you have the following installed:

  * **Python 3.6+**: The script is compatible with Python version 3.6 or newer.

  * **`requests`**: The `requests` library is required for making API calls. Install it using pip:

    ```bash
    pip install requests
    ```
