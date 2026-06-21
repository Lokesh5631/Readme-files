# Week 3: Integration with AI API
Have a look at this to get a quick idea of how an API works.  
https://www.youtube.com/watch?v=4ylNDFYH2xs  
We'll be using Gemini API as it is free of cost. Feel free to experiment with other API platforms.  
## Setup
https://ai.google.dev/gemini-api/docs/quickstart 
1. Create an API Key, install the requirements as given.    
2. Copy the API Key and create an environment variable storing it. This can be done by creating a **.env** file in the same folder where your js file exists.  
  ```
  API_KEY = "..." //Your API Key
  ```
3. Run this in your terminal to initialize a project in node js.
```
npm init -y
```
4. A package.json file would have been created. Edit the file, change the type from **"commonjs"** to **"module"**.  
Not doing this would throw an error while running your javascript file, as CommonJS does not allow to use an await keyword without an async wrapper, whereas the Gemini API template requires us to do so.  
5. Run this in your terminal to install dotenv, which would be used to read the API Key from your system environment.
```
npm install dotenv
```
6. Include this in ur js file, this is what reads ur .env file.
```
import dotenv from "dotenv"
dotenv.config()
```
7. Use the generate text template provided in the Gemini API docs in ur js file. Don't forget to include your api key in this line of the template. This is done by extracting the key from the variable you have created in the .env file.

```
const ai = new GoogleGenAI({apiKey: process.env.API_KEY});
```
Display the generated text in a html page.
Try experimenting with different models.
