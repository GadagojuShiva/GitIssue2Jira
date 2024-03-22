# GitIssue2Jira
This Flask application integrates GitHub and JIRA to automatically create JIRA tickets based on comments made in GitHub issues. Specifically, it listens for comments on GitHub issues and triggers the creation of a JIRA ticket when the comment contains the "/jira" command.

## Prerequisites

Before running this application, make sure you have the following:

- Python installed on your system ([Download Python](https://www.python.org/downloads/))
- Flask library installed (`pip install Flask`)
- Requests library installed (`pip install requests`)
- A GitHub account with repository access
- A JIRA account with API access and the necessary permissions to create issues

## Installation

1. Clone this repository to your local machine:

    ```
    git clone https://github.com/GadagojuShiva/GitIssue2Jira.git
    ```


2. Install dependencies using pip:

    ```
    pip install -r requirements.txt
    ```

3. Configure GitHub and JIRA credentials and settings in the `create-jira-ticket.py` file.

## Configuration

In order to run this application, you need to configure your GitHub and JIRA credentials in the `create-jira-ticket.py` file:

- Replace `"YOUR_JIRA_API_TOKEN"` with your actual JIRA API token.
- Update the `auth` variable with your JIRA username and API token.
- Modify the JIRA ticket payload in the `createJIRA()` function according to your requirements.

## Usage

To run the Flask application, execute the following command in your terminal:

```
python create-jira-ticket.py
```

This will start the Flask server, and the application will be accessible at `http://localhost:5000/`.

Once the application is running, it will listen for incoming GitHub webhook events. When a new comment is added to a GitHub issue and it contains the "/jira" command, the application will create a corresponding JIRA ticket using the provided information.


## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or create a pull request.


