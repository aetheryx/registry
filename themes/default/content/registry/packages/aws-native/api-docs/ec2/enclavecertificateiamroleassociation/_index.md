
---
title: "EnclaveCertificateIamRoleAssociation"
title_tag: "aws-native.ec2.EnclaveCertificateIamRoleAssociation"
meta_desc: "Documentation for the aws-native.ec2.EnclaveCertificateIamRoleAssociation resource with examples, input properties, output properties, lookup functions, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Associates an AWS Identity and Access Management (IAM) role with an AWS Certificate Manager (ACM) certificate. This association is based on Amazon Resource Names and it enables the certificate to be used by the ACM for Nitro Enclaves application inside an enclave.


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
        var myEnclaveCertificateIamRoleAssociation = new AwsNative.EC2.EnclaveCertificateIamRoleAssociation("myEnclaveCertificateIamRoleAssociation", new AwsNative.EC2.EnclaveCertificateIamRoleAssociationArgs
        {
            CertificateArn = "arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE",
            RoleArn = "arn:aws:iam::123456789012:role/my-acm-role",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/ec2"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := ec2.NewEnclaveCertificateIamRoleAssociation(ctx, "myEnclaveCertificateIamRoleAssociation", &ec2.EnclaveCertificateIamRoleAssociationArgs{
			CertificateArn: pulumi.String("arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE"),
			RoleArn:        pulumi.String("arn:aws:iam::123456789012:role/my-acm-role"),
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

my_enclave_certificate_iam_role_association = aws_native.ec2.EnclaveCertificateIamRoleAssociation("myEnclaveCertificateIamRoleAssociation",
    certificate_arn="arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE",
    role_arn="arn:aws:iam::123456789012:role/my-acm-role")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myEnclaveCertificateIamRoleAssociation = new aws_native.ec2.EnclaveCertificateIamRoleAssociation("myEnclaveCertificateIamRoleAssociation", {
    certificateArn: "arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE",
    roleArn: "arn:aws:iam::123456789012:role/my-acm-role",
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
        var myCertAssociation = new AwsNative.EC2.EnclaveCertificateIamRoleAssociation("myCertAssociation", new AwsNative.EC2.EnclaveCertificateIamRoleAssociationArgs
        {
            CertificateArn = "arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE",
            RoleArn = "arn:aws:iam::123456789012:role/my-acm-role",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/ec2"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := ec2.NewEnclaveCertificateIamRoleAssociation(ctx, "myCertAssociation", &ec2.EnclaveCertificateIamRoleAssociationArgs{
			CertificateArn: pulumi.String("arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE"),
			RoleArn:        pulumi.String("arn:aws:iam::123456789012:role/my-acm-role"),
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

my_cert_association = aws_native.ec2.EnclaveCertificateIamRoleAssociation("myCertAssociation",
    certificate_arn="arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE",
    role_arn="arn:aws:iam::123456789012:role/my-acm-role")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myCertAssociation = new aws_native.ec2.EnclaveCertificateIamRoleAssociation("myCertAssociation", {
    certificateArn: "arn:aws:acm:us-east-1:123456789012:certificate/123abcde-cdef-abcd-1234-123abEXAMPLE",
    roleArn: "arn:aws:iam::123456789012:role/my-acm-role",
});

```


{{< /example >}}





{{% /examples %}}




## Create a EnclaveCertificateIamRoleAssociation Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">EnclaveCertificateIamRoleAssociation</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">EnclaveCertificateIamRoleAssociationArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">EnclaveCertificateIamRoleAssociation</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                                         <span class="nx">certificate_arn</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                         <span class="nx">role_arn</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">EnclaveCertificateIamRoleAssociation</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                         <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">EnclaveCertificateIamRoleAssociationArgs</a></span><span class="p">,</span>
                                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewEnclaveCertificateIamRoleAssociation</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">EnclaveCertificateIamRoleAssociationArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">EnclaveCertificateIamRoleAssociation</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">EnclaveCertificateIamRoleAssociation</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">EnclaveCertificateIamRoleAssociationArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">EnclaveCertificateIamRoleAssociationArgs</a></span>
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
        <span class="property-type"><a href="#inputs">EnclaveCertificateIamRoleAssociationArgs</a></span>
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
        <span class="property-type"><a href="#inputs">EnclaveCertificateIamRoleAssociationArgs</a></span>
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
        <span class="property-type"><a href="#inputs">EnclaveCertificateIamRoleAssociationArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## EnclaveCertificateIamRoleAssociation Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The EnclaveCertificateIamRoleAssociation resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="certificatearn_csharp">
<a href="#certificatearn_csharp" style="color: inherit; text-decoration: inherit;">Certificate<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the ACM certificate with which to associate the IAM role.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rolearn_csharp">
<a href="#rolearn_csharp" style="color: inherit; text-decoration: inherit;">Role<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the IAM role to associate with the ACM certificate. You can associate up to 16 IAM roles with an ACM certificate.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="certificatearn_go">
<a href="#certificatearn_go" style="color: inherit; text-decoration: inherit;">Certificate<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the ACM certificate with which to associate the IAM role.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rolearn_go">
<a href="#rolearn_go" style="color: inherit; text-decoration: inherit;">Role<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the IAM role to associate with the ACM certificate. You can associate up to 16 IAM roles with an ACM certificate.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="certificatearn_nodejs">
<a href="#certificatearn_nodejs" style="color: inherit; text-decoration: inherit;">certificate<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the ACM certificate with which to associate the IAM role.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rolearn_nodejs">
<a href="#rolearn_nodejs" style="color: inherit; text-decoration: inherit;">role<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the IAM role to associate with the ACM certificate. You can associate up to 16 IAM roles with an ACM certificate.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="certificate_arn_python">
<a href="#certificate_arn_python" style="color: inherit; text-decoration: inherit;">certificate_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the ACM certificate with which to associate the IAM role.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="role_arn_python">
<a href="#role_arn_python" style="color: inherit; text-decoration: inherit;">role_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the IAM role to associate with the ACM certificate. You can associate up to 16 IAM roles with an ACM certificate.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the EnclaveCertificateIamRoleAssociation resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="certificates3bucketname_csharp">
<a href="#certificates3bucketname_csharp" style="color: inherit; text-decoration: inherit;">Certificate<wbr>S3Bucket<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Amazon S3 bucket to which the certificate was uploaded.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="certificates3objectkey_csharp">
<a href="#certificates3objectkey_csharp" style="color: inherit; text-decoration: inherit;">Certificate<wbr>S3Object<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon S3 object key where the certificate, certificate chain, and encrypted private key bundle are stored.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encryptionkmskeyid_csharp">
<a href="#encryptionkmskeyid_csharp" style="color: inherit; text-decoration: inherit;">Encryption<wbr>Kms<wbr>Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the AWS KMS CMK used to encrypt the private key of the certificate.{{% /md %}}</dd><dt class="property-"
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
        <span id="certificates3bucketname_go">
<a href="#certificates3bucketname_go" style="color: inherit; text-decoration: inherit;">Certificate<wbr>S3Bucket<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Amazon S3 bucket to which the certificate was uploaded.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="certificates3objectkey_go">
<a href="#certificates3objectkey_go" style="color: inherit; text-decoration: inherit;">Certificate<wbr>S3Object<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon S3 object key where the certificate, certificate chain, and encrypted private key bundle are stored.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encryptionkmskeyid_go">
<a href="#encryptionkmskeyid_go" style="color: inherit; text-decoration: inherit;">Encryption<wbr>Kms<wbr>Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the AWS KMS CMK used to encrypt the private key of the certificate.{{% /md %}}</dd><dt class="property-"
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
        <span id="certificates3bucketname_nodejs">
<a href="#certificates3bucketname_nodejs" style="color: inherit; text-decoration: inherit;">certificate<wbr>S3Bucket<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Amazon S3 bucket to which the certificate was uploaded.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="certificates3objectkey_nodejs">
<a href="#certificates3objectkey_nodejs" style="color: inherit; text-decoration: inherit;">certificate<wbr>S3Object<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon S3 object key where the certificate, certificate chain, and encrypted private key bundle are stored.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encryptionkmskeyid_nodejs">
<a href="#encryptionkmskeyid_nodejs" style="color: inherit; text-decoration: inherit;">encryption<wbr>Kms<wbr>Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the AWS KMS CMK used to encrypt the private key of the certificate.{{% /md %}}</dd><dt class="property-"
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
        <span id="certificate_s3_bucket_name_python">
<a href="#certificate_s3_bucket_name_python" style="color: inherit; text-decoration: inherit;">certificate_<wbr>s3_<wbr>bucket_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Amazon S3 bucket to which the certificate was uploaded.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="certificate_s3_object_key_python">
<a href="#certificate_s3_object_key_python" style="color: inherit; text-decoration: inherit;">certificate_<wbr>s3_<wbr>object_<wbr>key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon S3 object key where the certificate, certificate chain, and encrypted private key bundle are stored.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encryption_kms_key_id_python">
<a href="#encryption_kms_key_id_python" style="color: inherit; text-decoration: inherit;">encryption_<wbr>kms_<wbr>key_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the AWS KMS CMK used to encrypt the private key of the certificate.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}








<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws-native">https://github.com/pulumi/pulumi-aws-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
