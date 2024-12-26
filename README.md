---
title: "crypto-TFM"
type: "project"
tags: MBIT, lambda, AWS, S3, python, prefect, athena, power bi

---

# Crypto currencies analysis and perdiction model for Bitcoin.
This is the final project of my master in Data Engineering. This is a group project made by a group of 4 students from Data Science course, and myself who studied the Data Engineering course. The language of the final project is in spanish as our school is a spanish school but I will explain in english the part of the project that I was responsible for: design and development of the project architecture.

The architecture consists on:
- Daily ETLs built with AWS Lambda that use Twitter and Binance public APIs to load them into csv files in our datalake in S3.
- The ETLs have been orchestrated with Prefect.
- S3 buckets is organized in different folders depending on the type of cryptocurrency.
- This bucket will be used by the data scientists to perform their analysis and build their models. Data Scientists also used two other public APIs from the FRED (Federal Reserve Economic Data) and GlassNode to enrich their models.
- Since we wanted to be able to visualize the cryptocurrency data stored in S3, we used Athena crawler to create the different tables from our csv files in S3.
- Once we have the tables in Athena, we used Power BI to show both the most interesting information from each of the crypto currencies and also the results from the models of our Data Scientists.

You can seee a diagram of the architecture in the following image.

![image](https://github.com/aalferea91/cryptoTFM/assets/92360704/1f4774f9-a38b-49c8-a59e-216d08676ef4)

If you want to read (in spanish) the full description of the project, you can find it in the following link: [Memoria_crypto_final.pdf](https://github.com/aalferea91/cryptoTFM/files/12388270/Memoria_crypto_final.pdf)
