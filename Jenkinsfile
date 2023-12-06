#!groovy

@Library('demo-share-lib') _

def tools = new org.devops.tools()

pipeline {
    agent { node {  label "master" }}

    stages {
        //下载代码
        stage("GetCode"){
            steps{
                timeout(time:2, unit:"MINUTES"){
                    script{
                        tools.printMsg("获取代码",'yellow')
                    }
                }
            }
        }
        //执行代码
        stage("RunCode"){
            steps{
                timeout(time:5, unit:"MINUTES"){
                    script{
                        tools.printMsg("执行代码",'blue')
                    }
                }
            }
        }
        //执行成功
        stage("Success"){
            steps{
                timeout(time:2, unit:"MINUTES"){
                    script{
                        tools.printMsg("执行成功",'green')
                    }
                }
            }
        }
        //执行失败
        stage("Failure"){
            steps{
                timeout(time:2, unit:"MINUTES"){
                    script{
                        tools.printMsg("执行失败",'red')
                    }
                }
            }
        }
    }
}
