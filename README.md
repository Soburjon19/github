<p align="center">
    <img src="asset/logo.svg" height="150">
</p>

<h1 align="center">Github Readme Activity Graph</h1>

<a href="https://jb.gg/OpenSourceSupport">
<p align="center">
    <img src="https://resources.jetbrains.com/storage/products/company/brand/logos/jb_beam.svg" height="150">
</p>
</a>
<h3 align="center"><a href="https://jb.gg/OpenSourceSupport">Supported by JetBrains</a></h3>
A dynamically generated activity graph to show your GitHub activities of last 31 days.

## Table of contents

- [Table of contents](#table-of-contents)
- [How to Use](#how-to-use)
  - [Attention ⚠](#attention-)
- [Use themes](#use-themes)
- [Available Themes](#available-themes)
- [Customization](#customization)
  - [Common Options](#common-options)
- [Deploy on your own Aws instance](#deploy-on-your-own-heroku-instance)
  - [Step-by-step instructions for deploying to Aws **(from UI)**](#step-by-step-instructions-for-deploying-to-heroku-from-ui)
  - [Step-by-step instructions for deploying to Aws **(from CLI)**](#step-by-step-instructions-for-deploying-to-heroku-from-cli)
- [Deploy on your own Replit instance](#deploy-on-your-own-replit-instance)
  - [Step-by-step instructions for deploying to Replit **(from UI)**](#step-by-step-instructions-for-deploying-to-replit-from-ui)
- [Contributing](#contributing)
<!-- - [Core Team 💻](#core-team-) -->
<!-- - [Contributors ✨](#contributors-) -->
- [Resources Used to build this project](#resources-used-to-build-this-project)
  - [Made with ❤ and TypeScript <img src="https://www.vectorlogo.zone/logos/typescriptlang/typescriptlang-icon.svg" width="25">](#made-with--and-typescript-)

## How to Use

Just paste the following URL in your profile readme and you are good to go.

**Pass your `username` in the URL**

```md
[![soburjon's github activity graph](https://master.d1wlzgoxcnlxwr.amplifyapp.com/graph?username=Soburjon19)](https://github.com/Soburjon19/github)
```

### [Attention ⚠](#Deploy-on-your-own-aws-amazon-instance)

## Use themes

_`username=Soburjon19&theme=theme_name`_

```md
[![Soburjon's github activity graph](https://master.d1wlzgoxcnlxwr.amplifyapp.com/graph?username=Soburjon19&theme=dracula)](https://github.com/Soburjon19/github)
```

[Manual Customization](#customization) is also available

## Available Themes

|            Name            |                          Preview                            |
| :------------------------: | :--------------------------------------------------------:  |
| **Default (cotton candy)** |  <img src="./asset/default.svg" height=250 alt="graph"/>    |
|         **react**          | <img src="./asset/react.png" height=250 alt="graph"/>       |
|       **react-dark**       | <img src="./asset/react-dark.svg" height=250 alt="graph"/>  |
|         **github**         |   <img src="./asset/github.svg" height=250 alt="graph"/>    |
|         **xcode**          |   <img src="./asset/xcode.svg" height=250 alt="graph"/>     |
|         **rogue**          |   <img src="./asset/rogue.svg" height=250 alt="graph"/>     |
|         **merko**          |   <img src="./asset/merko.png" height=250 alt="graph"/>     |
|          **vue**           |   <img src="./asset/vue.png" height=250 alt="graph"/>       |
|       **tokyo-night**      |<img src="./asset/tokyo-night.png" height=250 alt="graph"/>  |
|       **high-contrast**    |<img src="./asset/high-contrast.png" height=250 alt="graph"/>|

For more themes click [here](https://github.com/Soburjon19/github/blob/master/THEMES.md)

## Customization

Customize the appearance of your Activity Graph however you want with URL params.

#### Common Options

|   Arguments    |                  Description                  |       Type of Value        |
| :------------: | :-------------------------------------------: | :------------------------: |
|   `bg_color`   |            card's background color            |   hex code (without `#`)   |
|    `color`     |            graph card's text color            |   hex code (without `#`)   |
| `title_color`  |            graph card's title color           |   hex code (without `#`)   |
|     `line`     |              graph's line color               |   hex code (without `#`)   |
|    `point`     |         color of points on line graph         |   hex code (without `#`)   |
|  `area_color`  |       color of the area under the graph       |   hex code (without `#`)   |
|     `area`     |          shows area under the graph           | boolean (default: `false`) |
| `hide_border`  |   makes the border of the graph transparent   | boolean (default: `false`) |
|  `hide_title`  |       sets the title to an empty string       | boolean (default: `false`) |
| `custom_title` |          set the title to any string          |           string           |
|    `theme`     | name of [available themes](#available-themes) |           string           |
|   `radius`     |            border radius of graph             |  number (0-16 inclusive)   |

⚠ **For `custom_title` please make sure that you are using %20 for spaces**

Example:

**`custom_title=This%20is%20a%20title`**

```md
[![Soburjon's github activity graph](https://master.d1wlzgoxcnlxwr.amplifyapp.com/graph?username=Soburjon19&custom_title=This%20is%20a%20title&hide_border=true)](https://github.com/Soburjon19/github)
```

**Example:**

```md
[![Soburjon's github activity graph](https://master.d1wlzgoxcnlxwr.amplifyapp.com/graph?username=Soburjon19&bg_color=fffff0&color=708090&line=24292e&point=24292e&area=true&hide_border=true)](https://github.com/Soburjon19/github)
```

## Deploy on your own Heroku instance

The GitHub API only allows limited requests per hour, my https://master.d1wlzgoxcnlxwr.amplifyapp.com/graph could possibly hit the rate limiter. If you host it on your own Heroku server, then you don't have to worry about anything.

You may use the server used by this project at <https://master.d1wlzgoxcnlxwr.amplifyapp.com/> and pass in your username to access your graph.
E.g. `https://master.d1wlzgoxcnlxwr.amplifyapp.com/graph?username=<your_username>`

However, if there are a large number of requests or if the Aws Amplify account being used for the project runs out of dyno hours your graph will not load.

### Step-by-step instructions for deploying to Aws Amplify (from UI)

1. Sign in to Heroku or create a new account at <https://aws.amazon.com/>
2. Click the Deploy button below

<p align="center">
    <a href="https://signin.aws.amazon.com/signin?redirect_uri=https%3A%2F%2Fconsole.aws.amazon.com%2Fconsole%2Fhome%3FhashArgs%3D%2523%26isauthcode%3Dtrue%26nc2%3Dh_ct%26src%3Dheader-signin%26state%3DhashArgsFromTB_ap-northeast-1_9b43b206f800906e&client_id=arn%3Aaws%3Asignin%3A%3A%3Aconsole%2Fcanvas&forceMobileApp=0&code_challenge=zn0Gx3u_Cj0Qeq_nVIfslJe-bw6kWUdo6BY1skQeDeo&code_challenge_method=SHA-256">
        <img width="100px;" hight="10px" src="https://velog.velcdn.com/images/minj_shalom/post/2283659c-430d-4a25-92a8-7ec3494ed48f/image.jpeg" title="Deploy to Heroku" alt="Deploy"/>
    </a>
</p>

3. On the page that comes up, click "**Deploy App**" at the end of the form
4. Once the app is deployed, click "**Manage App**" to go to the dashboard
5. Visit the "**Settings**" tab and click "**Reveal Config Vars**"
6. Visit [this link](https://github.com/settings/tokens/new?description=GitHub%20Readme%20Activity%20Graph) to create a new Personal Access Token
7. Scroll to the bottom and click "**Generate token**"
8. Add the token as a Config Var with the key `TOKEN`

![TOKEN](./asset/token-config.png)

9. Scroll down to the Domains section to find the URL you will use in place of `https://master.d1wlzgoxcnlxwr.amplifyapp.com/`

### Step-by-step instructions for deploying to AWS Amplify (from CLI)

1. Make a [AWS Amplify](https://signup.aws.amazon.com/) account.
2. Install the AWS Amplify CLI
   - Mac: [Find the Mac installer here](https://d2td7dqidlhjx7.cloudfront.net/prod/global/osx/WorkSpaces.pkg)
   - Ubuntu: `sudo snap install aws --classic`
   - Windows: [Find the Windows installer here](https://d2td7dqidlhjx7.cloudfront.net/prod/global/windows/Amazon+WorkSpaces.msi/)
3. Clone the repository: `git clone https://github.com/Soburjon19/github.git`
4. Navigate in to the directory: `cd github`
5. Login to Aws: `AWS Amplify login`
6. Create Aws app: `AWS Amplify create` and copy the URL you are given as output.
7. Deploy app to AWS: `git push AWS Amplify master`
8. [Generate personal access token](https://github.com/settings/tokens). Copy your token.
9. Set token as heroku config var: `AWS Amplify config:set TOKEN=<your token goes here>`

Now just add the following to your profile readme and you're good to go.

```md
![Github Activity Graph](<url from step 6>/graph?username=<username>)
```

## Deploy on your own Replit instance

### Step-by-step instructions for deploying to Replit (from UI)

1. Sign in to Replit or create a new account at https://replit.com
2. Click the Deploy button below

<p align="center">
<a href="https://repl.it/github/Soburjon19/github">
  <img alt="Run on Repl.it" src="https://repl.it/badge/github/Soburjon19/github" style="height: 40px; width: 190px;" />
</a></p>

3. On the page that comes up, choose language as `Node.js` and then click `Import from GitHub` Button

<!-- ![Replit](./asset/replit1.png) -->

4. Visit the "**Settings**" tab and click "**Reveal Config Vars**"
5. Visit [this link](https://github.com/settings/tokens/new?description=GitHub%20Readme%20Activity%20Graph) to create a new Personal Access Token
6. Scroll to the bottom and click "**Generate token**"
7. Wait clone done and add `Secrets` with your `Github token`

<!-- ![Secrets](./asset/replit2.png) -->

8. Click the green `RUN` button on top, the console will run and at last the url will shows on the right
9. Now just add the following to your profile readme and you're good to go

```
![Github Activity Graph](<url from step 5>/graph?username=<username>)
```

## Contributing

Please read through our [contributing guidelines](https://github.com/Soburjon19/github/blob/master/CONTRIBUTING.md). Directions are included for opening issues, coding standards, and notes on development.
<!-- 
## Core Team 💻

<table>
    <tr>
        <td align="center">
        <a href="http://github.com/Ashutosh00710">
            <img src="https://avatars.githubusercontent.com/u/42907572?s=460&u=3c5c03fdddeec2483819b845bd549616d48b71e5&v=4" width="100px;" alt=""/>
            <br />
            <sub><b>Ashutosh Dwivedi</b></sub>
        </a>
        <br />
        <a href="#projectManagement" title="Project Management">📆</a>
        <a href="https://github.com/Ashutosh00710/github-readme-activity-graph/commits?author=ashutosh00710" title="Code">💻</a>
        <a href="#documentation" title="Documentation">📖</a>
        <a href="#ideas" title="Ideas & Planning">🤔</a>
        <a href="#testing" title="Testing">⚠</a>
    </td>
    <td align="center">
        <a href="http://github.com/kshitij978">
            <img src="https://avatars.githubusercontent.com/u/42491256?s=460&u=db0c5e26632c9f4917db50e714cd7552c1559ba8&v=4" width="100px;" alt=""/>
            <br />
            <sub><b>Kshitij Srivastava</b></sub>
        </a>
        <br />
        <a href="#projectManagement" title="Project Management">📆</a>
        <a href="https://github.com/Ashutosh00710/github-readme-activity-graph/commits?author=kshitij978" title="Code">💻</a>
        <a href="#documentation" title="Documentation">📖</a>
        <a href="#design" title="Design">🎨</a>
    </td>
    </tr>
</table>
 -->

<!-- 

## Resources Used to build this project

|      Purpose       |  Library Name   |                   Link                    |
| :----------------: | :-------------: | :---------------------------------------: |
| Graph Construction | **CHARTIST.JS** | <https://github.com/Soburjon19/> |

</br>
<hr/>

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Ashutosh00710/github-readme-activity-graph&type=Timeline)](https://star-history.com/#Ashutosh00710/github-readme-activity-graph&Timeline)

-->

### Made with ❤ and TypeScript <img src="https://www.vectorlogo.zone/logos/typescriptlang/typescriptlang-icon.svg" width="25">
