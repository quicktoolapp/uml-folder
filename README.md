# uml-folder

## Prompts

### General UML prompt

```text
"I need a UML sequence diagram for a process in a web application involving interactions between various components: Front-End (FE), Back-End (BE), Facebook Service (FB Service), Database (DB), and Facebook API (FB API). Here's the workflow:

The Front-End sends a request to the Back-End with a bearer token.
The Back-End finds the corresponding Facebook access token for the user.
After parsing the access token, the Back-End requests the Facebook Service to check for saved ad accounts.
The Facebook Service then loops through each non-saved ad account and performs the following actions:
Calls the Facebook API to get ad campaigns.
Saves the ad campaigns to the Database.
For each non-saved ad campaign, the Facebook Service:
Calls the Facebook API to get ad sets.
Saves the ad set details to the Database.
After completing the ad campaign and ad set retrieval, the Back-End requests the Facebook Service to initiate scraping user data.
The Facebook Service works with the Facebook API to scrape data and updates the Database accordingly.
At the end, the Facebook Service returns the scraping progress to the Back-End.
Please include responses from the Database and Facebook API, indicating success or failure for each action. The diagram should visually represent the sequence of interactions and the flow of data among these components."
```

## Diagrams

[Facebook ad scrape](./facebook-api-workflow/facebook-ad-scrape.md)

[Long TTL access-token](./facebook-api-workflow/long-ttl-token.md)
