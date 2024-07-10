# Shell Scripting Project- Github API Integration

## GitHub API URL and Authentication:
   - The API_URL variable is set to the base URL for the GitHub API.
   - The USERNAME and TOKEN variables are placeholders for the GitHub username and personal access token. These credentials are used for authentication when making requests to the GitHub API.

## User and Repository Information:
   - The REPO_OWNER and REPO_NAME variables are expected to be passed as arguments to the script. They represent the owner (user or organization) and name of the repository, respectively.

## github_api_get Function
   - This function makes a GET request to the GitHub API.
   - It takes an endpoint (e.g., repos/${REPO_OWNER}/${REPO_NAME}/collaborators) and constructs the full URL.
   - The curl command sends the request with authentication using the provided credentials.
   - The response is processed using jq (a command-line JSON processor).

## list_users_with_read_access Function:
   - This function fetches the list of collaborators on the specified repository.
   - It filters collaborators who have read access (pull permissions) to the repository.
   - If there are no collaborators with read access, it prints a message indicating so; otherwise, it lists the usernames of collaborators.

## Main Script:
   - The script echoes a message indicating that it's listing users with read access.
   - It calls the list_users_with_read_access function.
