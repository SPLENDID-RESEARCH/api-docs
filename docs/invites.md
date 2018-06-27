# Explanation

With Invite Requests you can let us invite panelists to your surveys. Whether it is for a new survey or an already existing one, calling the API will lead to invitations beeing send out by us.<br />
In order to be able to do so we need some information on the survey as well as the participants to be invited.<br />
Since you have access to all panelist and their IDs, each Invite Request should contain the respective Member IDs you have selected.<br />
We also need some information on the survey itself in order to set the project up properly within our system.<br />

# Transmission

The Invite Requests should be sent to us via JSON/POST to an individual URL which you will be provided with and should contain the following information:

**IMPORTANT: The URL for Invite Requests is different to the URL for status transmission.**


Variable | Explanation
--- | ---
project_id | Unique id for this survey
country_iso_code | ISO 3166-2 Country Code
language | ISO 639-1 Language Code
loi | Length of interview in minutes
completes | Overall number of completes needed for the study
supported_devices | Values: “desktop”, “mobile” or “all”
survey_url | URL of survey
respondent_id | Member ID of participant 
unique_url_id | Unique ID for panelist and survey

# Example

```
{
	"project_information": {
		"project_id": "123456",
		"country_iso_code": "US",
		"language": "en",
		"loi": "15",
		"completes": "1000",
		"supported_devices": "all"
	},
	"survey_url": "https://www.example.com",

	"respondents": [{
		"respondent_id": "349-1-123456789",
		"unique_url_id": "tSfpoCXn4RnFLeftnAFc"
	}, {
		"respondent_id ": "B2345559953",
		"unique_url_id ": "HuPhCSiF7Up8R408FRbm"
	}, {
		"respondent_id ": "C2929292929",
		"unique_url_id ": "FkiQ6sw9A7uVK6aqdFZ4"
	}]
}
```












