## build locally and test
s2i build . centos/python-36-centos7 azure-voting-app-redis-openshift

after I source my environment (stored in .env),

docker run -p 8080:8080 -e REDIS=${REDIS} -e REDIS_PWD=${REDIS_PWD}   azure-voting-app-redis-openshift
