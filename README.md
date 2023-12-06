## AirBnB Clone - Deploy Static

This project deploys a static AirBnB clone website using Fabric and Nginx.

**Prerequisites:**

* Python 3.x
* Fabric
* Virtualenv (optional)
* Nginx
* Git

**Resources:**

* How to use Fabric: [https://docs.fabfile.org/](https://docs.fabfile.org/)
* How to use Fabric in Python: [https://docs.fabfile.org/en/1.11/tutorial.html](https://docs.fabfile.org/en/1.11/tutorial.html)
* Fabric and command line options: [https://docs.readthedocs.io/en/latest/](https://docs.readthedocs.io/en/latest/)
* CI/CD concept page: [https://en.wikipedia.org/wiki/CI/CD](https://en.wikipedia.org/wiki/CI/CD)
* Nginx configuration for beginners: [https://www.nginx.com/resources/wiki/start/topics/examples/server_blocks/](https://www.nginx.com/resources/wiki/start/topics/examples/server_blocks/)
* Difference between root and alias on NGINX: [https://fedingo.com/nginx-alias-vs-root/](https://fedingo.com/nginx-alias-vs-root/)
* Fabric for Python 3: [https://docs.readthedocs.io/en/latest/](https://docs.readthedocs.io/en/latest/)

**Instructions:**

1. Clone the repository.
2. Create a virtualenv (optional):
```
python3 -m venv venv
source venv/bin/activate
```
3. Install Fabric:
```
pip install fabric
```
4. Edit the `fabfile.py` to configure the deployment settings:
    * `HOST`: The host where the website will be deployed.
    * `USER`: The username for the remote server.
    * `KEY_FILE`: The path to the SSH key file for authentication.
    * `SITE_DIR`: The directory on the remote server where the website will be deployed.
5. Run the following command to deploy the website:
```
fab deploy
```

**Nginx configuration:**

1. Create a server block configuration file for the website.
2. Specify the `root` directive to point to the deployed website directory.
3. Configure the server block to listen on the desired port.
4. Reload Nginx:
```
sudo nginx -s reload
```

**CI/CD:**

This project can be integrated with a CI/CD pipeline for automated deployment. You can use tools like Jenkins, Travis CI, or CircleCI to automatically build and deploy the website after code changes.

**Contributing:**

Feel free to fork and contribute to this project. Pull requests are welcome!
