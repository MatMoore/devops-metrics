# Dev-Ops metrics

An experimental Jupyter notebook to analyse our development process based on Github pull requests and releases to [laa-ccms-pui](https://github.com/ministryofjustice/laa-ccms-pui/).

## What we want to measure

We want short lead times, high deployment frequency, low MTTR and low change fail percentage.

These metrics were popularised by the "Accelerate" book and are measured industry wide in the [State of DevOps Report](https://cloud.google.com/devops).

Not all of these can be measured from Github data. Lead time should cover the time it takes from requesting something to delivering it, and mean time to recovery isn't visible from this data at all. However, the github data can show us how quickly work progresses through the code review process.

We could potentially supplement this with data from Jira and Service Now.

## Running the notebook
### Dependencies
Install dependencies using pipenv:

```
pip install pipenv && pipenv install
```

### Configuration
Create a [personal access token](https://github.com/settings/tokens) in github. Choose repo scope. You also need to click "Enable SSO". Then run:

```
echo "GITHUB_ACCESS_TOKEN=YOUR_TOKEN_HERE" > .env
```

### Jupyter notebook
Run `pipenv shell` and then run:

```
ipython kernel install --user --name=devops-metrics
jupyter notebook
```

In the notebook, change the kernel to `devops-metrics`.

## Licence
MIT Licence.
