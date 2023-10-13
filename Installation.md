- clone microsoft/soundscape
- follow backend directions in `docs/authoring-web-client/onboarding.md`


## Backend

1. In the `/backend` folder, if there is no virtual environment (`.venv`), create one and select it as the default Python interpreter in VSCode. Run `python3 -m venv .venv`.
2. If the Python packages are not installed, run `pip install -r requirements.txt`.
3. Go to `backend/.env` and rename `example.env` to just `.env`
4. Fill in the needed properties as shown in the `.env` file.
      - set `DJANGO_SETTINGS_MODULE = "backend.settings.local"` and run `export DJANGO_SETTINGS_MODULE="backend.settings.local"`
      - set `ENV = "local"` and run `export ENV="local"`
      - set `AZURE_MAPS_SUBSCRIPTION_KEY = ""` and run `export AZURE_MAPS_SUBSCRIPTION_KEY=""`
      - set `DJANGO_SECRET_KEY=""` and run `export DJANGO_SECRET_KEY=""`
5. Run: **NOTE**: Google and install any modules that `python manage.py makemigrations` tells you cannot be found
   1. python manage.py makemigrations
   2. python manage.py makemigrations api
   3. python manage.py migrate
7. In the folder `/backend/.env`:
   1. Create the files `local.env`, `development.env` and `production.env` (You can copy everything from the base .env into these)
8. Add the auth file as described in the [Authentication](#authentication) section.
9. Before running, make sure you are running the needed configuration - in the file `/backend/.vscode/lunch.json`, make sure the `envFile` property points to the environment file you are looking to run.
10. Run via VSCode (F5).
 
those directions are pretty good with some minor modifications:

subscription key
  - beyond this point, just google and install whatever modules that `python manage.py makemigrations` tells you cannot be found
  - also create three copies of `backend/.env/.env` in the same directory called `development.env`, `local.env`, and `production.env`
