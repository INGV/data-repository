
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/INGV/data-repository/blob/main/LICENSE)

# INGV Open Data Repository

The aim of this project is to design and implement a **data repository** in order to equip the Institute with a tool that, together with the [Open Data Portal](https://data.ingv.it), is able to provide INGV researchers and technologists with a complete tool for the _publication_ and _traceability_ of research data, in line with the principles of the [FAIRness](https://www.go-fair.org/fair-principles/) of scientific research and [institutional data policy](https://data.ingv.it/docs/principles/).

## Getting started

Run the following commands in order to start your new **INGV Open Data repository**
instance:

```console
invenio-cli containers start --lock --build --setup
```

The above command first builds the application docker image and afterwards
starts the application and related services (database, Opensearch, Redis
and RabbitMQ). The build and boot process will take some time to complete,
especially the first time as docker images have to be downloaded during the
process.

Once running, visit https://127.0.0.1 in your browser.

**Note**: The server is using a self-signed SSL certificate, so your browser
will issue a warning that you will have to by-pass.

## Overview

Following is an overview of the generated files and folders:

| Name | Description |
|---|---|
| ``Dockerfile`` | Dockerfile used to build your application image. |
| ``Pipfile`` | Python requirements installed via [pipenv](https://pipenv.pypa.io) |
| ``Pipfile.lock`` | Locked requirements (generated on first install). |
| ``app_data`` | Application data such as vocabularies. |
| ``assets`` | Web assets (CSS, JavaScript, LESS, JSX templates) used in the Webpack build. |
| ``docker`` | Example configuration for NGINX and uWSGI. |
| ``docker-compose.full.yml`` | Example of a full infrastructure stack. |
| ``docker-compose.yml`` | Backend services needed for local development. |
| ``docker-services.yml`` | Common services for the Docker Compose files. |
| ``invenio.cfg`` | The Invenio application configuration. |
| ``logs`` | Log files. |
| ``static`` | Static files that need to be served as-is (e.g. images). |
| ``templates`` | Folder for your Jinja templates. |
| ``.invenio`` | Common file used by Invenio-CLI to be version controlled. |
| ``.invenio.private`` | Private file used by Invenio-CLI *not* to be version controlled. |

## Documentation

To learn how to configure, customize, deploy and much more, visit
the [InvenioRDM Documentation](https://inveniordm.docs.cern.ch/).
