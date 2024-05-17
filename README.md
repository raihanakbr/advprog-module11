## Hello Minikube
1. Run before and after expose service
#### Before
![image](https://media.discordapp.net/attachments/1240984346689802280/1240984769106411601/image.png?ex=66488ca1&is=66473b21&hm=57d58af8e34c65beeed86cf572e3d37e80a363c23cb5e946359d685a6d943563&=&format=webp&quality=lossless&width=1168&height=103)

#### After
![image](https://media.discordapp.net/attachments/1240984346689802280/1240984365023105104/image.png?ex=66488c40&is=66473ac0&hm=339615372b08bfaaf220fe10d42ff8aa282a7e921dc95e08fa7e77400021a4fc&=&format=webp&quality=lossless&width=1158&height=217)

Before expose of the service, it doesnt show any logs whenever there are any open browser. After the exposal of the service, it began to accept request. Those requests can be seen in the logs as shown in the picture above.

2. The -n stands for namespace. So, by declaring -n, we instruct the terminal to search for the service with the namespace that we want.

## Rolling Update & Kubernetes
1. The distinction lies in the downtime incurred by the Recreate strategy. In essence, Recreate involves deleting the previous deployment before creating a new updated version, resulting in a longer updating time compared to the rolling update strategy.

2.  Yes, I successfully applied the Recreate deployment strategy by following the manual recreate deployment section of the tutorial at [dev.to](https://dev.to/cloudskills/kubernetes-deployment-strategy-recreate-3kgn). First, I ran `kubectl edit deployments spring-petclinic-rest` and then edited the version from the text file that appeared. Then, Kubernetes automatically applied the Recreate deployment strategy.
![image](https://media.discordapp.net/attachments/1240984346689802280/1241007146355916870/image.png?ex=6648a178&is=66474ff8&hm=2a117326b588fce03bb32bb43c4b81af0b2c1fa0e09f2e9f808474c2e97c4afa&=&format=webp&quality=lossless&width=1440&height=393)
![image](https://media.discordapp.net/attachments/1240984346689802280/1241007267156070400/image.png?ex=6648a195&is=66475015&hm=ed9fa741f23d0a0a551fcbd9cbef6a11d4375cd803b9f9982cd0a2f5ce6deeae&=&format=webp&quality=lossless&width=1440&height=635)

3. The file has been attached to `deployment-recreate.yaml`

4. In my opinion, kubernetes manifest files help me a lot especially when I want to create a deployment. With kubernetes manifest files, I don't have to remember the sequence of the code, the syntax, the flow, etc. I simply run 1 line `kubectl apply -f <yaml files>` which will make either deployment, services, or any other things according to the yaml files configuration. It gives efficiency to the maximum level considering we humans have a tendency to forget complex things that are difficult to remember.