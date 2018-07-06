Aws autoscaling: why we need autoscaling if server performance will increse that we need create other server manually but in aws is provided autoscaling once we configure that it will automatically create onther server. For this we need take server backup first using that AMI we configure the autoscaling if server performance reach to 85% means it will create the server, when server performance decrease means it will stop the server based our conditions.

![auto](https://github.com/malli2221/ops/blob/master/images1/auto1%202018-07-06%2019-07-51.png)

![auto](https://github.com/malli2221/ops/blob/master/images1/autoscaling%202018-07-06%2021-35-53.png)

![auto1](https://github.com/malli2221/ops/blob/master/images1/auto32018-07-06%2019-22-40.png)

![auto](https://github.com/malli2221/ops/blob/master/images1/auto5%202018-07-06%2019-26-59.png)

![creating](https://github.com/malli2221/ops/blob/master/images1/scaling%202018-07-06%2021-51-49.png)

Aws s3 bucket : s3 means simple storage aws provide storage.

- this storage high scalable and size not planned(aws provided unlimted storage)

- s3 do the WORM opration ( write once read manytimes)

- s3 is safe place to storage our files.

- it is object based storage.

Bucket: 1.root level &quot;folders&quot; you creation in s3 are refered as &quot;bucket&quot;

2. any floder you creaate in bucket is reffered to as folder.

![s3.1](https://github.com/malli2221/ops/blob/master/images1/s3%202018-07-06%2015-51-04.png)

![s3.2](https://github.com/malli2221/ops/blob/master/images1/s3-1%202018-07-06%2015-53-32.png)

![s3.3](https://github.com/malli2221/ops/blob/master/images1/s3%20-cli%20%202018-07-06%2015-57-27.png)

Nat gateway: this nat get way we are using private vpc communications purpose we using this nat gateway.

Go to nat gateway-&gt; create the nat gateway.

Once we are crating the nat gateway associate to routing table then only communicate to privaten vpc server.

![nat](https://github.com/malli2221/ops/blob/master/images1/natgateway%202018-07-06%2018-57-24.png)

vpcpeering :  why we are using this vpe peering means we have created two vpc in our aws then in that vpc we are creating two server in two vpc, so it wont communicate each other so for that we are

creating vpc peering than after that this vpc perring add to paticular server routing tables then it will communicate to eath other.



![peering](https://github.com/malli2221/ops/blob/master/images1/peering%202018-07-06%2018-41-31.png)

![peering](https://github.com/malli2221/ops/blob/master/images1/peering2018-07-06%2018-42-27.png)
