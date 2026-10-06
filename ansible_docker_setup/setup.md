# Create the docker image
docker build -t ansible:latest .

# Run the ansible container
docker run -it -v ${pwd}/ansible:/ansible -w /ansible -e AWS_ACCESS_KEY_ID=<"ACCESS_KEY"> -e AWS_SECRET_ACCESS_KEY=<"ANSIBLE_SECRET_ACCESS_KEY"> ansible
