[[Kubernetes]] native 

Uses [[OpenJDK HotSpot]] and [[GraalVM]]

## Purpose

Make java a 1st class platform for [[Kubernetes]] and serverless envs 
[[reactive programming]] and [[imperative programming]] model 

## What it does

Container first,  [[Kubernetes]] native
Optimise for low mem and fast startup (~10s of milliseconds)
Does processing at build time
'Live coding' - can write code and refresh the output within seconds rather than waiting for compile time. 



## How it does it

Classes only used at startup anre not loaded into runime JVM 


## Interesting

`http://localhost:8080/q/dev` - dev mode interactive UI to showcase added dependencies

Uses [[testcontainers]] to provide a 'DevServices' tool for interacting with 'prod like' externalities (like a db) that would usually be considered too heavy to run on machine. 

Uses 'continuous testing' through CLI and dev UI. Removes need for external CI tool. 
