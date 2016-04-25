# NewsAI API Standards

This repository outlines the API standards that we follow at NewsAI. This was heavily inspired by the standards set by [18F](https://github.com/18f/api-standards). We are inspired from a lot of different specifications that already exist in building our API -- such as [JSON API](http://jsonapi.org/), [Django REST Framework](http://www.django-rest-framework.org/), and many others.

A lot of the categories below were taken from the document proposed by 18F. Major props to them!

### API Endpoints

### Just use JSON

### API Keys

### Error handling

We follow the error handling that was proposed in the [JSON API](http://jsonapi.org/format/#errors) spec. From this spec our error objects have the following members: `status`, `detail`, `title`, and `source`.

```json
{
    "status": "401",
    "detail": "Please login.",
    "title": "Authentication Required.",
    "source": {
        "pointer": "/api"
    }
}
```

### Pagination

### API Versioning and Semantic Versioning

### Always use HTTPS

### Use UTF-8

### CORS
