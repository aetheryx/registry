
---
title: "getMountTarget"
title_tag: "aws.efs.getMountTarget"
meta_desc: "Documentation for the aws.efs.getMountTarget function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Provides information about an Elastic File System Mount Target (EFS).


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var config = new Config();
        var mountTargetId = config.Get("mountTargetId") ?? "";
        var byId = Output.Create(Aws.Efs.GetMountTarget.InvokeAsync(new Aws.Efs.GetMountTargetArgs
        {
            MountTargetId = mountTargetId,
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v4/go/aws/efs"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi/config"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		cfg := config.New(ctx, "")
		mountTargetId := ""
		if param := cfg.Get("mountTargetId"); param != "" {
			mountTargetId = param
		}
		opt0 := mountTargetId
		_, err := efs.LookupMountTarget(ctx, &efs.LookupMountTargetArgs{
			MountTargetId: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_aws as aws

config = pulumi.Config()
mount_target_id = config.get("mountTargetId")
if mount_target_id is None:
    mount_target_id = ""
by_id = aws.efs.get_mount_target(mount_target_id=mount_target_id)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const config = new pulumi.Config();
const mountTargetId = config.get("mountTargetId") || "";
const byId = aws.efs.getMountTarget({
    mountTargetId: mountTargetId,
});
```


{{< /example >}}





{{% /examples %}}




## Using getMountTarget {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getMountTarget<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetMountTargetArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetMountTargetResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_mount_target(</span><span class="nx">access_point_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                     <span class="nx">file_system_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                     <span class="nx">mount_target_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                     <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetMountTargetResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupMountTarget<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupMountTargetArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupMountTargetResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupMountTarget` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetMountTarget </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetMountTargetResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetMountTargetArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="accesspointid_csharp">
<a href="#accesspointid_csharp" style="color: inherit; text-decoration: inherit;">Access<wbr>Point<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the access point whose mount target that you want to find. It must be included if a `file_system_id` and `mount_target_id` are not included.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filesystemid_csharp">
<a href="#filesystemid_csharp" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the file system whose mount target that you want to find. It must be included if an `access_point_id` and `mount_target_id` are not included.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mounttargetid_csharp">
<a href="#mounttargetid_csharp" style="color: inherit; text-decoration: inherit;">Mount<wbr>Target<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the mount target that you want to find. It must be included in your request if an `access_point_id` and `file_system_id` are not included.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="accesspointid_go">
<a href="#accesspointid_go" style="color: inherit; text-decoration: inherit;">Access<wbr>Point<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the access point whose mount target that you want to find. It must be included if a `file_system_id` and `mount_target_id` are not included.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filesystemid_go">
<a href="#filesystemid_go" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the file system whose mount target that you want to find. It must be included if an `access_point_id` and `mount_target_id` are not included.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mounttargetid_go">
<a href="#mounttargetid_go" style="color: inherit; text-decoration: inherit;">Mount<wbr>Target<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the mount target that you want to find. It must be included in your request if an `access_point_id` and `file_system_id` are not included.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="accesspointid_nodejs">
<a href="#accesspointid_nodejs" style="color: inherit; text-decoration: inherit;">access<wbr>Point<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the access point whose mount target that you want to find. It must be included if a `file_system_id` and `mount_target_id` are not included.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filesystemid_nodejs">
<a href="#filesystemid_nodejs" style="color: inherit; text-decoration: inherit;">file<wbr>System<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the file system whose mount target that you want to find. It must be included if an `access_point_id` and `mount_target_id` are not included.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mounttargetid_nodejs">
<a href="#mounttargetid_nodejs" style="color: inherit; text-decoration: inherit;">mount<wbr>Target<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the mount target that you want to find. It must be included in your request if an `access_point_id` and `file_system_id` are not included.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="access_point_id_python">
<a href="#access_point_id_python" style="color: inherit; text-decoration: inherit;">access_<wbr>point_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the access point whose mount target that you want to find. It must be included if a `file_system_id` and `mount_target_id` are not included.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="file_system_id_python">
<a href="#file_system_id_python" style="color: inherit; text-decoration: inherit;">file_<wbr>system_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the file system whose mount target that you want to find. It must be included if an `access_point_id` and `mount_target_id` are not included.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mount_target_id_python">
<a href="#mount_target_id_python" style="color: inherit; text-decoration: inherit;">mount_<wbr>target_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID or ARN of the mount target that you want to find. It must be included in your request if an `access_point_id` and `file_system_id` are not included.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getMountTarget Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="availabilityzoneid_csharp">
<a href="#availabilityzoneid_csharp" style="color: inherit; text-decoration: inherit;">Availability<wbr>Zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique and consistent identifier of the Availability Zone (AZ) that the mount target resides in.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzonename_csharp">
<a href="#availabilityzonename_csharp" style="color: inherit; text-decoration: inherit;">Availability<wbr>Zone<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Availability Zone (AZ) that the mount target resides in.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsname_csharp">
<a href="#dnsname_csharp" style="color: inherit; text-decoration: inherit;">Dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DNS name for the EFS file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filesystemarn_csharp">
<a href="#filesystemarn_csharp" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Resource Name of the file system for which the mount target is intended.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filesystemid_csharp">
<a href="#filesystemid_csharp" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ipaddress_csharp">
<a href="#ipaddress_csharp" style="color: inherit; text-decoration: inherit;">Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Address at which the file system may be mounted via the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="mounttargetdnsname_csharp">
<a href="#mounttargetdnsname_csharp" style="color: inherit; text-decoration: inherit;">Mount<wbr>Target<wbr>Dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DNS name for the given subnet/AZ per [documented convention](http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html).
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="mounttargetid_csharp">
<a href="#mounttargetid_csharp" style="color: inherit; text-decoration: inherit;">Mount<wbr>Target<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="networkinterfaceid_csharp">
<a href="#networkinterfaceid_csharp" style="color: inherit; text-decoration: inherit;">Network<wbr>Interface<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the network interface that Amazon EFS created when it created the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ownerid_csharp">
<a href="#ownerid_csharp" style="color: inherit; text-decoration: inherit;">Owner<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}AWS account ID that owns the resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="securitygroups_csharp">
<a href="#securitygroups_csharp" style="color: inherit; text-decoration: inherit;">Security<wbr>Groups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}List of VPC security group IDs attached to the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subnetid_csharp">
<a href="#subnetid_csharp" style="color: inherit; text-decoration: inherit;">Subnet<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the mount target's subnet.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="accesspointid_csharp">
<a href="#accesspointid_csharp" style="color: inherit; text-decoration: inherit;">Access<wbr>Point<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="availabilityzoneid_go">
<a href="#availabilityzoneid_go" style="color: inherit; text-decoration: inherit;">Availability<wbr>Zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique and consistent identifier of the Availability Zone (AZ) that the mount target resides in.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzonename_go">
<a href="#availabilityzonename_go" style="color: inherit; text-decoration: inherit;">Availability<wbr>Zone<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Availability Zone (AZ) that the mount target resides in.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsname_go">
<a href="#dnsname_go" style="color: inherit; text-decoration: inherit;">Dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DNS name for the EFS file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filesystemarn_go">
<a href="#filesystemarn_go" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Resource Name of the file system for which the mount target is intended.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filesystemid_go">
<a href="#filesystemid_go" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ipaddress_go">
<a href="#ipaddress_go" style="color: inherit; text-decoration: inherit;">Ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Address at which the file system may be mounted via the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="mounttargetdnsname_go">
<a href="#mounttargetdnsname_go" style="color: inherit; text-decoration: inherit;">Mount<wbr>Target<wbr>Dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DNS name for the given subnet/AZ per [documented convention](http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html).
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="mounttargetid_go">
<a href="#mounttargetid_go" style="color: inherit; text-decoration: inherit;">Mount<wbr>Target<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="networkinterfaceid_go">
<a href="#networkinterfaceid_go" style="color: inherit; text-decoration: inherit;">Network<wbr>Interface<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the network interface that Amazon EFS created when it created the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ownerid_go">
<a href="#ownerid_go" style="color: inherit; text-decoration: inherit;">Owner<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}AWS account ID that owns the resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="securitygroups_go">
<a href="#securitygroups_go" style="color: inherit; text-decoration: inherit;">Security<wbr>Groups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}List of VPC security group IDs attached to the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subnetid_go">
<a href="#subnetid_go" style="color: inherit; text-decoration: inherit;">Subnet<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the mount target's subnet.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="accesspointid_go">
<a href="#accesspointid_go" style="color: inherit; text-decoration: inherit;">Access<wbr>Point<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="availabilityzoneid_nodejs">
<a href="#availabilityzoneid_nodejs" style="color: inherit; text-decoration: inherit;">availability<wbr>Zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique and consistent identifier of the Availability Zone (AZ) that the mount target resides in.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzonename_nodejs">
<a href="#availabilityzonename_nodejs" style="color: inherit; text-decoration: inherit;">availability<wbr>Zone<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Availability Zone (AZ) that the mount target resides in.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsname_nodejs">
<a href="#dnsname_nodejs" style="color: inherit; text-decoration: inherit;">dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DNS name for the EFS file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filesystemarn_nodejs">
<a href="#filesystemarn_nodejs" style="color: inherit; text-decoration: inherit;">file<wbr>System<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Resource Name of the file system for which the mount target is intended.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filesystemid_nodejs">
<a href="#filesystemid_nodejs" style="color: inherit; text-decoration: inherit;">file<wbr>System<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ipaddress_nodejs">
<a href="#ipaddress_nodejs" style="color: inherit; text-decoration: inherit;">ip<wbr>Address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Address at which the file system may be mounted via the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="mounttargetdnsname_nodejs">
<a href="#mounttargetdnsname_nodejs" style="color: inherit; text-decoration: inherit;">mount<wbr>Target<wbr>Dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DNS name for the given subnet/AZ per [documented convention](http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html).
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="mounttargetid_nodejs">
<a href="#mounttargetid_nodejs" style="color: inherit; text-decoration: inherit;">mount<wbr>Target<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="networkinterfaceid_nodejs">
<a href="#networkinterfaceid_nodejs" style="color: inherit; text-decoration: inherit;">network<wbr>Interface<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the network interface that Amazon EFS created when it created the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ownerid_nodejs">
<a href="#ownerid_nodejs" style="color: inherit; text-decoration: inherit;">owner<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}AWS account ID that owns the resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="securitygroups_nodejs">
<a href="#securitygroups_nodejs" style="color: inherit; text-decoration: inherit;">security<wbr>Groups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}List of VPC security group IDs attached to the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subnetid_nodejs">
<a href="#subnetid_nodejs" style="color: inherit; text-decoration: inherit;">subnet<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the mount target's subnet.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="accesspointid_nodejs">
<a href="#accesspointid_nodejs" style="color: inherit; text-decoration: inherit;">access<wbr>Point<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="availability_zone_id_python">
<a href="#availability_zone_id_python" style="color: inherit; text-decoration: inherit;">availability_<wbr>zone_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique and consistent identifier of the Availability Zone (AZ) that the mount target resides in.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availability_zone_name_python">
<a href="#availability_zone_name_python" style="color: inherit; text-decoration: inherit;">availability_<wbr>zone_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Availability Zone (AZ) that the mount target resides in.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dns_name_python">
<a href="#dns_name_python" style="color: inherit; text-decoration: inherit;">dns_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The DNS name for the EFS file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="file_system_arn_python">
<a href="#file_system_arn_python" style="color: inherit; text-decoration: inherit;">file_<wbr>system_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Amazon Resource Name of the file system for which the mount target is intended.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="file_system_id_python">
<a href="#file_system_id_python" style="color: inherit; text-decoration: inherit;">file_<wbr>system_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ip_address_python">
<a href="#ip_address_python" style="color: inherit; text-decoration: inherit;">ip_<wbr>address</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Address at which the file system may be mounted via the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="mount_target_dns_name_python">
<a href="#mount_target_dns_name_python" style="color: inherit; text-decoration: inherit;">mount_<wbr>target_<wbr>dns_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The DNS name for the given subnet/AZ per [documented convention](http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html).
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="mount_target_id_python">
<a href="#mount_target_id_python" style="color: inherit; text-decoration: inherit;">mount_<wbr>target_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="network_interface_id_python">
<a href="#network_interface_id_python" style="color: inherit; text-decoration: inherit;">network_<wbr>interface_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the network interface that Amazon EFS created when it created the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="owner_id_python">
<a href="#owner_id_python" style="color: inherit; text-decoration: inherit;">owner_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}AWS account ID that owns the resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="security_groups_python">
<a href="#security_groups_python" style="color: inherit; text-decoration: inherit;">security_<wbr>groups</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}List of VPC security group IDs attached to the mount target.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subnet_id_python">
<a href="#subnet_id_python" style="color: inherit; text-decoration: inherit;">subnet_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the mount target's subnet.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="access_point_id_python">
<a href="#access_point_id_python" style="color: inherit; text-decoration: inherit;">access_<wbr>point_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws">https://github.com/pulumi/pulumi-aws</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`aws` Terraform Provider](https://github.com/terraform-providers/terraform-provider-aws).{{% /md %}}</dd>
</dl>
