### DEPLOYMENT OF KUBERNETES
## from jenkins server to handle kubernetes deployment

In the jenkins server we have to create global credentials.

go to credentials then after create global credentilas.

in that we have to give ---> ssh authentication
## user root
## id 
my-ssh-key

## use pricate key 
add private key of .ssd/id_rsa

add that key in add passprase

save and run the job.
