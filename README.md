# GPT-VocalAssistant-vscode

## Description

Plugin for vs code that will be your assistant.
This plugin allows you to listen from the microphone and perform actions. What will be said must be transformed into text and sent to an AI via API.
The APIs initially supported will be those of OpenAI's ChatGPT and those of GPT4All.
The AI will then have to understand the request and return a response or an action to take.

Examples of requests:
- create a file with name my_nations.txt and the content must be the list of all the countries where Spanish is spoken
- in which file do you hash a string?
- move the function calculateDiscount from the input.js file to the discount.js file
- cancel the modification.

The AI must also get as input the list of open files/files contained in the open folder in vs code.
Furthermore, when opening the folder, a check of the content of each file must be performed.
It must have a history of the actions performed.
A cache should be created.



## Steps

- [ ] Create a new extension for Visual Studio Code.
Set the necessary dependencies for the plugin (OpenAI packages for interacting with the ChatGPT and GPT4All APIs).

- [ ] Use the Visual Studio Code API to capture audio input from the microphone.
Transform audio into text using a speech recognition engine (e.g. using a Node.js package like 'node-record-lpcm16' and Google Cloud Speech-to-Text APIs).
Get the resulting text and send it to the ChatGPT and GPT4All APIs for processing.

- [ ] Use the libraries or packages provided by OpenAI to connect to the respective APIs.
Send input text to the ChatGPT and GPT4All APIs to get a response or an action to take.
Manage responses received from APIs.

- [ ] Use the Visual Studio Code API to get the list of files in the folder opened in the editor.
Check the contents of each file if necessary, for example by looking for the presence of certain specific strings or patterns.
Maintain an updated list of files and their contents to enable the AI to search and make decisions based on that information.

- [ ] Implement a mechanism to track the actions performed by the user and the AI.
Store the history of actions in a cache or local database, so that you can access and consult previous actions when needed.
Provide an interface to view the history of actions so that previous actions can be redone or undone if required.
