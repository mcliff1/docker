This docker image creates a build environment that has AWS cli with CDK


**mcliff/cdkbuild:0.1.1**

Added notes on a second implementation

To open this interactively without invoking sam
`docker run -it --entrypoint sh mcliff/sambuild:2.0.0`

## Releases

### version 0.1.1
 2021/03/13
    updated to CDK 1.42.0

### version 0.1.0
 2020/03/14
    started



## Releases (History from SAM)

### version 2.0.0
  2019/04/25
   updated Alpine 3.9
   add NPM 8.6

### version 1.1.1
  2019/04/24
   updated AMS SLI to 0.15.0 (from 0.2.2)

### version 1.1.0
  2019/01/10
  removed ENTRYPOINT
  added git

### version 1.0.1
  2018/11/10
  added jq

### version 1.0.0
  2018/11/08
  initial build with SAM; using Alpine 3.6


## References

* [sam local](https://github.com/cnadiminti/docker-aws-sam-local)
* [sam cli](https://hub.docker.com/r/pahud/aws-sam-cli)
* [frol docker github for docker](https://github.com/frol/docker-alpine-glibc)
