**Deepquads is libre software web-based continuous localization system,
used by over 2500 libre projects and companies in more than 165 countries.**

The docker-compose for Docker container for Deepquads

.. image:: https://readthedocs.org/projects/deepquads/badge/
    :alt: Documentation
    :target: https://docs.deepquads.github.io/en/latest/admin/install/docker.html

Documentation
-------------

Detailed documentation is available in Deepquads documentation:

https://docs.deepquads.github.io/en/latest/admin/install/docker.html

Getting started
---------------

1. Clone the docker-compose repository:

   .. code-block:: shell

      git clone https://github.com/deepSquads/docker-compose.git
      cd docker-compose

2. Create a ``docker-compose.override.yml`` file with your settings.

   .. code-block:: yml

        services:
          deepquads:
            ports:
              - 80:8080
            environment:
              DEEPSQUADS_SITE_DOMAIN: example.com
              DEEPSQUADS_EMAIL_HOST: smtp.example.com
              DEEPSQUADS_EMAIL_HOST_USER: user
              DEEPSQUADS_EMAIL_HOST_PASSWORD: pass
              DEEPSQUADS_ALLOWED_HOSTS: your hosts
              DEEPSQUADS_ADMIN_PASSWORD: password for admin user

3. Start it up:

   .. code-block:: shell

        docker compose up

5. For more detailed instructions and configuration visit https://docs.deepquads.github.io/en/latest/admin/install/docker.html

Rebuilding the deepquads docker image
-----------------------------------

The `docker-compose` files can be found in https://github.com/deepSquads/docker-compose.
The deepquads docker image is built from https://github.com/deepSquads/docker.
