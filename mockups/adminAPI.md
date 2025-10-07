# Recruit.me (Admin) API Mockup

## /reportCompanies

GET

```json
{}
```

200:

```json
{
    "companies": [
        {
            "company_id": "int",
            "name": "string",
            "profile": "string",
            "jobs": [
                {
                    "job_id": "int",
                    "job_name": "string",
                    "job_desc": "string",
                    "Active": "boolean",
                    "Required_Skills": ["string"],
                    "keywords": ["string"],
                    "applications": [
                        {
                            "parent": "int",
                            "applied_job": "int",
                            "rating": "string",
                            "status": "string"
                        }
                    ]
                }
            ]
        }
    ]
}
```

400:

```json
{ 
    "err": "No companies found" 
}
```

## /reportJobs

GET

```json
{ 
    "companyId": "string" 
}
```

200:

```json
{
    "jobs": [
        {
            "job_id": "int",
            "job_name": "string",
            "job_desc": "string",
            "Active": "boolean",
            "Required_Skills": ["string"],
            "keywords": ["string"],
            "applications": [
                {
                    "parent": "int",
                    "applied_job": "int",
                    "rating": "string",
                    "status": "string"
                }
            ]
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

## /reportApplicants

GET

```json
{}
```

200:

```json
{
    "applicants": [
        {
            "applicant_id": "int",
            "name": "string",
            "skills": ["string"],
            "applications": [
                {
                    "parent": "int",
                    "applied_job": "int",
                    "rating": "string",
                    "status": "string"
                }
            ]
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
