## How to run:
  * install docker & docker-compose
  * `cd <repo root>`
  * `docker-compose up backend` (or run in detached mode if you don't want to see some logging);
  * wait a bit and run at another tab `docker-compose up bot`;
  * or run docker-compose up

  * JWT authentication;
  * email verification through `hunter.io` on signup;
  * profile enrichment based on `clearbit.com/enrichment`;
  * API:
    * user creation and login;
    * post creation & retrieve;
    * post listing;
    * post like;
    * post unlike;