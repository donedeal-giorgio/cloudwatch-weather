# cloudwatch-weather

This application creates a cloudwatch dashboard for the monitoring
of the weather in Dublin.

## Dashboard

[Add screenshots here]

## Development
Create a python3 virtual env with:

```bash
git clone git@github.com:donedeal-giorgio/cloudwatch-weather.git cloudwatch-weather
cd cloudwatch-weather
python3 -m venv .venv
source .venv/bin/activate
pip install -r requiremnts.txt
pip install -e .
pytest -s
```

## Deployment

This application uses AWS Serverless Application Model (SAM)[https://aws.amazon.com/serverless/sam/]
to deploy a stack containing the following resources:
1. Lambda function getting metEirann weather data for today
2. An AWS CloudWatch event that triggers the lambda on a 30 mins schedule.
3. The definition of the cloudwatch dashboard [todo]

To deploy this application in your own stack, first follow the development steps.
The issue the following commands:

```bash
cd aws-weather
sam build --guided
sam deploy
```


