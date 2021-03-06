# Explanation

After a survey has been finished by a panelist, we need to be informed about the status he/she has accomplished in order to be able to credit the incentive.<br />
This can be done easily via API as well. There are different types of status which should be distinguished.<br />


# Types of Status

**Complete**<br />
The panelist was able to complete the survey successfully and will be credited by us.<br />
Each complete will be invoiced according to our agreement.<br />

**Screenout**<br />
The panelist did not qualify for the survey since he/she does not belong to the target group(s).<br />
Screening questions should be asked at the beginning of the survey.<br />

**Quotafull**<br />
The panelist did qualify for the survey, however there were already enough completes registered of the panelists group quota.


# Transmission

The status information should be sent to us via JSON/POST to an URL which you will be provided with and should contain the following information:

**IMPORTANT: The URL for status transmission is different to the URL for invite requests.**

Variable | Explanation
--- | ---
status | Values: COMPLETE, SCREENOUT, QUOTAFULL
loi | Length of interview in minutes
project_id | ID of project/survey
country_iso_code | Country ISO Code of project/survey
language | Language of survey
respondent_id | ID of panelist
hash_key | MD5 hash of secret_key, project_id and respondent_id



# Example

```
{
    "status":"COMPLETE",
    "loi":"15",
    "project_id":"12345",
    "country_iso_code":"US",
    "language":"en",
    "respondent_id":"349-1-12345678",
	"hash_key": "Fg2Ed2Nbp9Db5G63ss437"
}
```












