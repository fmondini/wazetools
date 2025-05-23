# App configuration file and its file structure

Each App has a main configuration file called `SiteCfg.json` located in its `WEB-INF` directory.
See each App's `README.md` file for details and keywords used.

## Generic Parameters

	"Globals": {
		"cookie": true
	}

| Keyword | Type | Description |
|--|--|--|
| `cookie` | boolean | **true**: Include cookies management script |

## Private Parameters JSON File Location

	"PrivateParams": {
		"devl": "C:/path/to/json/file/on/development/workstation/PrivateParams.json",
		"prod": "/path/to/json/file/on/production/server/PrivateParams.json"
	}

| Keyword | Type | Description |
|--|--|--|
| `devl` | String | Full path of file in development environment |
| `prod` | String | Full path of file in production environment |

## Top AppBar Configuration

	"TopAppBar": {
		"enabled": true,
		"drawer": [
			{ "only_if_logged": false, "text": "Bugs (Issue Tracker)", "icon": "bug_report", "link": "https://github.com/fmondini/wazetools-www/issues", "colr": "#007dc1", "dest": "_blank" },
			{ "only_if_logged": false, "text": "Condizioni d'uso", "icon": "copyright", "link": "https://danisoft.software/home/copyright.jsp", "colr": "#007dc1", "dest": "_blank" },
			{ "only_if_logged": true, "text": "", "icon": "", "link": "", "colr": "", "dest": "" },
			{ "only_if_logged": false, "text": "About...", "icon": "info_outline", "link": "../home/about.jsp", "colr": "", "dest": "" }
		]
	}

| Keyword | Type | Description |
|--|--|--|
| `enabled` | boolean| **true**: TopAppbar is enabled |
| `drawer` | JSONArray| Array of items in drawer. See below. |
| | `only_if_logged` | *(boolean)* **true**: Item is shown only if user i logged in |
| | `text` | *(String)* Item text |
| | `icon` | *(String)* Item icon name *(See https://fonts.google.com/icons?icon.set=Material+Symbols)* |
| | `link` | *(String)* Item destination when clicked |
| | `colr` | *(String)* Item color *(in hex value)* |
| | `dest` | *(String)* Item link destination *(use **_blank** to open in new window)* |

## Page Header Configuration

	"Header" : {
		"enabled": true,
		"space_up_class": "DS-padding-top-16px",
		"space_dn_class": "DS-padding-bottom-0px",
		"drop_shadow": false,
		"show_separator": false
	}

| Keyword | Type | Description |
|--|--|--|
| `enabled` | boolean| **true**: Header is enabled |
| `space_up_class` | String | Spacer class to add before header. Must exists in `/_common/default.css` |
| `space_dn_class` | String | Spacer class to add after header. Must exists in `/_common/default.css` |
| `drop_shadow` | boolean| **true**: Drop a shadow under the header |
| `show_separator` | boolean| **true**: Draw a line below the header |

## Page Footer Configuration

	"Footer": {
		"enabled": true,
		"space_up_class": "DS-padding-top-8px",
		"space_dn_class": "DS-padding-bottom-8px"
	}

| Keyword | Type | Description |
|--|--|--|
| `enabled` | boolean| **true**: Footer is enabled |
| `space_up_class` | String | Spacer class to add before footer. Must exists in `/_common/default.css` |
| `space_dn_class` | String | Spacer class to add after footer. Must exists in `/_common/default.css` |

## About Page Configuration

	"About": {
		"ethernet": "eth0",
		"srv_ping": "server.fqdn.net",
		"srv_traf": "server.fqdn.net",
		"srv_temp": "server.fqdn.net",
		"proprietary_license": false
	}

| Keyword | Type | Description |
|--|--|--|
| `ethernet` | String | Public IP ethernet name *(leave empty to disable all graphs)* |
| `srv_ping` | String | Server FQDN for the Latency graph |
| `srv_traf` | String | Server FQDN for the Traffic graph |
| `srv_temp` | String | Server FQDN for the Temperature graph |
| `proprietary_license` | boolean| **true**: Danisoft standard license - **false**: Apache 2.0 license |

## Google Analytics Configuration

	"GoogleAnalytics": {
		"id": "G-XXXXXX0YYY"
	}

| Keyword | Type | Description |
|--|--|--|
| `id` | String | Google Analytics ID *(leave empty to disable)* |

## Temporary Operating System Commands Configuration

	"BashQueue": {
		"bash_script_file": "/tmp/WazeToolsTempCmd.sh"
	}

| Keyword | Type | Description |
|--|--|--|
| `bash_script_file` | String | Temporary name of the bash script to be used in local processes |

## Mail Server Configuration

	"Smtp": {
		"enabled": true,
		"debug": false,
		"host": "localhost",
		"port": "25",
		"protocol": "smtp",
		"from": "noreply@waze.tools"
	}

| Keyword | Type | Description |
|--|--|--|
| `enabled` | boolean| **true**: SMTP is enabled |
| `debug` | boolean| **true**: Generate additional information *(for debugging purposes only)* |
| `host` | String | FQDN of the SMTP server *(usually `localhost`)* |
| `port` | String | Port of the SMTP server *(usually `25`)* |
| `protocol` | String | Protocol used by the SMTP server *(usually `smtp`)* |
| `from` | String | Sender mail address *(usually `noreply@waze.tools`)* |

## Database Configuration

	"MySQL": {
		"enabled": true,
		"class": "com.mysql.cj.jdbc.Driver",
		"schema": "Schema_Name_Here",
		"params": [
			"useSSL=false",
			"jdbcCompliantTruncation=false",
			"serverTimezone=Europe/Rome",
			"allowPublicKeyRetrieval=true"
		],
		"devl": {
			"host": "localhost",
			"port": 3306,
			"user": "Username_Here",
			"pass": "Password_Here"
		},
		"prod": {
			"host": "localhost",
			"port": 6446,
			"user": "Username_Here",
			"pass": "Password_Here"
		}
	}

| Keyword | Type | Description |
|--|--|--|
| `enabled` | boolean| **true**: MySQL is enabled |
| `class` | String | JDBC Driver class name *(usually `com.mysql.cj.jdbc.Driver`)* |
| `schema` | String | Database Schema name |
| `params` | JSONArray | Database parameter string elements |
| `devl` | JSONObject | Development parameters |
| | `host` | *(String)* Development Host FQDN *(usually `localhost`)* |
| | `port` | *(int)* Development Host MySQL port *(usually `3306`)* |
| | `user` | *(String)* Development Host Username |
| | `pass` | *(String)* Development Host Password |
| `prod` | JSONObject | Production parameters |
| | `host` | *(String)* Production Host FQDN |
| | `port` | *(int)* Production Host MySQL port *(usually `3306` for a local db or `6446` for a clustered db)* |
| | `user` | *(String)* Production Host Username |
| | `pass` | *(String)* Production Host Password |

## Disclaimer

Please be aware that any information you may find on this pages may be inaccurate, misleading, dangerous, addictive, unethical, or illegal.

None of the authors, contributors, vandals, administrators, or anyone else connected with this pages, in any way whatsoever, can be responsible for your use of the informations contained in or linked from these web pages.

**Neither Danisoft Srl nor Fulvio Mondini do not take any responsibility** and we are not liable for any damage caused through use of code, examples, products or services given through this website, be it indirect, special, incidental or consequential damages, including but not limited to damages for loss of business, loss of profits, interruption or the like.

If you need more information take a look at this [Terms and Conditions](https://danisoft.software/home/copyright.jsp) page (in italian).
