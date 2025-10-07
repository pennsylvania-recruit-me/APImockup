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
    "applicantId": "string",
    "message": "Account registered"
}
```

400:
```json
{
    "error": "Registration failed"
}
```

## /applicantProfile
GET:
```json
{
    "applicantId": "string"
}
```

200:
```json
{
    "profile": { }
}
```

400:
```json
{
    "error": "Profile not found"
}
```

## /editApplicantProfile
POST:
```json
{
    "applicantId": "string",
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

## /searchJobs
GET:
```json
{
    "searchParams": { }
}
```

200:
```json
{
    "jobs": [ { } ]
}
```

400:
```json
{
    "error": "No jobs found"
}
```

## /applyJob
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
    "message": "Applied successfully"
}
```

400:
```json
{
    "error": "Application failed"
}
```

## /withdrawApplication
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
    "message": "Withdrawn"
}
```

400:
```json
{
    "error": "Withdraw failed"
}
```

## /acceptOffer
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
    "message": "Offer accepted"
}
```

400:
```json
{
    "error": "Accept failed"
}
```

## /rejectOffer
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
    "message": "Offer rejected"
}
```

400:
```json
{
    "error": "Reject failed"
}
```
