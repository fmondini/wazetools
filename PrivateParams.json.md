# Private parameters file

The `PrivateParams.json` file contains some private keywords that must be provided for the suite to work properly.
The path to this json file is specified in the `SiteCfg.json` file 🠚 object `PrivateParams` 🠚 keywords `devl` and `prod`.

	{
		"debug_user": "username",
		"debug_pass": "password",
		"weblogs_user": "db_username",
		"weblogs_pass": "db_password",
		"gmap_key": "xxxxxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxx",
		"bmap_key": "xxxxx-xxxxxxxxxxxxxxxxxxxxxx_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
		"slack_token": "xoxp-0000000000-0000000000-00000000000-xxxxxxxxxx",
		"recaptcha_key": "xxxxx-XXXXXXXXXXXXXXXXXXXXXXXXX-xxxxxxxx"
	}

| Keyword | Type | Description |
|--|--|--|
| `debug_user` | String | Auto-Login Username in development mode |
| `debug_pass` | String | Auto-Login Password in development mode |
| `weblogs_user` | String | Database Username for WebLogs table *(See note [1])* |
| `weblogs_pass` | String | Database Password for WebLogs table *(See note [1])* |
| `gmap_key` | String | Google Maps API Key |
| `bmap_key` | String | Bing Maps API Key |
| `slack_token` | String | Slack API Token |
| `recaptcha_key` | String | Google ReCaptcha Secret Key |

## Notes

1. The username and password for the `WebLogs` database are only valid for the original hosting site at https://waze.tools/. Any other installations will need to provide the appropriate interfaces. If this is the case, please contact the author.

## Disclaimer

Please be aware that any information you may find on this pages may be inaccurate, misleading, dangerous, addictive, unethical, or illegal.

None of the authors, contributors, vandals, administrators, or anyone else connected with this pages, in any way whatsoever, can be responsible for your use of the informations contained in or linked from these web pages.

**Neither Danisoft Srl nor Fulvio Mondini do not take any responsibility** and we are not liable for any damage caused through use of code, examples, products or services given through this website, be it indirect, special, incidental or consequential damages, including but not limited to damages for loss of business, loss of profits, interruption or the like.

If you need more information take a look at this [Terms and Conditions](https://danisoft.software/home/copyright.jsp) page (in italian).
