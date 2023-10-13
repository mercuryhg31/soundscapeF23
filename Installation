- clone microsoft/soundscape
- follow backend directions in docs/authoring-web-client/onboarding.md

 
those directions are pretty good with some minor modifications:

- create the .venv directory as directed
  - you will probably run into issues with the first of the next three commands
      - go to backend/.env and rename example.env to just .env
      - set DJANGO_SETTINGS_MODULE = "backend.settings.local" and run export DJANGO_SETTINGS_MODULE="backend.settings.local"
      - set ENV = "local" and run export ENV="local"
      - you will need to set and export AZURE_MAPS_SUBSCRIPTION_KEY = "" as well at some point when it gives you an error claiming an invalid azure map subscription key
  - beyond this point, just google and install whatever modules that python manage.py makemigrations tells you cannot be found
  - also create three copies of backend/.env/.env in the same directory called development.env, local.env, and production.env
