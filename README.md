# firebase-emulator-docker
Wrapping the firebase emulator in a docker compose. The principal use case for this is allowing the creation of integration tests by people who are not working on firebase code in the organization. It also facilitates safely and quickly running accurate integration tests in your continuous integration pipeline. 

Drop these files directly into the root of your firebase implementation. 

Take care not to overwrite your own `firebase.json` file with this one if you have important differences. Just be sure to import the host 0.0.0.0 for each emulated service, as this is what allows you to interact with the services from outside of the localhost.

Then it's just a simple matter of:
~~~
docker-compose up
~~~
