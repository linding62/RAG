# **3. Setting up the Gemini API key (Colab Secrets)**

## How to get a Gemini API key from Google AI Studio and import it into Colab
*If you already set up your Gemini API key, you can skip to the next section to set up the Gemini Client.

1. Click on the `Key icon` in the left sidebar in Colab. There, you will find a dropdown related to **Gemini API keys**. Click on it, and it will reveal two options: *‘Import key from Google AI Studio’* and *‘Manage keys in Google AI Studio.’* Select the first option, **Import key from Google AI Studio**

![Step 1](assets/Import%20Gemini%20API%20Key%20step%201.png)

2. After clicking, a text box will appear saying **“No keys found.”** In that box, you will see a description along with a link: `Create your first key in Google AI Studio`. Click on this link, and it will take you to the Google AI Studio page.

![Step 1](assets/Import%20Gemini%20API%20Key%20step%202.png)

3. If you have not signed up for Google AI Studio yet, please sign up first. After signing in, on the UI you will find an option called **“API keys.”** Click on it.

![Step 1](assets/Import%20Gemini%20API%20Key%20step%203.png)

4. You will see a default API key already generated. Ignore that—we will create a new one. On the top, you will find an option to **create a new API key**. Click on it.

![Step 1](assets/Import%20Gemini%20API%20Key%20step%204.png)

5. A box will pop up asking you to configure your key details. Name your key **“Business Application of Gen AI MLS.”** For the project, choose **“Default Gemini Project,”** and then click on Create Key.

![Step 1](assets/Import%20Gemini%20API%20Key%20step%205.png)

6. Once the key is generated, copy it and return to your Colab window. There, click on **“Add new secret”**. In the Name field, enter `GEMINI_API_KEY`. In the Value field, paste your Gemini API key.

![Step 1](assets/Import%20Gemini%20API%20Key%20step%206.png)
