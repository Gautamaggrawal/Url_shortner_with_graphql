# Url_shortner_with_graphql


```
query {
  urls {
    id
    fullUrl
    urlHash
    clicks
    createdAt
  }
}

```

```
mutation {
  createUrl(fullUrl:"https://www.gautam.aggrawal.netlify.com/index") {
    url {
      id
      fullUrl
      urlHash
      clicks
      createdAt
    }
  }
}
```


```
mutation {
  createUrl(fullUrl:"not_valid_url"){
    url {
      id
      fullUrl
      urlHash
      clicks
      createdAt
    }
  }
}
```


```
query {
  urls(url:"index") {
    id
    fullUrl
    urlHash
    clicks
    createdAt
  }
}
```


```
query {
  urls(first: 2, skip: 1) {
    id
    fullUrl
    urlHash
    clicks
    createdAt
  }
}
```