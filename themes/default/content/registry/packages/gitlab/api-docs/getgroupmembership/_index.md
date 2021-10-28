
---
title: "getGroupMembership"
title_tag: "gitlab.getGroupMembership"
meta_desc: "Documentation for the gitlab.getGroupMembership function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

## # gitlab\_group\_membership

Provide details about a list of group members in the gitlab provider. The results include id, username, name and more about the requested members.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### By group&#39;s ID


{{< example csharp >}}

```csharp
using Pulumi;
using GitLab = Pulumi.GitLab;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(GitLab.GetGroupMembership.InvokeAsync(new GitLab.GetGroupMembershipArgs
        {
            GroupId = 123,
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-gitlab/sdk/v4/go/gitlab"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := 123
		_, err := gitlab.LookupGroupMembership(ctx, &gitlab.LookupGroupMembershipArgs{
			GroupId: &opt0,
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
import pulumi_gitlab as gitlab

example = gitlab.get_group_membership(group_id=123)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as gitlab from "@pulumi/gitlab";

const example = pulumi.output(gitlab.getGroupMembership({
    groupId: 123,
}));
```


{{< /example >}}




### By group&#39;s full path


{{< example csharp >}}

```csharp
using Pulumi;
using GitLab = Pulumi.GitLab;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(GitLab.GetGroupMembership.InvokeAsync(new GitLab.GetGroupMembershipArgs
        {
            FullPath = "foo/bar",
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-gitlab/sdk/v4/go/gitlab"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "foo/bar"
		_, err := gitlab.LookupGroupMembership(ctx, &gitlab.LookupGroupMembershipArgs{
			FullPath: &opt0,
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
import pulumi_gitlab as gitlab

example = gitlab.get_group_membership(full_path="foo/bar")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as gitlab from "@pulumi/gitlab";

const example = pulumi.output(gitlab.getGroupMembership({
    fullPath: "foo/bar",
}));
```


{{< /example >}}





{{% /examples %}}




## Using getGroupMembership {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getGroupMembership<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetGroupMembershipArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetGroupMembershipResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_group_membership(</span><span class="nx">access_level</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">full_path</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                         <span class="nx">group_id</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetGroupMembershipResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupGroupMembership<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupGroupMembershipArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupGroupMembershipResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupGroupMembership` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetGroupMembership </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetGroupMembershipResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetGroupMembershipArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="accesslevel_csharp">
<a href="#accesslevel_csharp" style="color: inherit; text-decoration: inherit;">Access<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Only return members with the desired access level. Acceptable values are: `guest`, `reporter`, `developer`, `maintainer`, `owner`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="fullpath_csharp">
<a href="#fullpath_csharp" style="color: inherit; text-decoration: inherit;">Full<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The full path of the group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="groupid_csharp">
<a href="#groupid_csharp" style="color: inherit; text-decoration: inherit;">Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the group.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="accesslevel_go">
<a href="#accesslevel_go" style="color: inherit; text-decoration: inherit;">Access<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Only return members with the desired access level. Acceptable values are: `guest`, `reporter`, `developer`, `maintainer`, `owner`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="fullpath_go">
<a href="#fullpath_go" style="color: inherit; text-decoration: inherit;">Full<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The full path of the group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="groupid_go">
<a href="#groupid_go" style="color: inherit; text-decoration: inherit;">Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the group.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="accesslevel_nodejs">
<a href="#accesslevel_nodejs" style="color: inherit; text-decoration: inherit;">access<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Only return members with the desired access level. Acceptable values are: `guest`, `reporter`, `developer`, `maintainer`, `owner`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="fullpath_nodejs">
<a href="#fullpath_nodejs" style="color: inherit; text-decoration: inherit;">full<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The full path of the group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="groupid_nodejs">
<a href="#groupid_nodejs" style="color: inherit; text-decoration: inherit;">group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The ID of the group.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="access_level_python">
<a href="#access_level_python" style="color: inherit; text-decoration: inherit;">access_<wbr>level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Only return members with the desired access level. Acceptable values are: `guest`, `reporter`, `developer`, `maintainer`, `owner`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="full_path_python">
<a href="#full_path_python" style="color: inherit; text-decoration: inherit;">full_<wbr>path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The full path of the group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="group_id_python">
<a href="#group_id_python" style="color: inherit; text-decoration: inherit;">group_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the group.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getGroupMembership Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="accesslevel_csharp">
<a href="#accesslevel_csharp" style="color: inherit; text-decoration: inherit;">Access<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}One of five levels of access to the group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fullpath_csharp">
<a href="#fullpath_csharp" style="color: inherit; text-decoration: inherit;">Full<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="groupid_csharp">
<a href="#groupid_csharp" style="color: inherit; text-decoration: inherit;">Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
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
        <span id="members_csharp">
<a href="#members_csharp" style="color: inherit; text-decoration: inherit;">Members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getgroupmembershipmember">List&lt;Pulumi.<wbr>Git<wbr>Lab.<wbr>Outputs.<wbr>Get<wbr>Group<wbr>Membership<wbr>Member&gt;</a></span>
    </dt>
    <dd>{{% md %}}The list of group members.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="accesslevel_go">
<a href="#accesslevel_go" style="color: inherit; text-decoration: inherit;">Access<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}One of five levels of access to the group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fullpath_go">
<a href="#fullpath_go" style="color: inherit; text-decoration: inherit;">Full<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="groupid_go">
<a href="#groupid_go" style="color: inherit; text-decoration: inherit;">Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
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
        <span id="members_go">
<a href="#members_go" style="color: inherit; text-decoration: inherit;">Members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getgroupmembershipmember">[]Get<wbr>Group<wbr>Membership<wbr>Member</a></span>
    </dt>
    <dd>{{% md %}}The list of group members.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="accesslevel_nodejs">
<a href="#accesslevel_nodejs" style="color: inherit; text-decoration: inherit;">access<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}One of five levels of access to the group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fullpath_nodejs">
<a href="#fullpath_nodejs" style="color: inherit; text-decoration: inherit;">full<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="groupid_nodejs">
<a href="#groupid_nodejs" style="color: inherit; text-decoration: inherit;">group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
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
        <span id="members_nodejs">
<a href="#members_nodejs" style="color: inherit; text-decoration: inherit;">members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getgroupmembershipmember">Get<wbr>Group<wbr>Membership<wbr>Member[]</a></span>
    </dt>
    <dd>{{% md %}}The list of group members.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="access_level_python">
<a href="#access_level_python" style="color: inherit; text-decoration: inherit;">access_<wbr>level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}One of five levels of access to the group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="full_path_python">
<a href="#full_path_python" style="color: inherit; text-decoration: inherit;">full_<wbr>path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="group_id_python">
<a href="#group_id_python" style="color: inherit; text-decoration: inherit;">group_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
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
        <span id="members_python">
<a href="#members_python" style="color: inherit; text-decoration: inherit;">members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getgroupmembershipmember">Sequence[Get<wbr>Group<wbr>Membership<wbr>Member]</a></span>
    </dt>
    <dd>{{% md %}}The list of group members.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getgroupmembershipmember">Get<wbr>Group<wbr>Membership<wbr>Member</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="accesslevel_csharp">
<a href="#accesslevel_csharp" style="color: inherit; text-decoration: inherit;">Access<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Only return members with the desired access level. Acceptable values are: `guest`, `reporter`, `developer`, `maintainer`, `owner`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="avatarurl_csharp">
<a href="#avatarurl_csharp" style="color: inherit; text-decoration: inherit;">Avatar<wbr>Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The avatar URL of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="expiresat_csharp">
<a href="#expiresat_csharp" style="color: inherit; text-decoration: inherit;">Expires<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Expiration date for the group membership.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The unique id assigned to the user by the gitlab server.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="state_csharp">
<a href="#state_csharp" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Whether the user is active or blocked.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_csharp">
<a href="#username_csharp" style="color: inherit; text-decoration: inherit;">Username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The username of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="weburl_csharp">
<a href="#weburl_csharp" style="color: inherit; text-decoration: inherit;">Web<wbr>Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User's website URL.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="accesslevel_go">
<a href="#accesslevel_go" style="color: inherit; text-decoration: inherit;">Access<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Only return members with the desired access level. Acceptable values are: `guest`, `reporter`, `developer`, `maintainer`, `owner`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="avatarurl_go">
<a href="#avatarurl_go" style="color: inherit; text-decoration: inherit;">Avatar<wbr>Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The avatar URL of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="expiresat_go">
<a href="#expiresat_go" style="color: inherit; text-decoration: inherit;">Expires<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Expiration date for the group membership.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The unique id assigned to the user by the gitlab server.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="state_go">
<a href="#state_go" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Whether the user is active or blocked.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_go">
<a href="#username_go" style="color: inherit; text-decoration: inherit;">Username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The username of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="weburl_go">
<a href="#weburl_go" style="color: inherit; text-decoration: inherit;">Web<wbr>Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User's website URL.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="accesslevel_nodejs">
<a href="#accesslevel_nodejs" style="color: inherit; text-decoration: inherit;">access<wbr>Level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Only return members with the desired access level. Acceptable values are: `guest`, `reporter`, `developer`, `maintainer`, `owner`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="avatarurl_nodejs">
<a href="#avatarurl_nodejs" style="color: inherit; text-decoration: inherit;">avatar<wbr>Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The avatar URL of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="expiresat_nodejs">
<a href="#expiresat_nodejs" style="color: inherit; text-decoration: inherit;">expires<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Expiration date for the group membership.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The unique id assigned to the user by the gitlab server.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="state_nodejs">
<a href="#state_nodejs" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Whether the user is active or blocked.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_nodejs">
<a href="#username_nodejs" style="color: inherit; text-decoration: inherit;">username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The username of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="weburl_nodejs">
<a href="#weburl_nodejs" style="color: inherit; text-decoration: inherit;">web<wbr>Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}User's website URL.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="access_level_python">
<a href="#access_level_python" style="color: inherit; text-decoration: inherit;">access_<wbr>level</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Only return members with the desired access level. Acceptable values are: `guest`, `reporter`, `developer`, `maintainer`, `owner`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="avatar_url_python">
<a href="#avatar_url_python" style="color: inherit; text-decoration: inherit;">avatar_<wbr>url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The avatar URL of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="expires_at_python">
<a href="#expires_at_python" style="color: inherit; text-decoration: inherit;">expires_<wbr>at</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Expiration date for the group membership.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The unique id assigned to the user by the gitlab server.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="state_python">
<a href="#state_python" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Whether the user is active or blocked.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="username_python">
<a href="#username_python" style="color: inherit; text-decoration: inherit;">username</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The username of the user.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="web_url_python">
<a href="#web_url_python" style="color: inherit; text-decoration: inherit;">web_<wbr>url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}User's website URL.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-gitlab">https://github.com/pulumi/pulumi-gitlab</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`gitlab` Terraform Provider](https://github.com/gitlabhq/terraform-provider-gitlab).{{% /md %}}</dd>
</dl>
