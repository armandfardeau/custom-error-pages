# Instructions

## Activate errors interception:
in `/etc/nginx/conf.d/mod-http-passenger.conf`:
```passenger_intercept_errors on;```

## Redirect to page:
In `/etc/nginx/site-availables/my-site.conf`, block server:
```
include custom-error-pages/error_pages.conf;
```



