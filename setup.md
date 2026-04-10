# How to setup OpenClaude in your local ( [YT link](https://www.youtube.com/watch?v=IZoOfNBYHG8) )

## Mac Installation Commands:

1. Download zip for OpenClaude Source Code
2. Determine where you want this application to be permanently installed. Don’t change or move it afterward. Applications folder on mac is good.
3. Unzip and add all the OpenClaude files to this destination folder.
4. Install nodeJS
Get command for your operating system here: https://nodejs.org/en/download

5. Install Bun: 
Get command for your operating system here:
https://bun.com/docs/installation#ins...


6. Open the source code folder in VS Code, Antigravity, or Cursor, and open a terminal.

Run (you can copy these three all at once and paste in):

```sh
npm install 
npm run build 
npm link
```

> This will install the dependencies, then build the application with bun. npm link creates a symlink that will let you run the OpenClaude run command in any folder.


7. Create a test folder and open it up in your IDE. 


8. Open your terminal and paste in your exports, configured with the openrouter model you want.

```sh
export CLAUDE_CODE_USE_OPENAI=1
export OPENAI_BASE_URL="https://openrouter.ai/api/v1"
export OPENAI_API_KEY="openrouter-api-key-here-dont-remove-quotation-marks"
export OPENAI_MODEL="google/gemini-3-flash-preview"
```

9. Run openclaude with `openclaude`


10. Test it to see if it works.


11. Switch models by using /exit, modifying your exports, pasting them back in, and hitting enter and then running openclaude again.

```sh
export CLAUDE_CODE_USE_OPENAI=1
export OPENAI_BASE_URL="https://openrouter.ai/api/v1"
export OPENAI_API_KEY=“openrouter-api-key-here-dont-remove-quotation-marks”
export OPENAI_MODEL=“openrouter-modelname-here”
```

## Windows: 

1. Download zip for OpenClaude Source Code

2. Determine where you want this application to be permanently installed. Don’t change or move it afterward. Applications folder on mac is good.

3. Unzip and add all the OpenClaude files to this destination folder. 


4. Install nodeJS
Get command for your operating system here: https://nodejs.org/en/download

5. Install Bun: 
Get command for your operating system here:
https://bun.com/docs/installation#ins...


6. Windows Specific:

Open PowerShell as Administrator and run this to ensure npm link is allowed to execute:

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

7. Open the source code folder in VS Code, Antigravity, or Cursor, and open a terminal. Ensure you run everything as administrator.

Run (you can copy these three all at once and paste in):

```sh
npm install 
npm run build 
npm link
```

> This will install the dependencies, then build the application with bun. npm link creates a symlink that will let you run the OpenClaude run command in any folder.


8. Create a test folder and open it up in your IDE. 


9. Open your terminal and paste these in, configured with the OpenRouter model you want and your openrouter API key.

```sh
$env:CLAUDE_CODE_USE_OPENAI="1"
$env:OPENAI_BASE_URL="https://openrouter.ai/api/v1"
$env:OPENAI_API_KEY="YOUR_OPENROUTER_KEY_HERE"
$env:OPENAI_MODEL="openrouter-model-here"
```

10. In a terminal, run: `openclaude`