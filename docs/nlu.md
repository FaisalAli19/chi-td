---
id: nlu
title: NLU (Natural Language Understanding)
sidebar_label: NLU
---

> [IBM Cloud Account](https://console.bluemix.net/registration/) required.

CHI application uses Watson natural-language-understanding and Watson tone analyzer to collect the sentiment and emotions data of the user responses. (refer sample example below)

**User Response**

```
'Love is composed of a single soul inhabiting two bodies. – Aristotle This is love: to fly towards a secret sky, to cause a hundred veils to fall each moment. First to let go of life. Finally, to take a step without feet. – Rumi Can miles truly separate you from friends… If you want to be with someone you love, aren’t you already there? – Richard Bach'
```

**Sentiment, tones and Emotions Data**

```json
sentiment: {"score": 0.945921, "label": "positive"}
emotions: {"sadness": 0.148826, "joy": 0.707453, "fear": 0.015879, "disgust": 0.033806, "anger": 0.115122}
tones: {"confident": 0.712295}
```

### Sentiment and Emotions Data using Watson natural-language-understanding

Watson Natural Language Understanding is a collection of APIs that offer text analysis through natural language processing. This set of APIs can analyze text to help you understand its concepts, entities, keywords, sentiment, and more.

**Following will help to get your API credientials**

- Go to the [Natural Language Understanding](https://console.bluemix.net/catalog/services/natural-language-understanding) page in the IBM Cloud Catalog.
- Log in to your IBM Cloud account.
- Click Create.
- Click Show to view the service credentials.
- Copy the apikey value, or copy the username and password values if your service instance doesn't provide an apikey.
- Copy the url value.

Once you receive the API credientials set the same to NLU_ID and NLU_PASSWORD in .env file.

```
const NaturalLanguageUnderstandingV1 = require("watson-developer-cloud/natural-language-understanding/v1.js");

const natural_language_understanding = new NaturalLanguageUnderstandingV1({
  url: "https://gateway.watsonplatform.net/natural-language-understanding/api",
  username: process.env.NLU_ID,
  password: process.env.NLU_PASSWORD,
  version_date: "2018-03-16"
});
```

In the above code we are calling the Watson NaturalLanguageUnderstandingV1 with the credentials and saving it to varibale natural_language_understanding.

```
 const parameters = {
    text: text,
    features: {
      emotion: {},
      entities: {
        sentiment: true,
        limit: 1
      },
      sentiment: {}
    }
  };

natural_language_understanding.analyze(parameters, (err, response) => {
    if (err) console.log("Sentiment error:", err);
    else {
      sentiment = response.sentiment.document;
      emotions = response.emotion.document.emotion;
			NLU.save({
				sentiment,
				emotions
			})
    }
  });
```

In the above code, we have created the params object and we pass the user response as text with sentiment entity set to true to get the sentiment analysis of the user response from the Watson NLU API. We store the received response in NLU collection.

### Tone Data using Watson tone-analyzer

The IBM Watson Tone Analyzer service is a cognitive linguistic analysis service that detects 7 tones which are most commonly used to detect the tone of written text. These are: anger, fear, joy, sadness, confident, analytical, and tentative.

**Following will help to get your API credientials**

- Create an instance of the Tone Analyzer service and get your credentials:
- Go to the [Tone Analyzer](https://console.bluemix.net/catalog/services/tone-analyzer) page in the IBM Cloud Catalog.
- Log in to your IBM Cloud account.
- Click Create.
- Click Show to view the service credentials.
- Copy the apikey value, or copy the username and password values if your service instance doesn't provide an apikey.
- Copy the url value.

Once you receive the API credientials set the same to TONE_ANALYZER_ID and TONE_ANALYZER_PASSWORD in .env file.

```
const ToneAnalyzerV3 = require("watson-developer-cloud/tone-analyzer/v3");

// Initializing watson tone analyzer api
const tone_analyzer = new ToneAnalyzerV3({
  username: process.env.TONE_ANALYZER_ID,
  password: process.env.TONE_ANALYZER_PASSWORD,
  version_date: "2017-09-21",
  url: "https://gateway.watsonplatform.net/tone-analyzer/api"
});
```

In the above code we are calling the Watson ToneAnalyzerV3 with the credentials and saving it to varibale tone_analyzer.

```
const params = {
    tone_input: { text: text },
    content_type: "application/json"
  };

tone_analyzer.tone(params, (error, response) => {
        // if error console log error
        if (error) console.log("Tone error:", error);
        // else add the response to tone varibale and create a new nlu collection
        else {
          // Declaring empty object to add different tone as a key and score as a value
          const tones = {};
          // Saving data to temp varibale
          const temp = response.document_tone.tones;
          // get only specified tones
          const allowedTones = ["Analytical", "Tentative", "Confident"];
          temp.forEach(({ tone_id, tone_name, score }) => {
            if (allowedTones.indexOf(tone_name) != -1) {
              tones[tone_id] = score;
            }
          });
        }
      });
```

In the above code, we have created the params object and we pass it to the tone function of the tone_analyser. We store the received response in the NLU collection.
