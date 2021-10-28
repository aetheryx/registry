
---
title: "Input"
title_tag: "aws-native.iotevents.Input"
meta_desc: "Documentation for the aws-native.iotevents.Input resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

The AWS::IoTEvents::Input resource creates an input. To monitor your devices and processes, they must have a way to get telemetry data into AWS IoT Events. This is done by sending messages as *inputs* to AWS IoT Events. For more information, see [How to Use AWS IoT Events](https://docs.aws.amazon.com/iotevents/latest/developerguide/how-to-use-iotevents.html) in the *AWS IoT Events Developer Guide*.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### Example


{{< example csharp >}}

```csharp
using Pulumi;
using AwsNative = Pulumi.AwsNative;

class MyStack : Stack
{
    public MyStack()
    {
        var myInput = new AwsNative.IoTEvents.Input("myInput", new AwsNative.IoTEvents.InputArgs
        {
            InputName = "myInput",
            InputDescription = "My Input created by CloudFormation",
            InputDefinition = new AwsNative.IoTEvents.Inputs.InputDefinitionArgs
            {
                Attributes = 
                {
                    new AwsNative.IoTEvents.Inputs.InputAttributeArgs
                    {
                        JsonPath = "foo",
                    },
                    new AwsNative.IoTEvents.Inputs.InputAttributeArgs
                    {
                        JsonPath = "bar",
                    },
                },
            },
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/iotevents"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := iotevents.NewInput(ctx, "myInput", &iotevents.InputArgs{
			InputName:        pulumi.String("myInput"),
			InputDescription: pulumi.String("My Input created by CloudFormation"),
			InputDefinition: &iotevents.InputDefinitionArgs{
				Attributes: iotevents.InputAttributeArray{
					&iotevents.InputAttributeArgs{
						JsonPath: pulumi.String("foo"),
					},
					&iotevents.InputAttributeArgs{
						JsonPath: pulumi.String("bar"),
					},
				},
			},
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
import pulumi_aws_native as aws_native

my_input = aws_native.iotevents.Input("myInput",
    input_name="myInput",
    input_description="My Input created by CloudFormation",
    input_definition=aws_native.iotevents.InputDefinitionArgs(
        attributes=[
            aws_native.iotevents.InputAttributeArgs(
                json_path="foo",
            ),
            aws_native.iotevents.InputAttributeArgs(
                json_path="bar",
            ),
        ],
    ))

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myInput = new aws_native.iotevents.Input("myInput", {
    inputName: "myInput",
    inputDescription: "My Input created by CloudFormation",
    inputDefinition: {
        attributes: [
            {
                jsonPath: "foo",
            },
            {
                jsonPath: "bar",
            },
        ],
    },
});

```


{{< /example >}}




### Example


{{< example csharp >}}

```csharp
using Pulumi;
using AwsNative = Pulumi.AwsNative;

class MyStack : Stack
{
    public MyStack()
    {
        var myInput = new AwsNative.IoTEvents.Input("myInput", new AwsNative.IoTEvents.InputArgs
        {
            InputName = "myInput",
            InputDescription = "My Input created by CloudFormation",
            InputDefinition = new AwsNative.IoTEvents.Inputs.InputDefinitionArgs
            {
                Attributes = 
                {
                    new AwsNative.IoTEvents.Inputs.InputAttributeArgs
                    {
                        JsonPath = "foo",
                    },
                    new AwsNative.IoTEvents.Inputs.InputAttributeArgs
                    {
                        JsonPath = "bar",
                    },
                },
            },
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/iotevents"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := iotevents.NewInput(ctx, "myInput", &iotevents.InputArgs{
			InputName:        pulumi.String("myInput"),
			InputDescription: pulumi.String("My Input created by CloudFormation"),
			InputDefinition: &iotevents.InputDefinitionArgs{
				Attributes: iotevents.InputAttributeArray{
					&iotevents.InputAttributeArgs{
						JsonPath: pulumi.String("foo"),
					},
					&iotevents.InputAttributeArgs{
						JsonPath: pulumi.String("bar"),
					},
				},
			},
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
import pulumi_aws_native as aws_native

my_input = aws_native.iotevents.Input("myInput",
    input_name="myInput",
    input_description="My Input created by CloudFormation",
    input_definition=aws_native.iotevents.InputDefinitionArgs(
        attributes=[
            aws_native.iotevents.InputAttributeArgs(
                json_path="foo",
            ),
            aws_native.iotevents.InputAttributeArgs(
                json_path="bar",
            ),
        ],
    ))

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myInput = new aws_native.iotevents.Input("myInput", {
    inputName: "myInput",
    inputDescription: "My Input created by CloudFormation",
    inputDefinition: {
        attributes: [
            {
                jsonPath: "foo",
            },
            {
                jsonPath: "bar",
            },
        ],
    },
});

```


{{< /example >}}





{{% /examples %}}




## Create a Input Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Input</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">InputArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Input</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
          <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
          <span class="nx">input_definition</span><span class="p">:</span> <span class="nx">Optional[InputDefinitionArgs]</span> = None<span class="p">,</span>
          <span class="nx">input_description</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
          <span class="nx">input_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
          <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Sequence[InputTagArgs]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Input</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
          <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">InputArgs</a></span><span class="p">,</span>
          <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewInput</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">InputArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Input</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Input</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">InputArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">InputArgs</a></span>
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
        <span class="property-type"><a href="#inputs">InputArgs</a></span>
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
        <span class="property-type"><a href="#inputs">InputArgs</a></span>
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
        <span class="property-type"><a href="#inputs">InputArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Input Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Input resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="inputdefinition_csharp">
<a href="#inputdefinition_csharp" style="color: inherit; text-decoration: inherit;">Input<wbr>Definition</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputdefinition">Pulumi.<wbr>Aws<wbr>Native.<wbr>Io<wbr>TEvents.<wbr>Inputs.<wbr>Input<wbr>Definition<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="inputdescription_csharp">
<a href="#inputdescription_csharp" style="color: inherit; text-decoration: inherit;">Input<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A brief description of the input.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="inputname_csharp">
<a href="#inputname_csharp" style="color: inherit; text-decoration: inherit;">Input<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the input.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputtag">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Io<wbr>TEvents.<wbr>Inputs.<wbr>Input<wbr>Tag<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}An array of key-value pairs to apply to this resource.

For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html).{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="inputdefinition_go">
<a href="#inputdefinition_go" style="color: inherit; text-decoration: inherit;">Input<wbr>Definition</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputdefinition">Input<wbr>Definition<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="inputdescription_go">
<a href="#inputdescription_go" style="color: inherit; text-decoration: inherit;">Input<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A brief description of the input.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="inputname_go">
<a href="#inputname_go" style="color: inherit; text-decoration: inherit;">Input<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the input.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputtag">[]Input<wbr>Tag<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}An array of key-value pairs to apply to this resource.

For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html).{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="inputdefinition_nodejs">
<a href="#inputdefinition_nodejs" style="color: inherit; text-decoration: inherit;">input<wbr>Definition</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputdefinition">Input<wbr>Definition<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="inputdescription_nodejs">
<a href="#inputdescription_nodejs" style="color: inherit; text-decoration: inherit;">input<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A brief description of the input.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="inputname_nodejs">
<a href="#inputname_nodejs" style="color: inherit; text-decoration: inherit;">input<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the input.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputtag">Input<wbr>Tag<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}An array of key-value pairs to apply to this resource.

For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html).{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="input_definition_python">
<a href="#input_definition_python" style="color: inherit; text-decoration: inherit;">input_<wbr>definition</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputdefinition">Input<wbr>Definition<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="input_description_python">
<a href="#input_description_python" style="color: inherit; text-decoration: inherit;">input_<wbr>description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A brief description of the input.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="input_name_python">
<a href="#input_name_python" style="color: inherit; text-decoration: inherit;">input_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the input.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputtag">Sequence[Input<wbr>Tag<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}An array of key-value pairs to apply to this resource.

For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html).{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Input resource produces the following output properties:



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







## Supporting Types



<h4 id="inputattribute">Input<wbr>Attribute</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="jsonpath_csharp">
<a href="#jsonpath_csharp" style="color: inherit; text-decoration: inherit;">Json<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An expression that specifies an attribute-value pair in a JSON structure. Use this to specify an attribute from the JSON payload that is made available by the input. Inputs are derived from messages sent to AWS IoT Events (`BatchPutMessage`). Each such message contains a JSON payload. The attribute (and its paired value) specified here are available for use in the `condition` expressions used by detectors.

_Syntax_: `<field-name>.<field-name>...`{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="jsonpath_go">
<a href="#jsonpath_go" style="color: inherit; text-decoration: inherit;">Json<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An expression that specifies an attribute-value pair in a JSON structure. Use this to specify an attribute from the JSON payload that is made available by the input. Inputs are derived from messages sent to AWS IoT Events (`BatchPutMessage`). Each such message contains a JSON payload. The attribute (and its paired value) specified here are available for use in the `condition` expressions used by detectors.

_Syntax_: `<field-name>.<field-name>...`{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="jsonpath_nodejs">
<a href="#jsonpath_nodejs" style="color: inherit; text-decoration: inherit;">json<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An expression that specifies an attribute-value pair in a JSON structure. Use this to specify an attribute from the JSON payload that is made available by the input. Inputs are derived from messages sent to AWS IoT Events (`BatchPutMessage`). Each such message contains a JSON payload. The attribute (and its paired value) specified here are available for use in the `condition` expressions used by detectors.

_Syntax_: `<field-name>.<field-name>...`{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="json_path_python">
<a href="#json_path_python" style="color: inherit; text-decoration: inherit;">json_<wbr>path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An expression that specifies an attribute-value pair in a JSON structure. Use this to specify an attribute from the JSON payload that is made available by the input. Inputs are derived from messages sent to AWS IoT Events (`BatchPutMessage`). Each such message contains a JSON payload. The attribute (and its paired value) specified here are available for use in the `condition` expressions used by detectors.

_Syntax_: `<field-name>.<field-name>...`{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="inputdefinition">Input<wbr>Definition</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="attributes_csharp">
<a href="#attributes_csharp" style="color: inherit; text-decoration: inherit;">Attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputattribute">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Io<wbr>TEvents.<wbr>Inputs.<wbr>Input<wbr>Attribute&gt;</a></span>
    </dt>
    <dd>{{% md %}}The attributes from the JSON payload that are made available by the input. Inputs are derived from messages sent to the AWS IoT Events system using `BatchPutMessage`. Each such message contains a JSON payload, and those attributes (and their paired values) specified here are available for use in the `condition` expressions used by detectors that monitor this input.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="attributes_go">
<a href="#attributes_go" style="color: inherit; text-decoration: inherit;">Attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputattribute">[]Input<wbr>Attribute</a></span>
    </dt>
    <dd>{{% md %}}The attributes from the JSON payload that are made available by the input. Inputs are derived from messages sent to the AWS IoT Events system using `BatchPutMessage`. Each such message contains a JSON payload, and those attributes (and their paired values) specified here are available for use in the `condition` expressions used by detectors that monitor this input.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="attributes_nodejs">
<a href="#attributes_nodejs" style="color: inherit; text-decoration: inherit;">attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputattribute">Input<wbr>Attribute[]</a></span>
    </dt>
    <dd>{{% md %}}The attributes from the JSON payload that are made available by the input. Inputs are derived from messages sent to the AWS IoT Events system using `BatchPutMessage`. Each such message contains a JSON payload, and those attributes (and their paired values) specified here are available for use in the `condition` expressions used by detectors that monitor this input.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="attributes_python">
<a href="#attributes_python" style="color: inherit; text-decoration: inherit;">attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputattribute">Sequence[Input<wbr>Attribute]</a></span>
    </dt>
    <dd>{{% md %}}The attributes from the JSON payload that are made available by the input. Inputs are derived from messages sent to the AWS IoT Events system using `BatchPutMessage`. Each such message contains a JSON payload, and those attributes (and their paired values) specified here are available for use in the `condition` expressions used by detectors that monitor this input.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="inputtag">Input<wbr>Tag</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_csharp">
<a href="#key_csharp" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Key of the Tag.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_csharp">
<a href="#value_csharp" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value of the Tag.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_go">
<a href="#key_go" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Key of the Tag.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_go">
<a href="#value_go" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value of the Tag.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_nodejs">
<a href="#key_nodejs" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Key of the Tag.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_nodejs">
<a href="#value_nodejs" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Value of the Tag.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_python">
<a href="#key_python" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Key of the Tag.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_python">
<a href="#value_python" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Value of the Tag.{{% /md %}}</dd></dl>
{{% /choosable %}}


<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws-native">https://github.com/pulumi/pulumi-aws-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
