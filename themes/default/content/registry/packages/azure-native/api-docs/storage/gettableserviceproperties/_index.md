
---
title: "getTableServiceProperties"
title_tag: "azure-native.storage.getTableServiceProperties"
meta_desc: "Documentation for the azure-native.storage.getTableServiceProperties function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

The properties of a storage account’s Table service.
API Version: 2021-02-01.




## Using getTableServiceProperties {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getTableServiceProperties<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetTableServicePropertiesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetTableServicePropertiesResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_table_service_properties(</span><span class="nx">account_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                 <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                 <span class="nx">table_service_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                 <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetTableServicePropertiesResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupTableServiceProperties<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupTableServicePropertiesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupTableServicePropertiesResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupTableServiceProperties` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetTableServiceProperties </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetTableServicePropertiesResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetTableServicePropertiesArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="accountname_csharp">
<a href="#accountname_csharp" style="color: inherit; text-decoration: inherit;">Account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="tableservicename_csharp">
<a href="#tableservicename_csharp" style="color: inherit; text-decoration: inherit;">Table<wbr>Service<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Table Service within the specified storage account. Table Service Name must be 'default'{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="accountname_go">
<a href="#accountname_go" style="color: inherit; text-decoration: inherit;">Account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="tableservicename_go">
<a href="#tableservicename_go" style="color: inherit; text-decoration: inherit;">Table<wbr>Service<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Table Service within the specified storage account. Table Service Name must be 'default'{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="accountname_nodejs">
<a href="#accountname_nodejs" style="color: inherit; text-decoration: inherit;">account<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="tableservicename_nodejs">
<a href="#tableservicename_nodejs" style="color: inherit; text-decoration: inherit;">table<wbr>Service<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Table Service within the specified storage account. Table Service Name must be 'default'{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="account_name_python">
<a href="#account_name_python" style="color: inherit; text-decoration: inherit;">account_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the storage account within the specified resource group. Storage account names must be between 3 and 24 characters in length and use numbers and lower-case letters only.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="table_service_name_python">
<a href="#table_service_name_python" style="color: inherit; text-decoration: inherit;">table_<wbr>service_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Table Service within the specified storage account. Table Service Name must be 'default'{{% /md %}}</dd></dl>
{{% /choosable %}}




## getTableServiceProperties Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="cors_csharp">
<a href="#cors_csharp" style="color: inherit; text-decoration: inherit;">Cors</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#corsrulesresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Storage.<wbr>Outputs.<wbr>Cors<wbr>Rules<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Specifies CORS rules for the Table service. You can include up to five CorsRule elements in the request. If no CorsRule elements are included in the request body, all CORS rules will be deleted, and CORS will be disabled for the Table service.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="cors_go">
<a href="#cors_go" style="color: inherit; text-decoration: inherit;">Cors</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#corsrulesresponse">Cors<wbr>Rules<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Specifies CORS rules for the Table service. You can include up to five CorsRule elements in the request. If no CorsRule elements are included in the request body, all CORS rules will be deleted, and CORS will be disabled for the Table service.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="cors_nodejs">
<a href="#cors_nodejs" style="color: inherit; text-decoration: inherit;">cors</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#corsrulesresponse">Cors<wbr>Rules<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Specifies CORS rules for the Table service. You can include up to five CorsRule elements in the request. If no CorsRule elements are included in the request body, all CORS rules will be deleted, and CORS will be disabled for the Table service.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="cors_python">
<a href="#cors_python" style="color: inherit; text-decoration: inherit;">cors</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#corsrulesresponse">Cors<wbr>Rules<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Specifies CORS rules for the Table service. You can include up to five CorsRule elements in the request. If no CorsRule elements are included in the request body, all CORS rules will be deleted, and CORS will be disabled for the Table service.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="corsruleresponse">Cors<wbr>Rule<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="allowedheaders_csharp">
<a href="#allowedheaders_csharp" style="color: inherit; text-decoration: inherit;">Allowed<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of headers allowed to be part of the cross-origin request.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="allowedmethods_csharp">
<a href="#allowedmethods_csharp" style="color: inherit; text-decoration: inherit;">Allowed<wbr>Methods</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of HTTP methods that are allowed to be executed by the origin.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="allowedorigins_csharp">
<a href="#allowedorigins_csharp" style="color: inherit; text-decoration: inherit;">Allowed<wbr>Origins</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of origin domains that will be allowed via CORS, or "*" to allow all domains{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="exposedheaders_csharp">
<a href="#exposedheaders_csharp" style="color: inherit; text-decoration: inherit;">Exposed<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of response headers to expose to CORS clients.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="maxageinseconds_csharp">
<a href="#maxageinseconds_csharp" style="color: inherit; text-decoration: inherit;">Max<wbr>Age<wbr>In<wbr>Seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. The number of seconds that the client/browser should cache a preflight response.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="allowedheaders_go">
<a href="#allowedheaders_go" style="color: inherit; text-decoration: inherit;">Allowed<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of headers allowed to be part of the cross-origin request.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="allowedmethods_go">
<a href="#allowedmethods_go" style="color: inherit; text-decoration: inherit;">Allowed<wbr>Methods</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of HTTP methods that are allowed to be executed by the origin.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="allowedorigins_go">
<a href="#allowedorigins_go" style="color: inherit; text-decoration: inherit;">Allowed<wbr>Origins</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of origin domains that will be allowed via CORS, or "*" to allow all domains{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="exposedheaders_go">
<a href="#exposedheaders_go" style="color: inherit; text-decoration: inherit;">Exposed<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of response headers to expose to CORS clients.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="maxageinseconds_go">
<a href="#maxageinseconds_go" style="color: inherit; text-decoration: inherit;">Max<wbr>Age<wbr>In<wbr>Seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. The number of seconds that the client/browser should cache a preflight response.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="allowedheaders_nodejs">
<a href="#allowedheaders_nodejs" style="color: inherit; text-decoration: inherit;">allowed<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of headers allowed to be part of the cross-origin request.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="allowedmethods_nodejs">
<a href="#allowedmethods_nodejs" style="color: inherit; text-decoration: inherit;">allowed<wbr>Methods</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of HTTP methods that are allowed to be executed by the origin.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="allowedorigins_nodejs">
<a href="#allowedorigins_nodejs" style="color: inherit; text-decoration: inherit;">allowed<wbr>Origins</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of origin domains that will be allowed via CORS, or "*" to allow all domains{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="exposedheaders_nodejs">
<a href="#exposedheaders_nodejs" style="color: inherit; text-decoration: inherit;">exposed<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of response headers to expose to CORS clients.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="maxageinseconds_nodejs">
<a href="#maxageinseconds_nodejs" style="color: inherit; text-decoration: inherit;">max<wbr>Age<wbr>In<wbr>Seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. The number of seconds that the client/browser should cache a preflight response.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="allowed_headers_python">
<a href="#allowed_headers_python" style="color: inherit; text-decoration: inherit;">allowed_<wbr>headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of headers allowed to be part of the cross-origin request.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="allowed_methods_python">
<a href="#allowed_methods_python" style="color: inherit; text-decoration: inherit;">allowed_<wbr>methods</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of HTTP methods that are allowed to be executed by the origin.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="allowed_origins_python">
<a href="#allowed_origins_python" style="color: inherit; text-decoration: inherit;">allowed_<wbr>origins</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of origin domains that will be allowed via CORS, or "*" to allow all domains{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="exposed_headers_python">
<a href="#exposed_headers_python" style="color: inherit; text-decoration: inherit;">exposed_<wbr>headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. A list of response headers to expose to CORS clients.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="max_age_in_seconds_python">
<a href="#max_age_in_seconds_python" style="color: inherit; text-decoration: inherit;">max_<wbr>age_<wbr>in_<wbr>seconds</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Required if CorsRule element is present. The number of seconds that the client/browser should cache a preflight response.{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="corsrulesresponse">Cors<wbr>Rules<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="corsrules_csharp">
<a href="#corsrules_csharp" style="color: inherit; text-decoration: inherit;">Cors<wbr>Rules</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#corsruleresponse">List&lt;Pulumi.<wbr>Azure<wbr>Native.<wbr>Storage.<wbr>Inputs.<wbr>Cors<wbr>Rule<wbr>Response&gt;</a></span>
    </dt>
    <dd>{{% md %}}The List of CORS rules. You can include up to five CorsRule elements in the request. {{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="corsrules_go">
<a href="#corsrules_go" style="color: inherit; text-decoration: inherit;">Cors<wbr>Rules</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#corsruleresponse">[]Cors<wbr>Rule<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}The List of CORS rules. You can include up to five CorsRule elements in the request. {{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="corsrules_nodejs">
<a href="#corsrules_nodejs" style="color: inherit; text-decoration: inherit;">cors<wbr>Rules</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#corsruleresponse">Cors<wbr>Rule<wbr>Response[]</a></span>
    </dt>
    <dd>{{% md %}}The List of CORS rules. You can include up to five CorsRule elements in the request. {{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="cors_rules_python">
<a href="#cors_rules_python" style="color: inherit; text-decoration: inherit;">cors_<wbr>rules</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#corsruleresponse">Sequence[Cors<wbr>Rule<wbr>Response]</a></span>
    </dt>
    <dd>{{% md %}}The List of CORS rules. You can include up to five CorsRule elements in the request. {{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
