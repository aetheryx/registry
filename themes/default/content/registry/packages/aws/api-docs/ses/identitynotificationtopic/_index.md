
---
title: "IdentityNotificationTopic"
title_tag: "aws.ses.IdentityNotificationTopic"
meta_desc: "Documentation for the aws.ses.IdentityNotificationTopic resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Resource for managing SES Identity Notification Topics

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
        var test = new Aws.Ses.IdentityNotificationTopic("test", new Aws.Ses.IdentityNotificationTopicArgs
        {
            TopicArn = aws_sns_topic.Example.Arn,
            NotificationType = "Bounce",
            Identity = aws_ses_domain_identity.Example.Domain,
            IncludeOriginalHeaders = true,
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v4/go/aws/ses"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := ses.NewIdentityNotificationTopic(ctx, "test", &ses.IdentityNotificationTopicArgs{
			TopicArn:               pulumi.Any(aws_sns_topic.Example.Arn),
			NotificationType:       pulumi.String("Bounce"),
			Identity:               pulumi.Any(aws_ses_domain_identity.Example.Domain),
			IncludeOriginalHeaders: pulumi.Bool(true),
		})
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

test = aws.ses.IdentityNotificationTopic("test",
    topic_arn=aws_sns_topic["example"]["arn"],
    notification_type="Bounce",
    identity=aws_ses_domain_identity["example"]["domain"],
    include_original_headers=True)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const test = new aws.ses.IdentityNotificationTopic("test", {
    topicArn: aws_sns_topic.example.arn,
    notificationType: "Bounce",
    identity: aws_ses_domain_identity.example.domain,
    includeOriginalHeaders: true,
});
```


{{< /example >}}





{{% /examples %}}




## Create a IdentityNotificationTopic Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">IdentityNotificationTopic</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">IdentityNotificationTopicArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">IdentityNotificationTopic</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                              <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                              <span class="nx">identity</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                              <span class="nx">include_original_headers</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
                              <span class="nx">notification_type</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                              <span class="nx">topic_arn</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">IdentityNotificationTopic</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                              <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">IdentityNotificationTopicArgs</a></span><span class="p">,</span>
                              <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewIdentityNotificationTopic</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">IdentityNotificationTopicArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">IdentityNotificationTopic</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">IdentityNotificationTopic</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">IdentityNotificationTopicArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">IdentityNotificationTopicArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language python %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">IdentityNotificationTopicArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">ResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties"><dt
        class="property-optional" title="Optional">
        <span>ctx</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span>
    </dt>
    <dd>Context object for the current deployment.</dd><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">IdentityNotificationTopicArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">IdentityNotificationTopicArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## IdentityNotificationTopic Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The IdentityNotificationTopic resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="identity_csharp">
<a href="#identity_csharp" style="color: inherit; text-decoration: inherit;">Identity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity for which the Amazon SNS topic will be set. You can specify an identity by using its name or by using its Amazon Resource Name (ARN).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notificationtype_csharp">
<a href="#notificationtype_csharp" style="color: inherit; text-decoration: inherit;">Notification<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of notifications that will be published to the specified Amazon SNS topic. Valid Values: *Bounce*, *Complaint* or *Delivery*.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="includeoriginalheaders_csharp">
<a href="#includeoriginalheaders_csharp" style="color: inherit; text-decoration: inherit;">Include<wbr>Original<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether SES should include original email headers in SNS notifications of this type. *false* by default.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="topicarn_csharp">
<a href="#topicarn_csharp" style="color: inherit; text-decoration: inherit;">Topic<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon SNS topic. Can be set to "" (an empty string) to disable publishing.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="identity_go">
<a href="#identity_go" style="color: inherit; text-decoration: inherit;">Identity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity for which the Amazon SNS topic will be set. You can specify an identity by using its name or by using its Amazon Resource Name (ARN).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notificationtype_go">
<a href="#notificationtype_go" style="color: inherit; text-decoration: inherit;">Notification<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of notifications that will be published to the specified Amazon SNS topic. Valid Values: *Bounce*, *Complaint* or *Delivery*.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="includeoriginalheaders_go">
<a href="#includeoriginalheaders_go" style="color: inherit; text-decoration: inherit;">Include<wbr>Original<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether SES should include original email headers in SNS notifications of this type. *false* by default.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="topicarn_go">
<a href="#topicarn_go" style="color: inherit; text-decoration: inherit;">Topic<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon SNS topic. Can be set to "" (an empty string) to disable publishing.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="identity_nodejs">
<a href="#identity_nodejs" style="color: inherit; text-decoration: inherit;">identity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity for which the Amazon SNS topic will be set. You can specify an identity by using its name or by using its Amazon Resource Name (ARN).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notificationtype_nodejs">
<a href="#notificationtype_nodejs" style="color: inherit; text-decoration: inherit;">notification<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of notifications that will be published to the specified Amazon SNS topic. Valid Values: *Bounce*, *Complaint* or *Delivery*.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="includeoriginalheaders_nodejs">
<a href="#includeoriginalheaders_nodejs" style="color: inherit; text-decoration: inherit;">include<wbr>Original<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether SES should include original email headers in SNS notifications of this type. *false* by default.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="topicarn_nodejs">
<a href="#topicarn_nodejs" style="color: inherit; text-decoration: inherit;">topic<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon SNS topic. Can be set to "" (an empty string) to disable publishing.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="identity_python">
<a href="#identity_python" style="color: inherit; text-decoration: inherit;">identity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The identity for which the Amazon SNS topic will be set. You can specify an identity by using its name or by using its Amazon Resource Name (ARN).
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notification_type_python">
<a href="#notification_type_python" style="color: inherit; text-decoration: inherit;">notification_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of notifications that will be published to the specified Amazon SNS topic. Valid Values: *Bounce*, *Complaint* or *Delivery*.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="include_original_headers_python">
<a href="#include_original_headers_python" style="color: inherit; text-decoration: inherit;">include_<wbr>original_<wbr>headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether SES should include original email headers in SNS notifications of this type. *false* by default.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="topic_arn_python">
<a href="#topic_arn_python" style="color: inherit; text-decoration: inherit;">topic_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon SNS topic. Can be set to "" (an empty string) to disable publishing.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the IdentityNotificationTopic resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing IdentityNotificationTopic Resource {#look-up}

Get an existing IdentityNotificationTopic resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">IdentityNotificationTopicState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">IdentityNotificationTopic</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">identity</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">include_original_headers</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
        <span class="nx">notification_type</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">topic_arn</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">) -&gt;</span> IdentityNotificationTopic</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetIdentityNotificationTopic<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">IdentityNotificationTopicState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">IdentityNotificationTopic</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">IdentityNotificationTopic</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">IdentityNotificationTopicState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_identity_csharp">
<a href="#state_identity_csharp" style="color: inherit; text-decoration: inherit;">Identity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity for which the Amazon SNS topic will be set. You can specify an identity by using its name or by using its Amazon Resource Name (ARN).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_includeoriginalheaders_csharp">
<a href="#state_includeoriginalheaders_csharp" style="color: inherit; text-decoration: inherit;">Include<wbr>Original<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether SES should include original email headers in SNS notifications of this type. *false* by default.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_notificationtype_csharp">
<a href="#state_notificationtype_csharp" style="color: inherit; text-decoration: inherit;">Notification<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of notifications that will be published to the specified Amazon SNS topic. Valid Values: *Bounce*, *Complaint* or *Delivery*.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_topicarn_csharp">
<a href="#state_topicarn_csharp" style="color: inherit; text-decoration: inherit;">Topic<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon SNS topic. Can be set to "" (an empty string) to disable publishing.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_identity_go">
<a href="#state_identity_go" style="color: inherit; text-decoration: inherit;">Identity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity for which the Amazon SNS topic will be set. You can specify an identity by using its name or by using its Amazon Resource Name (ARN).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_includeoriginalheaders_go">
<a href="#state_includeoriginalheaders_go" style="color: inherit; text-decoration: inherit;">Include<wbr>Original<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether SES should include original email headers in SNS notifications of this type. *false* by default.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_notificationtype_go">
<a href="#state_notificationtype_go" style="color: inherit; text-decoration: inherit;">Notification<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of notifications that will be published to the specified Amazon SNS topic. Valid Values: *Bounce*, *Complaint* or *Delivery*.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_topicarn_go">
<a href="#state_topicarn_go" style="color: inherit; text-decoration: inherit;">Topic<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon SNS topic. Can be set to "" (an empty string) to disable publishing.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_identity_nodejs">
<a href="#state_identity_nodejs" style="color: inherit; text-decoration: inherit;">identity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity for which the Amazon SNS topic will be set. You can specify an identity by using its name or by using its Amazon Resource Name (ARN).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_includeoriginalheaders_nodejs">
<a href="#state_includeoriginalheaders_nodejs" style="color: inherit; text-decoration: inherit;">include<wbr>Original<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether SES should include original email headers in SNS notifications of this type. *false* by default.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_notificationtype_nodejs">
<a href="#state_notificationtype_nodejs" style="color: inherit; text-decoration: inherit;">notification<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of notifications that will be published to the specified Amazon SNS topic. Valid Values: *Bounce*, *Complaint* or *Delivery*.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_topicarn_nodejs">
<a href="#state_topicarn_nodejs" style="color: inherit; text-decoration: inherit;">topic<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon SNS topic. Can be set to "" (an empty string) to disable publishing.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_identity_python">
<a href="#state_identity_python" style="color: inherit; text-decoration: inherit;">identity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The identity for which the Amazon SNS topic will be set. You can specify an identity by using its name or by using its Amazon Resource Name (ARN).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_include_original_headers_python">
<a href="#state_include_original_headers_python" style="color: inherit; text-decoration: inherit;">include_<wbr>original_<wbr>headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether SES should include original email headers in SNS notifications of this type. *false* by default.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_notification_type_python">
<a href="#state_notification_type_python" style="color: inherit; text-decoration: inherit;">notification_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of notifications that will be published to the specified Amazon SNS topic. Valid Values: *Bounce*, *Complaint* or *Delivery*.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_topic_arn_python">
<a href="#state_topic_arn_python" style="color: inherit; text-decoration: inherit;">topic_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon SNS topic. Can be set to "" (an empty string) to disable publishing.
{{% /md %}}</dd></dl>
{{% /choosable %}}





## Import


Identity Notification Topics can be imported using ID of the record. The ID is made up as IDENTITY|TYPE where IDENTITY is the SES Identity and TYPE is the Notification Type.

```sh
 $ pulumi import aws:ses/identityNotificationTopic:IdentityNotificationTopic test 'example.com|Bounce'
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws">https://github.com/pulumi/pulumi-aws</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`aws` Terraform Provider](https://github.com/terraform-providers/terraform-provider-aws).{{% /md %}}</dd>
</dl>
