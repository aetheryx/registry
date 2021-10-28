
---
title: "Email"
title_tag: "okta.template.Email"
meta_desc: "Documentation for the okta.template.Email resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Creates an Okta Email Template.

This resource allows you to create and configure an Okta Email Template.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Okta = Pulumi.Okta;

class MyStack : Stack
{
    public MyStack()
    {
        var example = new Okta.Template.Email("example", new Okta.Template.EmailArgs
        {
            Translations = 
            {
                new Okta.Template.Inputs.EmailTranslationArgs
                {
                    Language = "en",
                    Subject = "Stuff",
                    Template = "Hi $user.firstName,<br/><br/>Blah blah $resetPasswordLink",
                },
                new Okta.Template.Inputs.EmailTranslationArgs
                {
                    Language = "es",
                    Subject = "Cosas",
                    Template = "Hola $user.firstName,<br/><br/>Puedo ir al bano $resetPasswordLink",
                },
            },
            Type = "email.forgotPassword",
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"fmt"

	"github.com/pulumi/pulumi-okta/sdk/v3/go/okta/template"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := template.NewEmail(ctx, "example", &template.EmailArgs{
			Translations: template.EmailTranslationArray{
				&template.EmailTranslationArgs{
					Language: pulumi.String("en"),
					Subject:  pulumi.String("Stuff"),
					Template: pulumi.String(fmt.Sprintf("%v%v%v%v%v", "Hi ", "$", "user.firstName,<br/><br/>Blah blah ", "$", "resetPasswordLink")),
				},
				&template.EmailTranslationArgs{
					Language: pulumi.String("es"),
					Subject:  pulumi.String("Cosas"),
					Template: pulumi.String(fmt.Sprintf("%v%v%v%v%v", "Hola ", "$", "user.firstName,<br/><br/>Puedo ir al bano ", "$", "resetPasswordLink")),
				},
			},
			Type: pulumi.String("email.forgotPassword"),
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
import pulumi_okta as okta

example = okta.template.Email("example",
    translations=[
        okta.template.EmailTranslationArgs(
            language="en",
            subject="Stuff",
            template="Hi $user.firstName,<br/><br/>Blah blah $resetPasswordLink",
        ),
        okta.template.EmailTranslationArgs(
            language="es",
            subject="Cosas",
            template="Hola $user.firstName,<br/><br/>Puedo ir al bano $resetPasswordLink",
        ),
    ],
    type="email.forgotPassword")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as okta from "@pulumi/okta";

const example = new okta.template.Email("example", {
    translations: [
        {
            language: "en",
            subject: "Stuff",
            template: "Hi $user.firstName,<br/><br/>Blah blah $resetPasswordLink",
        },
        {
            language: "es",
            subject: "Cosas",
            template: "Hola $user.firstName,<br/><br/>Puedo ir al bano $resetPasswordLink",
        },
    ],
    type: "email.forgotPassword",
});
```


{{< /example >}}





{{% /examples %}}




## Create a Email Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Email</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">EmailArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Email</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
          <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
          <span class="nx">default_language</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
          <span class="nx">translations</span><span class="p">:</span> <span class="nx">Optional[Sequence[EmailTranslationArgs]]</span> = None<span class="p">,</span>
          <span class="nx">type</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Email</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
          <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">EmailArgs</a></span><span class="p">,</span>
          <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewEmail</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">EmailArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Email</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Email</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">EmailArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">EmailArgs</a></span>
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
        <span class="property-type"><a href="#inputs">EmailArgs</a></span>
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
        <span class="property-type"><a href="#inputs">EmailArgs</a></span>
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
        <span class="property-type"><a href="#inputs">EmailArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Email Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Email resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="translations_csharp">
<a href="#translations_csharp" style="color: inherit; text-decoration: inherit;">Translations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#emailtranslation">List&lt;Email<wbr>Translation<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Set of translations for a particular template.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Email template type
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="defaultlanguage_csharp">
<a href="#defaultlanguage_csharp" style="color: inherit; text-decoration: inherit;">Default<wbr>Language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default language, by default is set to `"en"`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="translations_go">
<a href="#translations_go" style="color: inherit; text-decoration: inherit;">Translations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#emailtranslation">[]Email<wbr>Translation<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}Set of translations for a particular template.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Email template type
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="defaultlanguage_go">
<a href="#defaultlanguage_go" style="color: inherit; text-decoration: inherit;">Default<wbr>Language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default language, by default is set to `"en"`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="translations_nodejs">
<a href="#translations_nodejs" style="color: inherit; text-decoration: inherit;">translations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#emailtranslation">Email<wbr>Translation<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}Set of translations for a particular template.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Email template type
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="defaultlanguage_nodejs">
<a href="#defaultlanguage_nodejs" style="color: inherit; text-decoration: inherit;">default<wbr>Language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default language, by default is set to `"en"`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="translations_python">
<a href="#translations_python" style="color: inherit; text-decoration: inherit;">translations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#emailtranslation">Sequence[Email<wbr>Translation<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}Set of translations for a particular template.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Email template type
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="default_language_python">
<a href="#default_language_python" style="color: inherit; text-decoration: inherit;">default_<wbr>language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The default language, by default is set to `"en"`.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Email resource produces the following output properties:



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



## Look up an Existing Email Resource {#look-up}

Get an existing Email resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">EmailState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">Email</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">default_language</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">translations</span><span class="p">:</span> <span class="nx">Optional[Sequence[EmailTranslationArgs]]</span> = None<span class="p">,</span>
        <span class="nx">type</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">) -&gt;</span> Email</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetEmail<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">EmailState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Email</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">Email</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">EmailState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span id="state_defaultlanguage_csharp">
<a href="#state_defaultlanguage_csharp" style="color: inherit; text-decoration: inherit;">Default<wbr>Language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default language, by default is set to `"en"`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_translations_csharp">
<a href="#state_translations_csharp" style="color: inherit; text-decoration: inherit;">Translations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#emailtranslation">List&lt;Email<wbr>Translation<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Set of translations for a particular template.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_type_csharp">
<a href="#state_type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Email template type
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_defaultlanguage_go">
<a href="#state_defaultlanguage_go" style="color: inherit; text-decoration: inherit;">Default<wbr>Language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default language, by default is set to `"en"`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_translations_go">
<a href="#state_translations_go" style="color: inherit; text-decoration: inherit;">Translations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#emailtranslation">[]Email<wbr>Translation<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}Set of translations for a particular template.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_type_go">
<a href="#state_type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Email template type
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_defaultlanguage_nodejs">
<a href="#state_defaultlanguage_nodejs" style="color: inherit; text-decoration: inherit;">default<wbr>Language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The default language, by default is set to `"en"`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_translations_nodejs">
<a href="#state_translations_nodejs" style="color: inherit; text-decoration: inherit;">translations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#emailtranslation">Email<wbr>Translation<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}Set of translations for a particular template.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_type_nodejs">
<a href="#state_type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Email template type
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_default_language_python">
<a href="#state_default_language_python" style="color: inherit; text-decoration: inherit;">default_<wbr>language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The default language, by default is set to `"en"`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_translations_python">
<a href="#state_translations_python" style="color: inherit; text-decoration: inherit;">translations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#emailtranslation">Sequence[Email<wbr>Translation<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}Set of translations for a particular template.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_type_python">
<a href="#state_type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Email template type
{{% /md %}}</dd></dl>
{{% /choosable %}}






## Supporting Types



<h4 id="emailtranslation">Email<wbr>Translation</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="language_csharp">
<a href="#language_csharp" style="color: inherit; text-decoration: inherit;">Language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The language to map the template to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="subject_csharp">
<a href="#subject_csharp" style="color: inherit; text-decoration: inherit;">Subject</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The email subject line.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="template_csharp">
<a href="#template_csharp" style="color: inherit; text-decoration: inherit;">Template</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The email body.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="language_go">
<a href="#language_go" style="color: inherit; text-decoration: inherit;">Language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The language to map the template to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="subject_go">
<a href="#subject_go" style="color: inherit; text-decoration: inherit;">Subject</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The email subject line.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="template_go">
<a href="#template_go" style="color: inherit; text-decoration: inherit;">Template</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The email body.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="language_nodejs">
<a href="#language_nodejs" style="color: inherit; text-decoration: inherit;">language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The language to map the template to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="subject_nodejs">
<a href="#subject_nodejs" style="color: inherit; text-decoration: inherit;">subject</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The email subject line.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="template_nodejs">
<a href="#template_nodejs" style="color: inherit; text-decoration: inherit;">template</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The email body.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="language_python">
<a href="#language_python" style="color: inherit; text-decoration: inherit;">language</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The language to map the template to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="subject_python">
<a href="#subject_python" style="color: inherit; text-decoration: inherit;">subject</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The email subject line.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="template_python">
<a href="#template_python" style="color: inherit; text-decoration: inherit;">template</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The email body.
{{% /md %}}</dd></dl>
{{% /choosable %}}
## Import


An Okta Email Template can be imported via the template type.

```sh
 $ pulumi import okta:template/email:Email example <template type>
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-okta">https://github.com/pulumi/pulumi-okta</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`okta` Terraform Provider](https://github.com/okta/terraform-provider-okta).{{% /md %}}</dd>
</dl>
