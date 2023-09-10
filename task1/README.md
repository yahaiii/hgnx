# Flask Endpoint for HNG Internship Task 1

This is a Flask-based endpoint that fulfills the requirements of the HNGx Internship task 1. It provides a publicly accessible API endpoint that accepts two GET request query parameters, `slack_name` and `track`, and returns specific information in JSON format.

## Requirements

The endpoint provides the following information in JSON format:

- Slack name
- Current day of the week
- Current UTC time (within +/-2 minutes)
- Track (based on the `track` parameter)
- GitHub URL of the file being run
- GitHub URL of the full source code
- Status code of 200 (Success)

## Usage

To use this endpoint, make a GET request to the following URL, providing the `slack_name` and `track` parameters:

`http://example.com/api?slack_name=example_name&track=backend`

Replace `example.com` with the actual URL where the Flask application is hosted.

### Example Response

```json
{
  "slack_name": "example_name",
  "current_day": "Monday",
  "utc_time": "2023-08-21T15:04:05Z",
  "track": "backend",
  "github_file_url": "https://github.com/username/repo/blob/main/file_name.ext",
  "github_repo_url": "https://github.com/username/repo",
  "status_code": 200
}
```

## Installation and Setup

To set up this Flask application locally, follow these steps:

1.  Clone the repository:

git clone `https://github.com/yahaiii/hngx.git`

2.  Navigate to the project directory:
`cd task1`

3.  Create a virtual environment (recommended):
`python -m venv venv`

4.  Activate the virtual environment:
On Windows:
`venv\Scripts\activate`

On macOS and Linux:
`source venv/bin/activate`

5.  Install the required dependencies:
`pip install -r requirements.txt`

6.  Run the Flask application:
`python app.py`

The Flask application should now be running locally, and you can access the endpoint at `http://localhost:5000/api`

## Deployment
To deploy this Flask application to a public server, you can follow your preferred deployment method, such as using a cloud platform or a web hosting service.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
Thanks to the HNG Internship team for providing this task.
