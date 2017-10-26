# dockers
Dockerfile for common use

## GoEnv for create a linux ubuntu environment image, you can use this environment to compile linex exec file. for exemple:
    1 create image :
        docker build -t go:env .
    2 create container :
        docker run -it -v hostdir:containerdir --name xxxx go:env
        
