
---
title: "ServiceDictionaryItemsv1"
title_tag: "fastly.ServiceDictionaryItemsv1"
meta_desc: "Documentation for the fastly.ServiceDictionaryItemsv1 resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Defines a map of Fastly dictionary items that can be used to populate a service dictionary.  This resource will populate a dictionary with the items and will track their state.

> **Warning:** This provider will take precedence over any changes you make in the UI or API. Such changes are likely to be reversed if you run the provider again.

If this provider is being used to populate the initial content of a dictionary which you intend to manage via API or UI, then the lifecycle `ignore_changes` field can be used with the resource.  An example of this configuration is provided below.

## Limitations

- `write_only` dictionaries are not supported

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### Basic usage:


{{< example csharp >}}

Coming soon!

{{< /example >}}


{{< example go >}}

Coming soon!

{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_fastly as fastly

config = pulumi.Config()
mydict_name = config.get("mydictName")
if mydict_name is None:
    mydict_name = "My Dictionary"
myservice = fastly.Servicev1("myservice",
    domains=[fastly.Servicev1DomainArgs(
        name="demo.notexample.com",
        comment="demo",
    )],
    backends=[fastly.Servicev1BackendArgs(
        address="demo.notexample.com.s3-website-us-west-2.amazonaws.com",
        name="AWS S3 hosting",
        port=80,
    )],
    dictionaries=[fastly.Servicev1DictionaryArgs(
        name=mydict_name,
    )],
    force_destroy=True)
items = []
for range in [{"key": k, "value": v} for [k, v] in enumerate({d.name: d for d in myservice.dictionaries if d.name == mydict_name})]:
    items.append(fastly.ServiceDictionaryItemsv1(f"items-{range['key']}",
        service_id=myservice.id,
        dictionary_id=range["value"],
        items={
            "key1": "value1",
            "key2": "value2",
        }))
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as fastly from "@pulumi/fastly";

const config = new pulumi.Config();
const mydictName = config.get("mydictName") || "My Dictionary";
const myservice = new fastly.Servicev1("myservice", {
    domains: [{
        name: "demo.notexample.com",
        comment: "demo",
    }],
    backends: [{
        address: "demo.notexample.com.s3-website-us-west-2.amazonaws.com",
        name: "AWS S3 hosting",
        port: 80,
    }],
    dictionaries: [{
        name: mydictName,
    }],
    forceDestroy: true,
});
const items: fastly.ServiceDictionaryItemsv1[];
for (const range of Object.entries(myservice.dictionaries.apply(dictionaries => dictionaries.filter(d => d.name == mydictName).reduce((__obj, d) => { ...__obj, [d.name]: d }))).map(([k, v]) => {key: k, value: v})) {
    items.push(new fastly.ServiceDictionaryItemsv1(`items-${range.key}`, {
        serviceId: myservice.id,
        dictionaryId: range.value.dictionaryId,
        items: {
            key1: "value1",
            key2: "value2",
        },
    }));
}
```


{{< /example >}}




### Complex object usage:


{{< example csharp >}}

Coming soon!

{{< /example >}}


{{< example go >}}

Coming soon!

{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_fastly as fastly

config = pulumi.Config()
mydict = config.get_object("mydict")
if mydict is None:
    mydict = {
        "name": "My Dictionary",
        "items": {
            "key1": "value1x",
            "key2": "value2x",
        },
    }
myservice = fastly.Servicev1("myservice",
    domains=[fastly.Servicev1DomainArgs(
        name="demo.notexample.com",
        comment="demo",
    )],
    backends=[fastly.Servicev1BackendArgs(
        address="demo.notexample.com.s3-website-us-west-2.amazonaws.com",
        name="AWS S3 hosting",
        port=80,
    )],
    dictionaries=[fastly.Servicev1DictionaryArgs(
        name=mydict["name"],
    )],
    force_destroy=True)
items = []
for range in [{"key": k, "value": v} for [k, v] in enumerate({d.name: d for d in myservice.dictionaries if d.name == mydict.name})]:
    items.append(fastly.ServiceDictionaryItemsv1(f"items-{range['key']}",
        service_id=myservice.id,
        dictionary_id=range["value"],
        items=mydict["items"]))
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as fastly from "@pulumi/fastly";

const config = new pulumi.Config();
const mydict = config.getObject("mydict") || {
    name: "My Dictionary",
    items: {
        key1: "value1x",
        key2: "value2x",
    },
};
const myservice = new fastly.Servicev1("myservice", {
    domains: [{
        name: "demo.notexample.com",
        comment: "demo",
    }],
    backends: [{
        address: "demo.notexample.com.s3-website-us-west-2.amazonaws.com",
        name: "AWS S3 hosting",
        port: 80,
    }],
    dictionaries: [{
        name: mydict.name,
    }],
    forceDestroy: true,
});
const items: fastly.ServiceDictionaryItemsv1[];
for (const range of Object.entries(myservice.dictionaries.apply(dictionaries => dictionaries.filter(d => d.name == mydict.name).reduce((__obj, d) => { ...__obj, [d.name]: d }))).map(([k, v]) => {key: k, value: v})) {
    items.push(new fastly.ServiceDictionaryItemsv1(`items-${range.key}`, {
        serviceId: myservice.id,
        dictionaryId: range.value.dictionaryId,
        items: mydict.items,
    }));
}
```


{{< /example >}}





{{% /examples %}}




## Create a ServiceDictionaryItemsv1 Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">ServiceDictionaryItemsv1</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">ServiceDictionaryItemsv1Args</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">ServiceDictionaryItemsv1</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                             <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                             <span class="nx">dictionary_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                             <span class="nx">items</span><span class="p">:</span> <span class="nx">Optional[Mapping[str, Any]]</span> = None<span class="p">,</span>
                             <span class="nx">service_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">ServiceDictionaryItemsv1</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                             <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">ServiceDictionaryItemsv1Args</a></span><span class="p">,</span>
                             <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewServiceDictionaryItemsv1</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">ServiceDictionaryItemsv1Args</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">ServiceDictionaryItemsv1</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">ServiceDictionaryItemsv1</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">ServiceDictionaryItemsv1Args</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">ServiceDictionaryItemsv1Args</a></span>
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
        <span class="property-type"><a href="#inputs">ServiceDictionaryItemsv1Args</a></span>
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
        <span class="property-type"><a href="#inputs">ServiceDictionaryItemsv1Args</a></span>
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
        <span class="property-type"><a href="#inputs">ServiceDictionaryItemsv1Args</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## ServiceDictionaryItemsv1 Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The ServiceDictionaryItemsv1 resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="dictionaryid_csharp">
<a href="#dictionaryid_csharp" style="color: inherit; text-decoration: inherit;">Dictionary<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dictionary that the items belong to
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="serviceid_csharp">
<a href="#serviceid_csharp" style="color: inherit; text-decoration: inherit;">Service<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the service that the dictionary belongs to
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="items_csharp">
<a href="#items_csharp" style="color: inherit; text-decoration: inherit;">Items</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, object&gt;</span>
    </dt>
    <dd>{{% md %}}A map representing an entry in the dictionary, (key/value)
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="dictionaryid_go">
<a href="#dictionaryid_go" style="color: inherit; text-decoration: inherit;">Dictionary<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dictionary that the items belong to
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="serviceid_go">
<a href="#serviceid_go" style="color: inherit; text-decoration: inherit;">Service<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the service that the dictionary belongs to
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="items_go">
<a href="#items_go" style="color: inherit; text-decoration: inherit;">Items</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A map representing an entry in the dictionary, (key/value)
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="dictionaryid_nodejs">
<a href="#dictionaryid_nodejs" style="color: inherit; text-decoration: inherit;">dictionary<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dictionary that the items belong to
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="serviceid_nodejs">
<a href="#serviceid_nodejs" style="color: inherit; text-decoration: inherit;">service<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the service that the dictionary belongs to
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="items_nodejs">
<a href="#items_nodejs" style="color: inherit; text-decoration: inherit;">items</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}A map representing an entry in the dictionary, (key/value)
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="dictionary_id_python">
<a href="#dictionary_id_python" style="color: inherit; text-decoration: inherit;">dictionary_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the dictionary that the items belong to
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="service_id_python">
<a href="#service_id_python" style="color: inherit; text-decoration: inherit;">service_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the service that the dictionary belongs to
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="items_python">
<a href="#items_python" style="color: inherit; text-decoration: inherit;">items</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, Any]</span>
    </dt>
    <dd>{{% md %}}A map representing an entry in the dictionary, (key/value)
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the ServiceDictionaryItemsv1 resource produces the following output properties:



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



## Look up an Existing ServiceDictionaryItemsv1 Resource {#look-up}

Get an existing ServiceDictionaryItemsv1 resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">ServiceDictionaryItemsv1State</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">ServiceDictionaryItemsv1</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">dictionary_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">items</span><span class="p">:</span> <span class="nx">Optional[Mapping[str, Any]]</span> = None<span class="p">,</span>
        <span class="nx">service_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">) -&gt;</span> ServiceDictionaryItemsv1</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetServiceDictionaryItemsv1<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">ServiceDictionaryItemsv1State</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">ServiceDictionaryItemsv1</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">ServiceDictionaryItemsv1</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">ServiceDictionaryItemsv1State</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span id="state_dictionaryid_csharp">
<a href="#state_dictionaryid_csharp" style="color: inherit; text-decoration: inherit;">Dictionary<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dictionary that the items belong to
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_items_csharp">
<a href="#state_items_csharp" style="color: inherit; text-decoration: inherit;">Items</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, object&gt;</span>
    </dt>
    <dd>{{% md %}}A map representing an entry in the dictionary, (key/value)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_serviceid_csharp">
<a href="#state_serviceid_csharp" style="color: inherit; text-decoration: inherit;">Service<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the service that the dictionary belongs to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_dictionaryid_go">
<a href="#state_dictionaryid_go" style="color: inherit; text-decoration: inherit;">Dictionary<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dictionary that the items belong to
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_items_go">
<a href="#state_items_go" style="color: inherit; text-decoration: inherit;">Items</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]interface{}</span>
    </dt>
    <dd>{{% md %}}A map representing an entry in the dictionary, (key/value)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_serviceid_go">
<a href="#state_serviceid_go" style="color: inherit; text-decoration: inherit;">Service<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the service that the dictionary belongs to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_dictionaryid_nodejs">
<a href="#state_dictionaryid_nodejs" style="color: inherit; text-decoration: inherit;">dictionary<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the dictionary that the items belong to
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_items_nodejs">
<a href="#state_items_nodejs" style="color: inherit; text-decoration: inherit;">items</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: any}</span>
    </dt>
    <dd>{{% md %}}A map representing an entry in the dictionary, (key/value)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_serviceid_nodejs">
<a href="#state_serviceid_nodejs" style="color: inherit; text-decoration: inherit;">service<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the service that the dictionary belongs to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_dictionary_id_python">
<a href="#state_dictionary_id_python" style="color: inherit; text-decoration: inherit;">dictionary_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the dictionary that the items belong to
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_items_python">
<a href="#state_items_python" style="color: inherit; text-decoration: inherit;">items</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, Any]</span>
    </dt>
    <dd>{{% md %}}A map representing an entry in the dictionary, (key/value)
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_service_id_python">
<a href="#state_service_id_python" style="color: inherit; text-decoration: inherit;">service_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the service that the dictionary belongs to
{{% /md %}}</dd></dl>
{{% /choosable %}}





## Import


This is an example of the import command being applied to the resource named `fastly_service_dictionary_items_v1.items` The resource ID is a combined value of the `service_id` and `dictionary_id` separated by a forward slash.

```sh
 $ pulumi import fastly:index/serviceDictionaryItemsv1:ServiceDictionaryItemsv1 items xxxxxxxxxxxxxxxxxxxx/xxxxxxxxxxxxxxxxxxxx
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-fastly">https://github.com/pulumi/pulumi-fastly</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`fastly` Terraform Provider](https://github.com/fastly/terraform-provider-fastly).{{% /md %}}</dd>
</dl>
