# Instructions

## Activate errors interception:
in `/etc/nginx/conf.d/mod-http-passenger.conf`:
```passenger_intercept_errors on;```

## Redirect to page:
In `/etc/nginx/site-availables/my-site.conf`, block server:
```
error_page 400 401 402 403 405 406 407 408 409 410 411 412 413 414 415 416 417 418 421 422 423 424 425 426 428 429 431 451 501 502 504 505 506 507 508 510 511 /error.html;
location = /error.html {
  ssi on;
  internal;
  auth_basic off;
  root /home/mako/osp-app/public/custom-error-pages/;
}

error_page 404 /error-404.html;
location = /error-404.html {
  ssi on;
  internal;
  auth_basic off;
  root /home/mako/osp-app/public/custom-error-pages/;
}

error_page 503 /error-503.html;
location = /error-503.html {
  ssi on;
  internal;
  auth_basic off;
  root /home/mako/osp-app/public/custom-error-pages/;
}

error_page 500 /error-500.html;
location = /error-500.html {
  ssi on;
  internal;
  auth_basic off;
  root /home/mako/osp-app/public/custom-error-pages/;
}
```



