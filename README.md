# A serverless guestbook web application and API built with Cloud Functions

The application is a simple guestbook website where users can post messages. It demonstrates how to build a serverless web application where static content is hosted in a storage bucket (here it uses GitHub Pages) and the backend is implemented with Cloud Functions. API Gateway is used to expose the Cloud Functions for the web user interface.

The user accesses the application hosted in GitHub Pages.
The web application calls a backend API.
The backend API is defined in API Gateway.
API Gateway forwards the request to Cloud Functions.
The Cloud Functions actions use IBM Cloudant to store and retrieve guestbook entries.

Refer to [this tutorial](https://console.bluemix.net/docs/solution-tutorials/serverless-api-webapp.html) for instructions.

## License

See [License.txt](License.txt) for license information.
