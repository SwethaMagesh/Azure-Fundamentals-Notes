# [Choose the best AI service for your needs](https://docs.microsoft.com/en-us/learn/modules/ai-machine-learning-fundamentals/)
## Module 2 has 8 units
### UNIT 1: Introduction
- **Prerequisites**
  - Familiarity with the concept of application programming interfaces, or APIs. Programmers use APIs to interact with the functionality that's contained in code libraries.
  - Familiarity with the following additional concepts:
    - **Web API**: An API that's accessible from servers that accept requests via HTTP.
    - **Web API endpoint**: The location of the code library.
    - **REST API**: The design of the URL style that's used to expose the API's functionality.
---
### UNIT 2: Identify the product options
-  A goal of AI is to create a software system that's able to adapt, or learn something on its own without being explicitly programmed to do it
- 2 approaches
  - The first is to employ a **deep learning system** 
    - that's modeled on the **neural network of the human mind**, enabling it to discover, learn, and grow through experience.
  - The second approach is **machine learning**,
    - a **data science technique that uses existing data** to train a model, test it, and then apply the model to new data to forecast future behaviors, outcomes, and trends.
 - SCOPE:  every device or software system that collects textual, visual, and audio data could feed a **machine learning model** that makes that device or software system **smarter** about how it functions in the future.
- **ML**
  - Data -> Train n test model -> _you can deploy and use it in real time via a **web API endpoint**_
  - Even after deploying, feedback or data helps to retune the model
- **Cognitive service**
  - prebuilt machine learning models that enable applications to see, hear, speak, understand, and even begin to reason.
  - Developers access Azure Cognitive Services via APIs and can easily include these features in just a few lines of code.
  - Eg: object recognition, face detection, image to text, sentiment analysis
  - No training data => direct **live data**
  - **Types**
  1. Language
  2. Speech
  3. Decision
  4. Vision
- **Bot service**
  - _**Azure Bot Service and Bot Framework**_ are platforms for creating virtual agents
  - uses other Azure services, such as Azure Cognitive Services, to understand what their human counterparts are asking for.
  - Users converse with a bot by using **text, interactive cards, and speech**
  - _can be a sophisticated conversation that intelligently provides access to services._
---
### UNIT 3: Analyse Design criteria
- **Are you building a virtual agent that interfaces with humans via natural language?**
  - _prebuilt, no-code solutions that cover common scenarios_ Eg. **QnAMaker** - uses FAQ pages, support websites, product manuals, SharePoint documents, or editorial content through an easy-to-use **UI or via REST APIs**
  - _Power Virtual Agents integrates with Microsoft Power Platform_
  - More complex interactions with Microsoft Bot Framework
- **Do you need a service that can understand the content and meaning of images, video, or audio, or that can translate text into a different language?**
  - Choose _Azure Cognitive Services_ 
- **Do you need to predict user behavior or provide users with personalized recommendations in your app?**
  - Choose _Azure Cognitive Services Personalizer service_
  - Another costly option -  capture and store user behavior and create your own custom Azure Machine Learning solution to do these things
- **Will your app predict future outcomes based on private historical data?**
  - Choose Azure Machine Learning
  - with proprietary data, you'll likely need to build a more custom-tailored machine learning model.
- **Do you need to build a model by using your own data or perform a different task than those listed above?**
  - Use _Azure Machine Learning_ for maximum flexibility
---
### UNIT 4: Use ML for decision support 
- Situation
>The Tailwind Traders e-commerce website allows its customers to browse and purchase items that can be delivered or picked up from a retail store nearest to their location. The Marketing team is convinced that it can increase sales dramatically by suggesting add-on products that complement the items in a shopper's cart at the point of checkout. The team could hard-code these suggestions, but it feels that a more organic approach would be to use its years' worth of sales data as well as new shopping trends to decide what products to display to the shopper. Additionally, the suggestions could be influenced by product availability, product profitability, and other factors. The Marketing team's existing data science experts have already done some initial analysis of the problem domain, and have determined that its plan might take months to prototype, and possibly a year to roll out.
  - Will the Tailwind Traders app predict future outcomes based on private historical data? Yes, and that is why in this scenario, Azure Machine Learning is likely the best choice. 
  - The success of this effort would depend primarily on the ability of the model to select precisely the right up-sale products to suggest to the shopper. 
  - Because the model would need to be tweaked and tuned over time, an off-the-shelf model would likely not suffice.
---
### UNIT 5: Use Cognitive services for data analysis
- Situation
>The first generation of the Tailwind Traders e-commerce website was available exclusively in English. However, when the Marketing team sponsored a demographics study for the company's brick-and-mortar locations, it found that, on average, only 80 percent of potential customers speak English. In some neighborhoods, that number falls to 50 percent. The team sees the addition of multiple languages as a wonderful opportunity to serve non-English speakers with the same online e-commerce experience as English speakers.
  - Use Cognitive service 
  - _Azure Cognitive Services Translator service_ specifically
---
### UNIT 6: Use Bot Service for interactive chat applications
- Situation
>The Customer Service team has long asked for a virtual agent to handle the vast majority of questions it gets asked. No matter how prominent it makes the answers to the most frequently asked questions on the website, shoppers are impatient and perceive contact in a chat window as saving them time. 
>The team wants shoppers to feel as though they're interacting with a real human. When it becomes clear that the virtual agent can't provide an answer, the chat session should be transferred to a human.
>Providing a virtual agent would decrease the amount of time it takes for all shoppers to receive answers. The virtual agent could answer most questions, which would free up human customer service agents to provide support for more difficult questions or thorny account-related issues.
  - BOT SERVICE => Customer Service supervisors can test and tweak the answers to continue to refine the chat experience.
  - understand the content and meaning of images, video, audio, or translate text => **prebuilt solutions** like QnA Maker (part of Cognitive Services) or Power Virtual Agents 
  - **_ Any Azure Bot solution would likely implement several Azure Cognitive Services, such as Language Understanding (LUIS) and possibly Translator_**
---
### UNIT 7: Knowledge check
![image](https://user-images.githubusercontent.com/43994542/119233801-3c619680-bb48-11eb-82d8-223a56b6f0e5.png)

---
### UNIT 8: Summary
- Without AI services, Tailwind Traders would spend more time and effort on manual tasks, respond to customers less quickly, offer weak product recommendations, and be unable to fully support customers who speak languages other than English.
  
---

