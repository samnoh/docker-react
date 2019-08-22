# Docker + React

## `TIL`

### CI/CD

-   `.travis.yml`
    -   CI -> Deploy to AWS Elastic Beanstalk (CD)
    -   `$KEY` -> env variables

```yaml
deploy:
    provider: elasticbeanstalk
    region: 'ap-southeast-2'
    app: 'docker-react'
    env: 'DockerReact-env'
    bucket_name: 'elasticbeanstalk-ap-southeast-2-0531803850'
    bucket_path: 'docker-react'
    on:
        branch: master
    access_key_id:
        secure: $AWS_ACCESS_KEY
    secret_access_key:
        secure: '$AWS_SECRET_KEY'
```
