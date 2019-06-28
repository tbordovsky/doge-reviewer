This is an example GitHub App that sends thank you messages for pull request reviews submitted in a repository. You can follow the "[Using the GitHub API in your app](https://developer.github.com/apps/quickstart-guides/using-the-github-api-in-your-app/)" quickstart guide on developer.github.com.

This project listens for webhook events sends a slack message to thank helpful reviewers:
* `app.py` (Single module flask app)

To learn how to set up a template GitHub App, follow the "[Setting up your development environment](https://developer.github.com/apps/quickstart-guides/setting-up-your-development-environment/)" quickstart guide on developer.github.com.
It probably won't help you look at this code, but you can still use it to figure out how to set everything up locally.

## Install

Make sure to set up a virtualenv with python3.6 or greater, it's necessary for the latest slack API.

To install dependencies, run `pip install requirements.txt` inside of your virtualenv.

To run the app, first add these vars to your virtualenv hooks like so `echo 'export FLASK_APP=app.py\nexport FLASK_ENV=development' >> $VIRTUAL_ENV/bin/postactivate` and `echo 'unset FLASK_APP\nunset FLASK_ENV' >> VIRTUAL_ENV/bin/predeactivate'`

## Set environment variables

1. Create a copy of the `.env-example` file called `.env`.
2. Add your GitHub App's webhook secret to the `.env` file.
3. Add your Slack API key to the `.env` file.

## Run the server

1. Run `flask run` or `python -m flask run` on the command line.
1. View the default Flask app at `localhost:5000`.
