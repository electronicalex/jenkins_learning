#!groovy

@Library('demo-share-lib') _

def tools = new org.devops.tools()

pipeline {
    agent { node {  label "master" }}

    stages {
        //下载代码
        stage("GetCode"){
            steps{
                timeout(time:1, unit:"MINUTES"){
                    script{
                        tools.PrintMes("获取代码",'yellow')
                    }
                }
            }
        }
        //执行代码
        stage("RunCode"){
            steps{
                timeout(time:5, unit:"MINUTES"){
                    script{
                        tools.PrintMes("执行代码",'blue')
                    }
                }
            }
        }
        //执行成功
        stage("GetCode"){
            steps{
                timeout(time:1, unit:"MINUTES"){
                    script{
                        tools.PrintMes("执行成功",'green')
                    }
                }
            }
        }
        //执行失败
        stage("GetCode"){
            steps{
                timeout(time:1, unit:"MINUTES"){
                    script{
                        tools.PrintMes("执行失败",'red')
                    }
                }
            }
        }
    }
}
