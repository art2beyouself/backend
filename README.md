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
## Automated bot:
Object of this bot demonstrate functionalities of the system according to defined rules. This
bot should read rules from a config file (in any format chosen by the candidate), but should
have following fields (all integers, candidate can rename as they see fit):
● number_of_users
● max_posts_per_user
● max_likes_per_user