# Waze.Tools Suite Documentation

The Waze.Tools suite is a set of WebApps, written primarily in Java and JSP, designed to simplify the daily work of editors using WME.
They were designed to run under Apache as a web server and Tomcat as an application server (with Java 8), but with small modifications they can also be adapted to other environments.

## Contents of the suite

The suite contains (in alphabetical order):

| App | Title | Description | Web Link |
|--|--|--|--|
| **`AUTH`** | Credential Manager | Credentials and privileges management | https://auth.waze.tools/ |
| **`CIFP`** | Closures Feed Project | Closure and Incident Feed Project (beta) | https://cifp.waze.tools/ |
| **`CMON`** | Italian Cities Monitor | Cities Completion Monitor (Italy only) | https://cmon.waze.tools/ |
| **`CODE`** | Scripts Repository | Scripts repository for devs and editors | https://code.waze.tools/ |
| **`SIGN`** | Forum Signatures | Beautiful icons for forum signatures | https://sign.waze.tools/ |
| **`UREQ`** | Unlock Requests | Manage unlock requests in your area | https://ureq.waze.tools/ |
| **`WEB`** | Home Page | The main entry point to the suite | https://www.waze.tools/ |
| | **Other Sites** |
| **`MAIL`** | WazeItalia WebMail | Access to the `wazeitalia.it` e-Mail domain | https://domino.wazeitalia.it/ |
| | **Inactive Sites** |
| **`AMGR`** | *AM Layers Manager* | *Manage AM areas in your Country* | *(deprecated)* |
| **`MNTR`** | *Mentoring Manager* | *Track editors' skills in your Country* | *(deprecated)* |

## SiteCfg.json

The configuration of each App is found in the `SiteCfg.json` file.
More info about its content in the `SiteCfg.json.md` file.

## PrivateParams.json

"Sensitive" data such as database passwords, tokens or secret keys are stored in the `PrivateParams.json` file.
More info about its content in the `PrivateParams.json.md` file.

## Disclaimer

Please be aware that any information you may find on this pages may be inaccurate, misleading, dangerous, addictive, unethical, or illegal.

None of the authors, contributors, vandals, administrators, or anyone else connected with this pages, in any way whatsoever, can be responsible for your use of the informations contained in or linked from these web pages.

**Neither Danisoft Srl nor Fulvio Mondini do not take any responsibility** and we are not liable for any damage caused through use of code, examples, products or services given through this website, be it indirect, special, incidental or consequential damages, including but not limited to damages for loss of business, loss of profits, interruption or the like.

If you need more information take a look at this [Terms and Conditions](https://danisoft.software/home/copyright.jsp) page (in italian).
