# AWX Container
You will want to remove the existing SECRET_KEY file and replace it with another string.  You can use your favorite method to generate randomness and uniqueness.  I'm not the boss of you.

Also, you'll want to go through credentials.py and change the passwords for Postgres and RabbitMQ.

Once you get all of that done, copy the files to /var/lib/awx.  Make sure selinux is not set to enforcing.  For this configuration, you'll also have to create a traefik-public network in Docker, even though I haven't implemented Traefik, as originally intended.

Eventually, I'll fix the selinux stuff so that it can run in enforcing, but that's project for another day.
