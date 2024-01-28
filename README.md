# Sabath-and-Jewish-Holidays-Data-Project
This Python project aims to provide a comprehensive solution for developers seeking Jewish holiday and Sabbath data. Leveraging APIs, JSON, and Google Cloud Platform (GCP) connections, this tool facilitates easy integration of Jewish religious data into projects that involve global timeframes.
HabCal (Hebrew Calendar) API documentations and notes, as well as additional more broad highlights and other sources for this project will be provided.

## Table of Contents

- [About the Project](#about-the-project)
- [Important Prerequisites](#important-prerequisites)
- [Google Cloud Platform Application](#google-cloud-platform-application)
  - [IAM & Credentials](#iam--credentials)
  - [Service Account](#service-account)
  - [Writing Cloud Function](#writing-cloud-function)
- [Code Structure](#code-structure)
  - [Geographical IDs](#geographical-ids)
    - [Israeli](#israeli)
    - [Global](#global)
  - [Translation Methods](#translation-methods)
- [Google Sheets Connectivity](#google-sheets-connectivity)
- [Cloud Operation Recap & Conclusion](#cloud-operation-recap--conclusion)


## About the Project

The Jewish Holidays Integration Project is designed to assist developers in seamlessly incorporating Jewish holidays data into their projects. This comprehensive dataset includes essential information such as Shabbat entrance and exit times, "Parashat HaShavua" (weekly Torah portion with English translation), entrance and exit times for various holidays, "Rosh Hodesh" (New Moon) details with English translation, English-Hebrew translations, global and local geographical IDs for cities and countries, and a fundamental understanding of the Shabbat entrance time difference around the world due to sunrise and sunset factors.

Key Features 
* Shabbat Times: Access precise Shabbat entrance and exit times, crucial for applications requiring accurate scheduling aligned with Jewish observances.
* Parashat HaShavua: Retrieve the weekly Torah portion along with its English translation, facilitating the integration of relevant religious content into your project.
* Holiday Timings: Obtain entrance and exit times for major Jewish holidays, enabling applications to incorporate holiday-specific features and functionalities.
* Rosh Hodesh Information: Access details about the New Moon celebration, including English translations, to enrich your project with cultural and religious content.
* English-Hebrew Translations: Integrate translation capabilities to seamlessly switch between English and Hebrew within your application.
* Geographical IDs: Utilize global and local geographical IDs for cities and countries, ensuring accurate localization and customization based on geographic locations.
* Shabbat Time Variations: Understand the differences in Shabbat entrance times worldwide due to variations in sunrise and sunset, allowing your application to adapt to regional practices.
* How to Use Integration: Easily integrate the provided data into your project to enhance its cultural and religious features.
* Localization: Leverage geographical IDs for accurate localization, providing users with personalized content based on their location.
* Customization: Tailor your application to observe Jewish holidays, Shabbat times, and cultural events, fostering inclusivity and diversity.
* Language Support: Implement English-Hebrew translations to make your application accessible and user-friendly for both English and Hebrew-speaking audiences.
Explore the Jewish Holidays Integration Project to bring a rich cultural and religious experience to your application, fostering a deeper connection with users who observe Jewish traditions.




