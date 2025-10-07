# Company API Mockup

## /registerCompany

POST:
```json
{
    "companyName": "string",
    "email": "string",
    "password": "string"
}
```

200:
```json
{
    "companyId": "string",
    "message": "Company registered successfully"
}
```

400:
```json
{
    "error": "Registration failed",
    "details": "string"
}
```

## /companyProfile
GET:
```json
{
    "companyId": "string"
}
```

200: 
```json
{
    "companyId": "string",
    "profile": { }
}
```

400: 
```json
{
    "error": "Profile not found"
}
```

## /editCompanyProfile
POST: 
```json
{
    "companyId": "string",
    "profileUpdates": { }
}
```

200: 
```json
{
    "message": "Profile updated"
}
```

400: 
```json
{
    "error": "Update failed"
}
```

## /createJob
POST: 
```json
{
    "companyId": "string",
    "jobDetails": { }
}
```

200: 
```json
{
    "jobId": "string",
    "message": "Job created"
}
```

400: 
```json
{
    "error": "Job creation failed"
}
```

## /editJob
POST: 
```json
{
    "jobId": "string",
    "jobUpdates": { }
}
```

200: 
```json
{
    "message": "Job updated"
}
```

400: 
```json
{
    "error": "Update failed"
}
```

## /activateJob
POST: 
```json
{
    "jobId": "string"
}
```

200: 
```json
{
    "message": "Job activated"
}
```

400: 
```json
{
    "error": "Activation failed"
}
```

## /closeJob
POST: 
```json
{
    "jobId": "string"
}
```

200: 
```json
{
    "message": "Job closed"
}
```

400: 
```json
{
    "error": "Close failed"
}
```

## /jobApplicants
GET: 
```json
{
    "jobId": "string"
}
```

200: 
```json
{
    "applicants": [ ]
}
```

400: 
```json
{
    "error": "No applicants found"
}
```

## /viewApplicant
GET: 
```json
{
    "applicantId": "string"
}
```

200: 
```json
{
    "applicant": { }
}
```

400: 
```json
{
    "error": "Applicant not found"
}
```

## /rateApplicant
POST: 
```json
{
    "jobId": "string",
    "applicantId": "string",
    "rating": "number"
}
```

200: 
```json
{
    "message": "Rating submitted"
}
```

400: 
```json
{
    "error": "Rating failed"
}
```

## /offerJob
POST: 
```json
{
    "jobId": "string",
    "applicantId": "string"
}
```

200: 
```json
{
    "message": "Offer sent"
}
```

400: 
```json
{
    "error": "Offer failed"
}
```

## /rescindOffer
POST: 
```json
{
    "jobId": "string",
    "applicantId": "string"
}
```

200: 
```json
{
    "message": "Offer rescinded"
}
```

400: 
```json
{
    "error": "Rescind failed"
}
```

## /companyProfile
GET

    { "companyId": "string" }
200:
    { "companyId": "string", "profile": { ... } }
400:
    { "error": "Profile not found" }

## /editCompanyProfile

POST

    { "companyId": "string", "profileUpdates": { ... } }
200:
    { "message": "Profile updated" }
400:
    { "error": "Update failed" }

## /createJob
POST

    { "companyId": "string", "jobDetails": { ... } }
200:
    { "jobId": "string", "message": "Job created" }
400:
    { "error": "Job creation failed" }

## /editJob
POST

    { "jobId": "string", "jobUpdates": { ... } }
200:
    { "message": "Job updated" }
400:
    { "error": "Update failed" }

## /activateJob
POST

    { "jobId": "string" }
200:
    { "message": "Job activated" }
400:
    { "error": "Activation failed" }

## /closeJob
POST

    { "jobId": "string" }
200:
    { "message": "Job closed" }
400:
    { "error": "Close failed" }

## /jobApplicants
GET

    { "jobId": "string" }
200:
    { "applicants": [ { ... } ] }
400:
    { "error": "No applicants found" }

## /viewApplicant
GET

    { "applicantId": "string" }
200:
    { "applicant": { ... } }
400:
    { "error": "Applicant not found" }

## /rateApplicant
POST

        { "jobId": "string", "applicantId": "string", "rating": "number" }
200:
    { "message": "Rating submitted" }
400:
    { "error": "Rating failed" }

## /offerJob
POST

    { "jobId": "string", "applicantId": "string" }
200:
    { "message": "Offer sent" }
400:
    { "error": "Offer failed" }

## /rescindOffer
POST

    { "jobId": "string", "applicantId": "string" }
200:
    { "message": "Offer rescinded" }
400:
    { "error": "Rescind failed" }
