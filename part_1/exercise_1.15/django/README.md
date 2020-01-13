Use this image to run django development server on a docker container.

How to use this image
* Create requirements.txt file to the same folder where you want to build & run the image
* Add dependencies that you want to use to requirements.txt, for example:
    ```
    psycopg2==2.8.4
    django==3.0.2
    ```
* Run `docker run -p 80:8888 -t django`
* Open browser at http://localhost/
* You should see message about successful installation 