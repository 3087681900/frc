# FRC Instruction
## About FRC
+ FRC means FREE REDIS CLUSTER.
+ It is similar with Twemproxy.

## Compare with other system

<table>
<thead>
<tr>
<td></td><td>FRC</td><td>Codis</td><td>Twemproxy</td><td>Redis Cluster</td>
</tr>
</thead>
<tbody>
<tr>
<td>resharding without restarting cluster</td>
<td>Yes</td>
<td>Yes</td>
<td>No</td>
<td>Yes</td>
</tr>

<tr>
<td>hash tags for multi-key operations</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>

<tr>
<td>multi-key operations while resharding</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>

<tr>
<td>Redis clients supporting</td>
<td>Any</td>
<td>Any</td>
<td>Any</td>
<td>-</td>
</tr>

<tr>
<td>Redis clients supporting</td>
<td>No</td>
<td>Yes</td>
<td>-</td>
<td>No</td>
</tr>

<tr>
<td>Language</td>
<td>Java</td>
<td>Go</td>
<td>-</td>
<td>C</td>
</tr>

</tbody>
</table>

## Archtecture of FRC
moro info,can see the Docs.

## Usage
You can use use the FRCClient to invoke the api of FRC.<br/>
The way of invoking api as same sa jedis.<br/>
The client has implement the object-pool with common-pool.<br/>
e.g.<br/>
>       FrcClient client = new FrcClient(host, port, timeout);
>       boolean ret = client.set(logIndex, key, value);
>       if (ret) {
>          System.out.println("ok");
>       } else {
>         System.out.println("fail");
>       }






