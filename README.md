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

## Important Prerequisites
Before deploying the Jewish Holidays Integration Project as a Google Cloud Function in a Python environment, ensure the following prerequisites are met: 
* Python Environment (Both for Testing on-prem and in your GCP Cloud Functions enviorenement): Google Cloud Functions support Python.
  Confirm that your script is compatible with the version of Python supported by Google Cloud Functions.
* Required Libraries: Include the necessary libraries in your Google Cloud Functions deployment. These can be specified in the requirements.txt file. Ensure these libraries are compatible with Google Cloud Functions and are available in the Python environment.
* Add the following lines to your requirements.txt file:
    pandas,
    gspread
    requests
* Google Cloud Platform (GCP) Credentials: Set up the necessary Google Cloud credentials. Ensure the service account associated with your Cloud Function has the required permissions, including access to Google Sheets and the ability to make outbound requests to 'https://www.hebcal.com/'.
* Set the GCP service account key as an environment variable within the Cloud Function.
* Google Sheets: Create a Google Sheets document to store the Jewish holidays data. Share the document with the GCP service account associated with the Cloud Function.
* API Access: Confirm that the Cloud Function environment allows outbound requests to 'https://www.hebcal.com/' for fetching data from the API.
* Cloud Pub/Sub: Set up a Cloud Pub/Sub environment in your GCP project.
* Create a Pub/Sub topic that will trigger the Cloud Function.
* Ensure that the Cloud Function is configured to be triggered by the Pub/Sub topic.
* Additional Files: If there are additional Python files or configurations required (e.g., 'shabat_params_v2.py'), ensure these files are included in the deployment package.
* City Translations: Provide translations for city names in the 'trans_geo_names' and 'inter_trans_geo_names' dictionaries, ensuring proper mapping for accurate data representation.
* Data Deployment: If you plan to update a Google Sheets document with the data, ensure the document URL is correctly specified within the script or as an environment variable in the Cloud Function.
* Execution Permissions: Confirm that the Cloud Function has the necessary execution permissions.
* Validate that the Cloud Function service account has the required roles to interact with Google Sheets, Pub/Sub, and other relevant services.




