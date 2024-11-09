Jobs API Project
This Jobs API provides a simple and efficient way to manage job listings through RESTful API endpoints. It allows for creating, reading, updating, and deleting job entries, making it ideal for job boards, career portals, or internal job management systems.

Installation
Clone the repository:
git clone https://github.com/HongKai12345/Jobs-API-Project.git

Install dependencies:
npm install

Setup Environment Variables:
MONGO_URI=<your_mongodb_connection_string>

Start the Server
npm start
The API will now be running on http://localhost:3000


API Endpoints
POST: /api/v1/auth/register - register new user
Example:
{
  "name":"john",
  "email":"john@gmail.com",
  "password":"secret"
}

POST: /api/v1/auth/login - login user
Example:
{
  "email":"john@gmail.com",
  "password":"secret"
}

POST: /api/v1/jobs - create job
Example:
{
  "company":"random",
  "position":"random"
}

GET - /api/v1/jobs - returns a JSON objcet of all jobs tied to user and the number of jobs 

GET - /api/v1/jobs/:id - returns a JSON object of :id job

PATCH - /api/v1/jobs/:id - updates the :id job details 
Example:
{
    "company":"random",
    "position":"intern"
}

DELETE - /api/v1/jobs/:id - deletes the job listing associated to the id
