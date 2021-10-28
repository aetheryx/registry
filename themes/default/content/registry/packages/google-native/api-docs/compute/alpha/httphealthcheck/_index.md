
---
title: "HttpHealthCheck"
title_tag: "google-native.compute/alpha.HttpHealthCheck"
meta_desc: "Documentation for the google-native.compute/alpha.HttpHealthCheck resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Creates a HttpHealthCheck resource in the specified project using the data included in the request.




## Create a HttpHealthCheck Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">HttpHealthCheck</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">?:</span> <span class="nx"><a href="#inputs">HttpHealthCheckArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">HttpHealthCheck</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                    <span class="nx">check_interval_sec</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                    <span class="nx">description</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">healthy_threshold</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                    <span class="nx">host</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">port</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                    <span class="nx">project</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">request_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">request_path</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">timeout_sec</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                    <span class="nx">unhealthy_threshold</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">HttpHealthCheck</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                    <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">Optional[HttpHealthCheckArgs]</a></span> = None<span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewHttpHealthCheck</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx"><a href="#inputs">HttpHealthCheckArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">HttpHealthCheck</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">HttpHealthCheck</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">HttpHealthCheckArgs</a></span><span class="p">? </span><span class="nx">args = null<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">HttpHealthCheckArgs</a></span>
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
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">HttpHealthCheckArgs</a></span>
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
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">HttpHealthCheckArgs</a></span>
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
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">HttpHealthCheckArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## HttpHealthCheck Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The HttpHealthCheck resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="checkintervalsec_csharp">
<a href="#checkintervalsec_csharp" style="color: inherit; text-decoration: inherit;">Check<wbr>Interval<wbr>Sec</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How often (in seconds) to send a health check. The default value is 5 seconds.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="healthythreshold_csharp">
<a href="#healthythreshold_csharp" style="color: inherit; text-decoration: inherit;">Healthy<wbr>Threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}A so-far unhealthy instance will be marked healthy after this many consecutive successes. The default value is 2.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="host_csharp">
<a href="#host_csharp" style="color: inherit; text-decoration: inherit;">Host</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value of the host header in the HTTP health check request. If left empty (default value), the public IP on behalf of which this health check is performed will be used.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression `[a-z]([-a-z0-9]*[a-z0-9])?` which means the first character must be a lowercase letter, and all following characters must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="port_csharp">
<a href="#port_csharp" style="color: inherit; text-decoration: inherit;">Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The TCP port number for the HTTP health check request. The default value is 80.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_csharp">
<a href="#project_csharp" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="requestid_csharp">
<a href="#requestid_csharp" style="color: inherit; text-decoration: inherit;">Request<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="requestpath_csharp">
<a href="#requestpath_csharp" style="color: inherit; text-decoration: inherit;">Request<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The request path of the HTTP health check request. The default value is /. This field does not support query parameters.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="timeoutsec_csharp">
<a href="#timeoutsec_csharp" style="color: inherit; text-decoration: inherit;">Timeout<wbr>Sec</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How long (in seconds) to wait before claiming failure. The default value is 5 seconds. It is invalid for timeoutSec to have greater value than checkIntervalSec.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="unhealthythreshold_csharp">
<a href="#unhealthythreshold_csharp" style="color: inherit; text-decoration: inherit;">Unhealthy<wbr>Threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}A so-far healthy instance will be marked unhealthy after this many consecutive failures. The default value is 2.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="checkintervalsec_go">
<a href="#checkintervalsec_go" style="color: inherit; text-decoration: inherit;">Check<wbr>Interval<wbr>Sec</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How often (in seconds) to send a health check. The default value is 5 seconds.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="healthythreshold_go">
<a href="#healthythreshold_go" style="color: inherit; text-decoration: inherit;">Healthy<wbr>Threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}A so-far unhealthy instance will be marked healthy after this many consecutive successes. The default value is 2.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="host_go">
<a href="#host_go" style="color: inherit; text-decoration: inherit;">Host</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value of the host header in the HTTP health check request. If left empty (default value), the public IP on behalf of which this health check is performed will be used.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression `[a-z]([-a-z0-9]*[a-z0-9])?` which means the first character must be a lowercase letter, and all following characters must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="port_go">
<a href="#port_go" style="color: inherit; text-decoration: inherit;">Port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The TCP port number for the HTTP health check request. The default value is 80.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_go">
<a href="#project_go" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="requestid_go">
<a href="#requestid_go" style="color: inherit; text-decoration: inherit;">Request<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="requestpath_go">
<a href="#requestpath_go" style="color: inherit; text-decoration: inherit;">Request<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The request path of the HTTP health check request. The default value is /. This field does not support query parameters.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="timeoutsec_go">
<a href="#timeoutsec_go" style="color: inherit; text-decoration: inherit;">Timeout<wbr>Sec</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How long (in seconds) to wait before claiming failure. The default value is 5 seconds. It is invalid for timeoutSec to have greater value than checkIntervalSec.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="unhealthythreshold_go">
<a href="#unhealthythreshold_go" style="color: inherit; text-decoration: inherit;">Unhealthy<wbr>Threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}A so-far healthy instance will be marked unhealthy after this many consecutive failures. The default value is 2.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="checkintervalsec_nodejs">
<a href="#checkintervalsec_nodejs" style="color: inherit; text-decoration: inherit;">check<wbr>Interval<wbr>Sec</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}How often (in seconds) to send a health check. The default value is 5 seconds.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="healthythreshold_nodejs">
<a href="#healthythreshold_nodejs" style="color: inherit; text-decoration: inherit;">healthy<wbr>Threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}A so-far unhealthy instance will be marked healthy after this many consecutive successes. The default value is 2.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="host_nodejs">
<a href="#host_nodejs" style="color: inherit; text-decoration: inherit;">host</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value of the host header in the HTTP health check request. If left empty (default value), the public IP on behalf of which this health check is performed will be used.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression `[a-z]([-a-z0-9]*[a-z0-9])?` which means the first character must be a lowercase letter, and all following characters must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="port_nodejs">
<a href="#port_nodejs" style="color: inherit; text-decoration: inherit;">port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The TCP port number for the HTTP health check request. The default value is 80.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_nodejs">
<a href="#project_nodejs" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="requestid_nodejs">
<a href="#requestid_nodejs" style="color: inherit; text-decoration: inherit;">request<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="requestpath_nodejs">
<a href="#requestpath_nodejs" style="color: inherit; text-decoration: inherit;">request<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The request path of the HTTP health check request. The default value is /. This field does not support query parameters.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="timeoutsec_nodejs">
<a href="#timeoutsec_nodejs" style="color: inherit; text-decoration: inherit;">timeout<wbr>Sec</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}How long (in seconds) to wait before claiming failure. The default value is 5 seconds. It is invalid for timeoutSec to have greater value than checkIntervalSec.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="unhealthythreshold_nodejs">
<a href="#unhealthythreshold_nodejs" style="color: inherit; text-decoration: inherit;">unhealthy<wbr>Threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}A so-far healthy instance will be marked unhealthy after this many consecutive failures. The default value is 2.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="check_interval_sec_python">
<a href="#check_interval_sec_python" style="color: inherit; text-decoration: inherit;">check_<wbr>interval_<wbr>sec</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How often (in seconds) to send a health check. The default value is 5 seconds.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}An optional description of this resource. Provide this property when you create the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="healthy_threshold_python">
<a href="#healthy_threshold_python" style="color: inherit; text-decoration: inherit;">healthy_<wbr>threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}A so-far unhealthy instance will be marked healthy after this many consecutive successes. The default value is 2.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="host_python">
<a href="#host_python" style="color: inherit; text-decoration: inherit;">host</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The value of the host header in the HTTP health check request. If left empty (default value), the public IP on behalf of which this health check is performed will be used.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the resource. Provided by the client when the resource is created. The name must be 1-63 characters long, and comply with RFC1035. Specifically, the name must be 1-63 characters long and match the regular expression `[a-z]([-a-z0-9]*[a-z0-9])?` which means the first character must be a lowercase letter, and all following characters must be a dash, lowercase letter, or digit, except the last character, which cannot be a dash.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="port_python">
<a href="#port_python" style="color: inherit; text-decoration: inherit;">port</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The TCP port number for the HTTP health check request. The default value is 80.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_python">
<a href="#project_python" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="request_id_python">
<a href="#request_id_python" style="color: inherit; text-decoration: inherit;">request_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="request_path_python">
<a href="#request_path_python" style="color: inherit; text-decoration: inherit;">request_<wbr>path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The request path of the HTTP health check request. The default value is /. This field does not support query parameters.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="timeout_sec_python">
<a href="#timeout_sec_python" style="color: inherit; text-decoration: inherit;">timeout_<wbr>sec</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}How long (in seconds) to wait before claiming failure. The default value is 5 seconds. It is invalid for timeoutSec to have greater value than checkIntervalSec.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="unhealthy_threshold_python">
<a href="#unhealthy_threshold_python" style="color: inherit; text-decoration: inherit;">unhealthy_<wbr>threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}A so-far healthy instance will be marked unhealthy after this many consecutive failures. The default value is 2.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the HttpHealthCheck resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="creationtimestamp_csharp">
<a href="#creationtimestamp_csharp" style="color: inherit; text-decoration: inherit;">Creation<wbr>Timestamp</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Creation timestamp in RFC3339 text format.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="kind_csharp">
<a href="#kind_csharp" style="color: inherit; text-decoration: inherit;">Kind</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Type of the resource. Always compute#httpHealthCheck for HTTP health checks.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="selflink_csharp">
<a href="#selflink_csharp" style="color: inherit; text-decoration: inherit;">Self<wbr>Link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server-defined URL for the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="selflinkwithid_csharp">
<a href="#selflinkwithid_csharp" style="color: inherit; text-decoration: inherit;">Self<wbr>Link<wbr>With<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server-defined URL for this resource with the resource id.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="creationtimestamp_go">
<a href="#creationtimestamp_go" style="color: inherit; text-decoration: inherit;">Creation<wbr>Timestamp</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Creation timestamp in RFC3339 text format.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="kind_go">
<a href="#kind_go" style="color: inherit; text-decoration: inherit;">Kind</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Type of the resource. Always compute#httpHealthCheck for HTTP health checks.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="selflink_go">
<a href="#selflink_go" style="color: inherit; text-decoration: inherit;">Self<wbr>Link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server-defined URL for the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="selflinkwithid_go">
<a href="#selflinkwithid_go" style="color: inherit; text-decoration: inherit;">Self<wbr>Link<wbr>With<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server-defined URL for this resource with the resource id.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="creationtimestamp_nodejs">
<a href="#creationtimestamp_nodejs" style="color: inherit; text-decoration: inherit;">creation<wbr>Timestamp</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Creation timestamp in RFC3339 text format.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="kind_nodejs">
<a href="#kind_nodejs" style="color: inherit; text-decoration: inherit;">kind</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Type of the resource. Always compute#httpHealthCheck for HTTP health checks.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="selflink_nodejs">
<a href="#selflink_nodejs" style="color: inherit; text-decoration: inherit;">self<wbr>Link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server-defined URL for the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="selflinkwithid_nodejs">
<a href="#selflinkwithid_nodejs" style="color: inherit; text-decoration: inherit;">self<wbr>Link<wbr>With<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Server-defined URL for this resource with the resource id.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="creation_timestamp_python">
<a href="#creation_timestamp_python" style="color: inherit; text-decoration: inherit;">creation_<wbr>timestamp</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Creation timestamp in RFC3339 text format.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="kind_python">
<a href="#kind_python" style="color: inherit; text-decoration: inherit;">kind</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Type of the resource. Always compute#httpHealthCheck for HTTP health checks.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="self_link_python">
<a href="#self_link_python" style="color: inherit; text-decoration: inherit;">self_<wbr>link</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Server-defined URL for the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="self_link_with_id_python">
<a href="#self_link_with_id_python" style="color: inherit; text-decoration: inherit;">self_<wbr>link_<wbr>with_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Server-defined URL for this resource with the resource id.{{% /md %}}</dd></dl>
{{% /choosable %}}








<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-google-native">https://github.com/pulumi/pulumi-google-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
