# NewsAI API Standards

This repository outlines the API standards that we follow at NewsAI. This was heavily inspired by the standards set by [18F](https://github.com/18f/api-standards). We are inspired from a lot of different specifications that already exist in building our API -- such as [JSON API](http://jsonapi.org/), [Django REST Framework](http://www.django-rest-framework.org/), and many others.

A lot of the categories below were taken from the document proposed by 18F and the JSON API spec. Major props to both of them!

### Top level

At the top level of our API we currently have four major fields: `count`, `next`, `previous`, and `results`.

```json
{
    "count": 1,
    "next": "https://api.newsai.org/api/feeds/?limit=20&offset=20",
    "previous": null,
    "results": []
}
```

### API Endpoints

### Just use JSON

### API Keys

### Error handling

We follow the error handling that was proposed in the [JSON API](http://jsonapi.org/format/#errors) spec. From this spec our `error` objects have the following members: `status`, `detail`, `title`, and `source`. The top level of the JSON document is the keyword `errors`, and it contains an array of objects with those members.

```json
{
    "errors": [{
        "status": "401",
        "detail": "Please login.",
        "title": "Authentication Required.",
        "source": {
            "pointer": "/api"
        }
    }]
}
```

### Pagination

### API Versioning and Semantic Versioning

### Always use HTTPS

### Use UTF-8

### CORS
