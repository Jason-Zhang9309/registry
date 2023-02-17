
---
title: "getProject"
title_tag: "huaweicloud.Eps.getProject"
meta_desc: "Documentation for the huaweicloud.Eps.getProject function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to get an enterprise project from HuaweiCloud
## Resources Supported Currently

<!-- markdownlint-disable MD033 -->
Service Name | Resource Name | Sub Resource Name
---- | --- | ---
AS  | huaweicloud.As.Group |
BCS | huaweicloud.Bcs.Instance |
BMS | huaweicloud.Bms.Instance |
CBR | huaweicloud.Cbr.Vault |
CCE | huaweicloud.Cce.Cluster | huaweicloud_cce_node<br>huaweicloud_cce_node_pool<br>huaweicloud_cce_addon
CDM | huaweicloud.Cdm.Cluster |
CDN | huaweicloud.Cdn.Domain |
CES | huaweicloud.Cse.Alarmrule |
DCS | huaweicloud.Dcs.Instance |
DDS | huaweicloud.Dds.Instance |
DMS | huaweicloud_dms_kafka_instance<br>huaweicloud_dms_rabbitmq_instance |
DNS | huaweicloud_dns_ptrrecord<br>huaweicloud_dns_zone |
ECS | huaweicloud.Ecs.Instance |
EIP | huaweicloud_vpc_eip<br>huaweicloud_vpc_bandwidth |
ELB | huaweicloud.Elb.Loadbalancer |
Dedicated ELB | huaweicloud_elb_certificate<br>huaweicloud_elb_ipgroup<br>huaweicloud_elb_loadbalancer |
EVS | huaweicloud.Evs.Volume |
FGS | huaweicloud.FunctionGraph.Function |
GaussDB | huaweicloud_gaussdb_cassandra_instance<br>huaweicloud_gaussdb_mysql_instance<br>huaweicloud_gaussdb_opengauss_instance |
IMS | huaweicloud.Ims.Image |
KMS | huaweicloud.Dew.Key |
NAT | huaweicloud.Nat.Gateway | huaweicloud_nat_snat_rule<br>huaweicloud_nat_dnat_rule
OBS | huaweicloud.Obs.Bucket | huaweicloud_obs_bucket_object<br>huaweicloud_obs_bucket_policy
RDS | huaweicloud_rds_instance<br>huaweicloud_rds_read_replica_instance |
SFS | huaweicloud_sfs_file_system<br>huaweicloud_sfs_turbo | huaweicloud.Sfs.AccessRule
SMN | huaweicloud.Smn.Topic |
VPC | huaweicloud_vpc<br>huaweicloud_networking_secgroup | huaweicloud_vpc_subnet<br>huaweicloud_vpc_route<br>huaweicloud_networking_secgroup_rule
<!-- markdownlint-enable MD033 -->


<div><pulumi-examples>

## Example Usage

<div><pulumi-chooser type="language" options="typescript,python,go,csharp,java,yaml"></pulumi-chooser></div>





<div>
<pulumi-choosable type="language" values="csharp">

```csharp
using System.Collections.Generic;
using Pulumi;
using Huaweicloud = Pulumi.Huaweicloud;

return await Deployment.RunAsync(() => 
{
    var test = Huaweicloud.Eps.GetProject.Invoke(new()
    {
        Name = "test",
    });

});
```


</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="go">

```go
package main

import (
	"github.com/huaweicloud/pulumi-huaweicloud/sdk/go/huaweicloud/Eps"
	"github.com/pulumi/pulumi-huaweicloud/sdk/go/huaweicloud/Eps"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := Eps.GetProject(ctx, &eps.GetProjectArgs{
			Name: pulumi.StringRef("test"),
		}, nil)
		if err != nil {
			return err
		}
		return nil
	})
}
```


</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="java">

```java
package generated_program;

import com.pulumi.Context;
import com.pulumi.Pulumi;
import com.pulumi.core.Output;
import com.pulumi.huaweicloud.Eps.EpsFunctions;
import com.pulumi.huaweicloud.Eps.inputs.GetProjectArgs;
import java.util.List;
import java.util.ArrayList;
import java.util.Map;
import java.io.File;
import java.nio.file.Files;
import java.nio.file.Paths;

public class App {
    public static void main(String[] args) {
        Pulumi.run(App::stack);
    }

    public static void stack(Context ctx) {
        final var test = EpsFunctions.getProject(GetProjectArgs.builder()
            .name("test")
            .build());

    }
}
```


</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="python">

```python
import pulumi
import pulumi_huaweicloud as huaweicloud

test = huaweicloud.Eps.get_project(name="test")
```


</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="typescript">


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as huaweicloud from "@pulumi/huaweicloud";

const test = pulumi.output(huaweicloud.Eps.getProject({
    name: "test",
}));
```


</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="yaml">

```yaml
variables:
  test:
    Fn::Invoke:
      Function: huaweicloud:Eps:getProject
      Arguments:
        name: test
```


</pulumi-choosable>
</div>





</pulumi-examples></div>




## Using getProject {#using}

Two invocation forms are available. The direct form accepts plain
arguments and either blocks until the result value is available, or
returns a Promise-wrapped result. The output form accepts
Input-wrapped arguments and returns an Output-wrapped result.

<div>
<pulumi-chooser type="language" options="typescript,python,go,csharp,java,yaml"></pulumi-chooser>
</div>


<div>
<pulumi-choosable type="language" values="javascript,typescript">
<div class="highlight"
><pre class="chroma"><code class="language-typescript" data-lang="typescript"
><span class="k">function </span>getProject<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetProjectArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetProjectResult</a></span>></span
><span class="k">
function </span>getProjectOutput<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetProjectOutputArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Output&lt;<span class="nx"><a href="#result">GetProjectResult</a></span>></span
></code></pre></div>
</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="python">
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"
><span class="k">def </span>get_project<span class="p">(</span><span class="nx">id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                <span class="nx">status</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> <span>GetProjectResult</span
><span class="k">
def </span>get_project_output<span class="p">(</span><span class="nx">id</span><span class="p">:</span> <span class="nx">Optional[pulumi.Input[str]]</span> = None<span class="p">,</span>
                <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[pulumi.Input[str]]</span> = None<span class="p">,</span>
                <span class="nx">status</span><span class="p">:</span> <span class="nx">Optional[pulumi.Input[int]]</span> = None<span class="p">,</span>
                <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> <span>Output[GetProjectResult]</span
></code></pre></div>
</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="go">
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"
><span class="k">func </span>GetProject<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetProjectArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetProjectResult</a></span>, error)</span
><span class="k">
func </span>GetProjectOutput<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetProjectOutputArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) GetProjectResultOutput</span
></code></pre></div>

&gt; Note: This function is named `GetProject` in the Go SDK.

</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="csharp">
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetProject </span><span class="p">
{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetProjectResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetProjectArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="k">
    public static </span>Output&lt;<span class="nx"><a href="#result">GetProjectResult</a></span>> <span class="p">Invoke(</span><span class="nx">GetProjectInvokeArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="java">
<div class="highlight"><pre class="chroma"><code class="language-java" data-lang="java"><span class="k">public static CompletableFuture&lt;<span class="nx"><a href="#result">GetProjectResult</a></span>> </span>getProject<span class="p">(</span><span class="nx">GetProjectArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx">InvokeOptions</span><span class="p"> </span><span class="nx">options<span class="p">)</span>
<span class="c">// Output-based functions aren't available in Java yet</span>
</code></pre></div>
</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="yaml">
<div class="highlight"><pre class="chroma"><code class="language-yaml" data-lang="yaml"><span class="k">Fn::Invoke:</span>
<span class="k">&nbsp;&nbsp;Function:</span> huaweicloud:Eps/getProject:getProject
<span class="k">&nbsp;&nbsp;Arguments:</span>
<span class="c">&nbsp;&nbsp;&nbsp;&nbsp;# Arguments dictionary</span></code></pre></div>
</pulumi-choosable>
</div>



The following arguments are supported:


<div>
<pulumi-choosable type="language" values="csharp">
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="id_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the ID of an enterprise project. The value 0 indicates enterprise project default.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the enterprise project name. Fuzzy search is supported.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="status_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_csharp" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd><p>Specifies the status of an enterprise project.</p>
<ul>
<li>1 indicates Enabled.</li>
<li>2 indicates Disabled.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="go">
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="id_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the ID of an enterprise project. The value 0 indicates enterprise project default.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the enterprise project name. Fuzzy search is supported.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="status_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_go" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd><p>Specifies the status of an enterprise project.</p>
<ul>
<li>1 indicates Enabled.</li>
<li>2 indicates Disabled.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="java">
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="id_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_java" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Specifies the ID of an enterprise project. The value 0 indicates enterprise project default.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="name_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_java" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Specifies the enterprise project name. Fuzzy search is supported.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="status_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_java" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Integer</span>
    </dt>
    <dd><p>Specifies the status of an enterprise project.</p>
<ul>
<li>1 indicates Enabled.</li>
<li>2 indicates Disabled.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="javascript,typescript">
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="id_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the ID of an enterprise project. The value 0 indicates enterprise project default.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the enterprise project name. Fuzzy search is supported.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="status_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_nodejs" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd><p>Specifies the status of an enterprise project.</p>
<ul>
<li>1 indicates Enabled.</li>
<li>2 indicates Disabled.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="python">
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="id_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>Specifies the ID of an enterprise project. The value 0 indicates enterprise project default.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>Specifies the enterprise project name. Fuzzy search is supported.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="status_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_python" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd><p>Specifies the status of an enterprise project.</p>
<ul>
<li>1 indicates Enabled.</li>
<li>2 indicates Disabled.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="yaml">
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="id_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_yaml" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Specifies the ID of an enterprise project. The value 0 indicates enterprise project default.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="name_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_yaml" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Specifies the enterprise project name. Fuzzy search is supported.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="status_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_yaml" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Number</span>
    </dt>
    <dd><p>Specifies the status of an enterprise project.</p>
<ul>
<li>1 indicates Enabled.</li>
<li>2 indicates Disabled.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>




## getProject Result {#result}

The following output properties are available:



<div>
<pulumi-choosable type="language" values="csharp">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#createdat_csharp" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was created. Example: 2018-05-18T06:49:06Z</p>
</dd><dt class="property-"
            title="">
        <span id="description_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Provides supplementary information about the enterprise project.</p>
</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="status_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_csharp" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="updatedat_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#updatedat_csharp" style="color: inherit; text-decoration: inherit;">Updated<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was modified. Example: 2018-05-28T02:21:36Z</p>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="go">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#createdat_go" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was created. Example: 2018-05-18T06:49:06Z</p>
</dd><dt class="property-"
            title="">
        <span id="description_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Provides supplementary information about the enterprise project.</p>
</dd><dt class="property-"
            title="">
        <span id="id_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="name_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="status_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_go" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="updatedat_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#updatedat_go" style="color: inherit; text-decoration: inherit;">Updated<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was modified. Example: 2018-05-28T02:21:36Z</p>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="java">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#createdat_java" style="color: inherit; text-decoration: inherit;">created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was created. Example: 2018-05-18T06:49:06Z</p>
</dd><dt class="property-"
            title="">
        <span id="description_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_java" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Provides supplementary information about the enterprise project.</p>
</dd><dt class="property-"
            title="">
        <span id="id_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_java" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="name_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_java" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="status_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_java" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Integer</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="updatedat_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#updatedat_java" style="color: inherit; text-decoration: inherit;">updated<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was modified. Example: 2018-05-28T02:21:36Z</p>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="javascript,typescript">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#createdat_nodejs" style="color: inherit; text-decoration: inherit;">created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was created. Example: 2018-05-18T06:49:06Z</p>
</dd><dt class="property-"
            title="">
        <span id="description_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Provides supplementary information about the enterprise project.</p>
</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="status_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_nodejs" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="updatedat_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#updatedat_nodejs" style="color: inherit; text-decoration: inherit;">updated<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was modified. Example: 2018-05-28T02:21:36Z</p>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="python">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="created_at_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#created_at_python" style="color: inherit; text-decoration: inherit;">created_<wbr>at</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was created. Example: 2018-05-18T06:49:06Z</p>
</dd><dt class="property-"
            title="">
        <span id="description_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>Provides supplementary information about the enterprise project.</p>
</dd><dt class="property-"
            title="">
        <span id="id_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="name_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="status_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_python" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="updated_at_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#updated_at_python" style="color: inherit; text-decoration: inherit;">updated_<wbr>at</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was modified. Example: 2018-05-28T02:21:36Z</p>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="yaml">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#createdat_yaml" style="color: inherit; text-decoration: inherit;">created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was created. Example: 2018-05-18T06:49:06Z</p>
</dd><dt class="property-"
            title="">
        <span id="description_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_yaml" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Provides supplementary information about the enterprise project.</p>
</dd><dt class="property-"
            title="">
        <span id="id_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_yaml" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="name_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_yaml" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="status_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#status_yaml" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Number</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="updatedat_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#updatedat_yaml" style="color: inherit; text-decoration: inherit;">updated<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Specifies the time (UTC) when the enterprise project was modified. Example: 2018-05-28T02:21:36Z</p>
</dd></dl>
</pulumi-choosable>
</div>





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/huaweicloud/pulumi-huaweicloud">https://github.com/huaweicloud/pulumi-huaweicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd><p>This Pulumi package is based on the <a href="https://github.com/huaweicloud/terraform-provider-huaweicloud"><code>huaweicloud</code> Terraform Provider</a>.</p>
</dd>
</dl>
