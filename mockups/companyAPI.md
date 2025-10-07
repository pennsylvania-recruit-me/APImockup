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
    "companyId": "int",
    "msg": "Company registered successfully"
}
```

400:

```json
{
    "err": "Registration failed",
}
```

## /companyProfile

GET:

```json
{
    "companyId": "int"
}
```

200:

```json
{
    "companyId": "int",
    "profile": {
        "name": "string",
        "profile": "string",
        "jobs": [
            {
                "jobId": "int",
                "jobName": "string",
                "jobDesc": "string",
                "requiredSkills": ["string"],
                "keywords": ["string"],
                "active": "boolean"
            }
        ]
    }
}
```

400:

```json
{
    "err": "Profile not found"
}
```

## /editCompanyProfile

POST:

```json
{
    "companyId": "int",
    "profileUpdates": {
        "name": "string",
        "profile": "string"
    }
}
```

200:

```json
{
    "msg": "Profile updated"
}
```

400:

```json
{
    "err": "Update failed"
}
```

## /createJob

POST:

```json
{
    "companyId": "int",
    "jobDetails": {
        "jobName": "string",
        "jobDesc": "string",
        "requiredSkills": ["string"],
        "keywords": ["string"],
        "active": "boolean"
    }
}
```

200:

```json
{
    "jobId": "int",
    "msg": "Job created"
}
```

400:

```json
{
    "err": "Job creation failed"
}
```

## /editJob

POST:

```json
{
    "jobId": "int",
    "jobUpdates": {
        "jobName": "string",
        "jobDesc": "string",
        "requiredSkills": ["string"],
        "keywords": ["string"],
        "active": "boolean"
    }
}
```

200:

```json
{
    "msg": "Job updated"
}
```

400:

```json
{
    "err": "Update failed"
}
```

## /activateJob

POST:

```json
{
    "jobId": "int"
}
```

200:

```json
{
    "msg": "Job activated"
}
```

400:

```json
{
    "err": "Activation failed"
}
```

## /closeJob

POST:

```json
{
    "jobId": "int"
}
```

200:

```json
{
    "msg": "Job closed"
}
```

400:

```json
{
    "err": "Close failed"
}
```

## /jobApplicants

GET:

```json
{
    "jobId": "int"
}
```

200:

```json
{
    "applicants": [
        {
            "applicantId": "int",
            "name": "string",
            "skills": ["string"],
            "rating": "string",
            "status": "string"
        }
    ]
}
```

400:

```json
{
    "err": "No applicants found"
}
```

## /viewApplicant

GET:

```json
{
    "applicantId": "int"
}
```

200:

```json
{
    "applicant": {
        "name": "string",
        "skills": ["string"],
        "applications": [
            {
                "jobId": "int",
                "status": "string",
                "rating": "string"
            }
        ]
    }
}
```

400:

```json
{
    "err": "Applicant not found"
}
```

## /rateApplicant

POST:

```json
{
    "jobId": "int",
    "applicantId": "int",
    "rating": "string"
}
```

200:

```json
{
    "msg": "Rating submitted"
}
```

400:

```json
{
    "err": "Rating failed"
}
```

## /offerJob

POST:

```json
{
    "jobId": "int",
    "applicantId": "int"
}
```

200:

```json
{
    "msg": "Offer sent"
}
```

400:

```json
{
    "err": "Offer failed"
}
```

## /rescindOffer

POST:

```json
{
    "jobId": "int",
    "applicantId": "int"
}
```

200:

```json
{
    "msg": "Offer rescinded"
}
```

400:

```json
{
    "err": "Rescind failed"
}
```
