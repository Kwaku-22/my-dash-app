import more_itertools
from dash import dcc
from dash import html
from dash.dependencies import Input, Output
import pandas as pd
import plotly.graph_objs as go
import plotly.express as px

# Load the data using pandas
data = pd.read_csv('https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DV0101EN-SkillsNetwork/Data%20Files/historical_automobile_sales.csv')


# Initialize the Dash app
app = dash.Dash(__name__)

# Set the title of the dashboard
app.layout = html.Div([
    html.H1('Automobile Sales Statistics Dashboard',
            style={'textAlign': 'center', 'color': '#503D36', 'fontSize': 24})
])

# Run the app
if __name__ == '__main__':
    app.run_server(debug=True)

