# A serverless guestbook web application and API built with Cloud Functions

The application is a simple guestbook website where users can post messages. It demonstrates how to build a serverless web application where static content is hosted in a storage bucket (here it uses GitHub Pages) and the backend is implemented with Cloud Functions. API Gateway is used to expose the Cloud Functions for the web user interface.

<img src='./Architecture.png' />

## Workflow

1. The user accesses the application hosted in GitHub Pages.
2. The web application calls a backend API.
3. The backend API is defined in API Gateway.
4. API Gateway forwards the request to Cloud Functions.
5. The Cloud Functions actions use IBM Cloudant to store and retrieve guestbook entries.

## API

- Create an API
- Go to Actions.
- Select the read-guestbook-entries-sequence sequence. Next to the name, click on Web Action, check Enable as Web Action and Save.
- Do the same for the save-guestbook-entry-sequence sequence.
- Go to APIs and click Create API (or Create Managed API if you have existing APIs).
- Set the API name to guestbook and, accordingly, the base path to /guestbook.
- Click on Create operation and create an operation to retrieve guestbook entries:
- Set path to /entries
- Set verb to GET
- Select the read-guestbook-entries-sequence action
- Click on Create operation and create an operation to persist a guestbook entry:
- Set path to /entries
- Set verb to PUT
- Select the save-guestbook-entry-sequence action
- Scroll to the end of the page to Create the API. Make note of the provided route, as you will use it from your web application.

Refer to [this tutorial](https://console.bluemix.net/docs/solution-tutorials/serverless-api-webapp.html) for instructions.

## License

See [License.txt](License.txt) for license information.
