## Hello Minikube
1. Run before and after expose service
#### Before
![image](https://media.discordapp.net/attachments/1240984346689802280/1240984769106411601/image.png?ex=66488ca1&is=66473b21&hm=57d58af8e34c65beeed86cf572e3d37e80a363c23cb5e946359d685a6d943563&=&format=webp&quality=lossless&width=1168&height=103)

#### After
![image](https://media.discordapp.net/attachments/1240984346689802280/1240984365023105104/image.png?ex=66488c40&is=66473ac0&hm=339615372b08bfaaf220fe10d42ff8aa282a7e921dc95e08fa7e77400021a4fc&=&format=webp&quality=lossless&width=1158&height=217)

Before expose of the service, it doesnt show any logs whenever there are any open browser. After the exposal of the service, it began to accept request. Those requests can be seen in the logs as shown in the picture above.

2. The -n stands for namespace. So, by declaring -n, we instruct the terminal to search for the service with the namespace that we want.
