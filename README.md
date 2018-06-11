# Insight DevOps Engineering Systems Puzzle Solution

# Installing

    git clone https://github.com/bhprtk/systems-puzzle-solution

Assuming you have the Docker Engine and Docker Compose already installed, open a terminal and `cd` into this repo, and then enter these two commands:

    docker-compose up -d db
    docker-compose run --rm flaskapp /bin/bash -c "cd /opt/services/flaskapp/src && python -c  'import database; database.init_db()'"

This "bootstraps" the PostgreSQL database with the correct tables. After that you can run the whole system with:

    docker-compose up -d

At that point, the web application should be visible by going to [`localhost:8080`](http://localhost:8080/) in a web browser. 