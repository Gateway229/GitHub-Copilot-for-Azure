**About GitHub Copilot for Azure**

GitHub Copilot for Azure is an extension to the GitHub Copilot Chat interface that lets you interact with Azure, to ask and receive answers to questions about Azure resources within Visual Studio Code. GitHub Copilot for Azure is accessed by using the @azure chat participant in the GitHub Copilot Chat interface. The chat interface provides access to information and support without requiring you to navigate documentation or search online forums. For more information, see  [About GitHub Copilot Chat](https://docs.github.com/en/copilot/responsible-use-of-github-copilot-features/responsible-use-of-github-copilot-chat-in-your-ide#about-github-copilot-chat).

GitHub Copilot for Azure can answer a wide range of Azure-related questions on topics including learning, deploying, troubleshooting, resourcing, costs and more. GitHub Copilot for Azure is not designed to provide general information on topics outside of Azure. 

The primary supported language for GitHub Copilot for Azure is English. 

GitHub Copilot for Azure works by using a combination of natural language processing and machine learning to understand your question and provide you with an answer. This process can be broken down into several steps. 

**Input processing** 

The input prompt from the user is pre-processed by the GitHub Copilot for Azure system, combined with contextual information (for example, Azure subscription that is currently selected), and sent to a large language model. User input is in the form of plain language. 

The large language model will take the prompt, gather additional context (for example repository data in the project folder), and provide a response based on the prompt. The system is only intended to respond to Azure-related questions. 

**Language model analysis** 

The pre-processed prompt is then passed through the Copilot Chat language model, which is a neural network that has been trained on a large body of text data. The language model analyzes the input prompt. 

**Response generation** 

The language model generates a response based on its analysis of the input prompt and the context provided to it. The language model can gather additional context and provide a response based on the prompt. This response can take the form of informational text, instructions for completing a task, tabular information about Azure resources, or code snippets to perform tasks. 

When you use the @azure chat participant and sign in to your Azure account, GitHub Copilot for Azure will be able to gather context from your Azure resources, adhering to the same role-based access controls established in the Azure Portal (enabled by your administrator). 

**Output formatting** 

The response generated by GitHub Copilot for Azure is formatted and presented to the user. GitHub Copilot for Azure may use syntax highlighting, indentation, and other formatting features to add clarity to the generated response. Depending upon the type of question from the user, links to context that the model used when generating a response, such as source documentation, templates or query results, may also be provided. 

GitHub Copilot for Azure is intended to provide you with the most relevant answer to your question. However, it may not always provide the answer you are looking for. Users of GitHub Copilot for Azure are responsible for reviewing and validating responses generated by the system to ensure they are accurate and appropriate. Additionally, as part of our product development process, we undertake red teaming to understand and improve the safety of GitHub Copilot for Azure. Input prompts and output completions are run through content filters. The content filtering system detects and prevents the output on specific categories of content including harmful, offensive, or off-topic content. For more information on improving the performance of GitHub Copilot for Azure, see the section "Improving performance for GitHub Copilot for Azure". 

**Use cases for GitHub Copilot for Azure** 

GitHub Copilot for Azure can help in a variety of Azure scenarios. 

**Answering general questions about Azure** 

GitHub Copilot for Azure uses content from learn.microsoft.com as well as the 3rd party site kubernetes.io to answer users’ questions through a process called retrieval augmented generation (RAG). When a user asks a question that is appropriate to answer with such content, GitHub Copilot for Azure searches an index of the content from those sites, then uses that content in the generation of the response. 

**Answering questions about Azure resources** 

When a user asks a question that is related to deployed Azure resources, GitHub Copilot for Azure will convert the user’s question from natural language to a query compatible with Azure Resource Graph, run the query, and then use the results from the query to generate a response. 

**Deploying sample applications with azd templates** 

GitHub Copilot for Azure can detect when a user is interested in deploying a new application based on an Azure Developer CLI (azd) template. GitHub Copilot for Azure will query the available templates to find one that most closely matches the user’s question and present it to the user, along with instructions for initializing the template on their local machine in preparation for deploying it to Azure. GitHub Copilot for Azure can also instruct the user in how to deploy the application to Azure through use of azd CLI commands. 

**Troubleshooting application issues** 

GitHub Copilot for Azure can detect when a user wants to troubleshoot an application that is deployed in Azure. GitHub Copilot for Azure will collect from the user or from Azure Resource Graph the information necessary to properly identify the application and then call the Diagnostic plugin, which will analyze multiple aspects of the deployed application and resources and return any relevant advice to the user for fixing the issue. 

**Answering questions about Azure costs** 

GitHub Copilot for Azure can answer questions the user may have about the cost of resources that are deployed in Azure.  

**Answering coding questions** 

While not it’s primary purpose, you can ask GitHub Copilot for Azure for help or clarification on specific coding problems and receive responses in natural language format or in code snippet format. 

The response generated by GitHub Copilot for Azure will use the model's training data set to answer your questions. 

The response generated may additionally use search results from learn.microsoft.com or query results from Azure Resource Graph. 

This can be a useful tool for Azure developers, as it can provide guidance and support for common resource questions, deployment tasks and other Azure challenges. 

**Improving performance for GitHub Copilot for Azure** 

GitHub Copilot for Azure can support a wide range of practical applications like answering general questions about Azure resources, finding and deploying application templates, diagnosing issues, deploying applications, and code generation, each with different performance metrics and mitigation strategies. To enhance performance and address some of the limitations of GitHub Copilot for Azure, there are various measures that you can adopt. For more information on the limitations of GitHub Copilot for Azure, see the section "Limitations of GitHub Copilot for Azure." 

**Keep your prompts on topic** 

GitHub Copilot for Azure is intended to address queries related to Azure exclusively. Therefore, limiting the prompt to Azure questions or tasks can enhance the model's output quality. 

**Use GitHub Copilot for Azure as a tool, not a replacement** 

While GitHub Copilot for Azure can be a powerful tool for interacting with Azure and generating code, it is important to use it as a tool rather than a replacement for human programming. You should always review and test the code generated by GitHub Copilot for Azure to ensure that it meets your requirements and is free of errors or security concerns. 

**Use secure coding and code review practices** 

While GitHub Copilot for Azure can generate syntactically correct code, it may not always be secure. You should always follow best practices for secure coding, such as avoiding hard-coded passwords or SQL injection vulnerabilities, as well as following code review best practices, to address GitHub Copilot for Azure’s limitations. 

**Provide feedback** 

If you encounter any issues or limitations with GitHub Copilot for Azure, we recommend that you provide feedback through the share feedback link in the Copilot Chat interface of Visual Studio Code. This can help the developers to improve the tool and address any concerns or limitations. 

**Stay up to date** 

GitHub Copilot for Azure is a new technology and is likely to evolve over time. You should stay up to date with any updates or changes to the tool, as well as any new security risks or best practices that may emerge. Automated extension updates are enabled by default in Visual Studio Code. If you have automatic updates enabled, Copilot Chat will automatically update to the latest version when you open Visual Studio Code. For more information on automatic updates in Visual Studio code, see the Visual Studio Code documentation. 

**Limitations of GitHub Copilot for Azure** 

Depending on factors such as your access to Azure resources and input data, you may experience different levels of performance when using GitHub Copilot for Azure. The following information is designed to help you understand system limitations and key concepts about performance as they apply to GitHub Copilot for Azure. 

**Limited scope** 

For interacting with Azure resources, you can only read information or perform tasks like deploying new resources if you have the access required to do so in the Azure Portal. In addition, there is information available in the Azure Portal may not be available via GitHub Copilot for Azure. 

For code generation, GitHub Copilot has been trained on a large body of code but still has a limited scope and may not be able to handle more complex code structures or obscure programming languages. For each language, the quality of suggestions you receive may depend on the volume and diversity of training data for that language. For example, JavaScript is well-represented in public repositories and is one of GitHub Copilot's best supported languages. Languages with less representation in public repositories may be more challenging for GitHub Copilot to provide assistance with. Additionally, GitHub Copilot can only suggest code based on the context provided, so it may not be able to identify larger design or architectural issues. 

**Potential biases** 

Copilot's training data is drawn from existing code repositories, which may contain biases and errors that can be perpetuated by the tool. Additionally, GitHub Copilot for Azure may be biased towards certain programming languages or coding styles, which can lead to suboptimal or incomplete code suggestions. 

**Security risks** 

GitHub Copilot for Azure can generate code based on the context of the question and any code that is included as context, which can potentially expose sensitive information or vulnerabilities if not used carefully. You should be careful when using GitHub Copilot for Azure to generate code for security-sensitive applications and always review and test the generated code thoroughly. 

**Inaccurate code** 

One of the limitations of GitHub Copilot for Azure is that it may generate code snippets or CLI commands that appear to be valid but may not actually be semantically or syntactically correct or may not accurately reflect the intent of the developer. To mitigate the risk of inaccuracies, you should carefully review and test the generated code and CLI commands, particularly when dealing with critical or sensitive applications. You should also ensure that the generated code adheres to best practices and design patterns and fits within the overall architecture and style of the codebase. 

**Inaccurate responses to non-coding topics** 

GitHub Copilot for Azure is not designed to answer non-Azure questions, and therefore its responses may not always be accurate or helpful in these contexts. If a user asks GitHub Copilot for Azure a non-coding question, it may generate an answer that is irrelevant or nonsensical, or it may simply indicate that it is unable to provide a useful response. 