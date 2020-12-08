# Demo of Plone Containers

## Running Locally

Install Docker Desktop and run

    $ docker-compose up

Now go to http://foo.local.test/ and enjoy Plone!

BTW, to get the initial user password run this

    $ docker run --rm sixfeetup/dietplonedocker cat /opt/plone/inituser

## Running in AWS

Quick spin using [AWS Copilot](https://aws.github.io/copilot-cli/).

Set up your [credentials](https://aws.github.io/copilot-cli/docs/credentials/) and then run

    $ copilot init --app cloudplone          \
      --name cms                             \
      --type 'Load Balanced Web Service'     \
      --dockerfile './Dockerfile'            \
      --deploy

The output of that command will give you a URL to go and enjoy your Cloud Plone.

Don't forget to clean up your demo, AWS will keep charging you for running the Fargate container and the ALB.

    $ copilot app delete

