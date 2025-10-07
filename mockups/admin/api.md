# Recruit.me (Admin) API Mockup

## /reportCompanies

GET

```json
{}
```

200:

```json
{ "companies": [ { ... } ] }
```

400:

```json
{ "error": "No companies found" }
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
    "jobs": [ { ... } ] 
}
```

400:

```json
{ 
    "error": "No jobs found" 
}
```

## /reportApplicants
GET

```json
{

}
```

200:

```json
{ 
    "applicants": [ { ... } ] 
}
```

400:

```json
{
     "error": "No applicants found" 
}
```
