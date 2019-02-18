# GraphQLDoc

GraphQLDoc is a simple Django app to document GraphQL schemas.

## Quick start
1. Add **graphqldoc** to your INSTALLED_APPS setting like this:
    
        INSTALLED_APPS = [
            ...
            'graphqldoc',
        ]

2. Add GRAPHQLDOC config settings in your settings file, and configure the host of your graphql server, like this:

        GRAPHQLDOC = {
            'GRAPHQL_HOST': 'http://localhost:8000/graphql/',
        }

3. Include the graphqldoc URLconf in your project `urls.py` like this:

        path('docs/', include('graphqldoc.urls')),

4. Run `python manage.py migrate` to create the graphqldoc models.

5. Start the development server and visit http://localhost:8000/docs/ to view the rendered documentation for your GraphQL server.