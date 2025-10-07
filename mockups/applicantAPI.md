# Applicant API Mockup

## /registerApplicant

POST:

```json
{
    "name": "string",
    "email": "string",
    "password": "string"
}
```

200:

```json
{
    "applicantId": "int",
    "msg": "Account registered"
}
```

400:

```json
{
    "err": "Registration failed"
}
```

## /applicantProfile

GET:

```json
{
    "applicantId": "int"
}
```

200:

```json
{
    "profile": {
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
    "err": "Profile not found"
}
```

## /editApplicantProfile

POST:

```json
{
    "applicantId": "int",
    "profileUpdates": {
        "name": "string",
        "skills": ["string"]
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

## /searchJobs

GET:

```json
{
    "searchParams": {
        "keywords": ["string"],
        "requiredSkills": ["string"],
        "active": "boolean"
    }
}
```

200:

```json
{
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
```

400:

```json
{
    "err": "No jobs found"
}
```

## /applyJob

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
    "msg": "Applied successfully"
}
```

400:

```json
{
    "err": "Application failed"
}
```

## /withdrawApplication

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
    "msg": "Withdrawn"
}
```

400:

```json
{
    "err": "Withdraw failed"
}
```

## /acceptOffer

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
    "msg": "Offer accepted"
}
```

400:

```json
{
    "err": "Accept failed"
}
```

## /rejectOffer

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
    "msg": "Offer rejected"
}
```

400:

```json
{
    "err": "Reject failed"
}
```
