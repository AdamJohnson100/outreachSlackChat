# outreachSlackChat

*INPUTS: OUTREACH API TOKEN/ OUTREACH WEBHOOK/ SLACK BOT API TOKEN

*SLACK RELEVANT INPUTS: API Refresh token, client_id, client_secret,code

This app will listen for events from Outreach (via webhooks, initially on lead creation)


The first step is defining what you want to be notified on by creating a webhook within the Outreach tool.  Their webhooks API (https://api.outreach.io/api/v2/docs#webhook) enables us to set up a webhook that will page for whenever some action is taken.  The original scope of this design is to notify our team in slack when any event occurs that requires action.

We will need:
1) An Outreach API token
2) Slack bot definition and token

STEPS:

1) Outreach API Token
	In order to get started with the Outreach API, you first need to reach out to their platform team.  There is a 2-step process for getting an Outreach token.  Instructions are listed here: https://api.outreach.io/api/v2/docs#authentication .

Once you have your API token, you can create the webhook in Outreach that fires on event creating. This is the call I made:

***TO BE UPDATED***

```curl https://api.outreach.io/api/v2/webhooks \
	-X POST \ 
	-H "Authorization: Bearer <KEY>" \
	-d action=* \
	-d url="<ROUTE>" \
	-d resource="events" \
	-d 
```

2) To set up our bot in Slack, we must register our bot.

Relevant links: Follow this: https://api.slack.com/docs/working-with-workspace-tokens


Relevant for ME: https://api.slack.com/docs/rotating-and-refreshing-credentials#automatic_expiration

 
