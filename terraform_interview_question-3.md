# Top 250 Questions and Answers For Terraform Associate Certification - 3
---

 We have consolidated a list of frequently asked questions in Terraform AssociateCertification. Same list consists of frequently asked Terraform interview questions. This will help DevOps Engineers in their preparations for Interview.
  You will find these questions very helpful in your DevOps interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

{!inpage-ads.md!}

---

179. What are Backends?

        A "backend" in Terraform determines how state is loaded and how an operation such as apply is executed. 
        This abstraction enables non-local file state storage, remote execution, etc. By default, Terraform uses
        the "local" backend, which is the normal behavior of Terraform.

180. What is local Backend?

        The local backend stores state on the local filesystem, locks that state using system APIs, and performs
        operations locally.

        // Example
          terraform {
            backend "local" {
              path = "relative/path/to/terraform.tfstate"
            }
          }

181. What is the default path for the local backend?

        This defaults to "terraform.tfstate" relative to the root module by default.

182. What is State Locking?

        If supported by your backend, Terraform will lock your state for all operations that could write state.
        This prevents others from acquiring the lock and potentially corrupting your state. State locking happens
        automatically on all operations that could write state. You will not see any message that it is happening.
        If state locking fails, Terraform will not continue.

183. Does Terraform continue if state locking fails?

        No.

        If state locking fails, Terraform will not continue.

184. Can you disable state locking?

        Yes.

        You can disable state locking for most commands with the -lock flag but it is not recommended.

185. What are the types of Backend?

        Standard: State management, functionality covered in State Storage & Locking.

        Enhanced: Everything in standard plus remote operations.

186. What are remote Backends?

        Remote backends allow Terraform to use a shared storage space for state data, so any member of your team
        can use Terraform to manage the same infrastructure.

187. What is the benefit of using remote backend?

        Remote state storage makes collaboration easier and keeps state and secret information off your local disk.
        Remote state is loaded only in memory when it is used.

188. If you want to switch from using remote backend to local backend. Whatshould you do?

        If you want to move back to local state, you can remove the backend configuration block from your
        configuration and run terraform init again.
        Terraform will once again ask if you want to migrate your state back to local.

189. What does the command refresh do?

        The "terraform refresh" command is used to reconcile the state Terraform knows about (via its state file)
        with the real-world infrastructure. This can be used to detect any drift from the last-known state, and to
        update the state file.

190. Does the command refresh modify the infrastructure?

        The command "refresh" does not modify infrastructure, but does modify the state file.
        If the state is changed, this may cause changes to occur during the next plan or apply.

191. How do you backup the state to the remote backend?

        1. When configuring a backend for the first time (moving from no defined backend to explicitly configuring
           one), Terraform will give you the option to migrate your state to the new backend. This lets you adopt
           backends without losing any existing state.

        2. To be extra careful, we always recommend manually backing up your state as well. You can do this by
           simply copying your "terraform.tfstate" file to another location.

192. What is a partial configuration in terms of configuring Backends?

        You do not need to specify every required argument in the backend configuration. Omitting certain arguments
        may be desirable to avoid storing secrets, such as access keys, within the main configuration. When some or
        all of the arguments are omitted, we call this a partial configuration.

193. What are the ways to provide remaining arguments when using partialconfiguration?

        Interactively: Terraform will interactively ask you for the required values, unless interactive input is 
                       disabled. Terraform will not prompt for optional values.

        File: A configuration file may be specified via the init command line. To specify a file, use the 
              -backend-config=PATH option when running terraform init. If the file contains secrets it may be kept
              in a secure data store, such as Vault, in which case it must be downloaded to the local disk before
              running Terraform.

        Command-line key-value pairs: Key/value pairs can be specified via the init command line. Note that many
                      shells retain command-line flags in a history file, so this isn't recommended for secrets.
                      To specify a single key/value pair, use the -backend-config="KEY=VALUE" option when running
                      terraform init.

      Ref: <a target="_blank" href=https://www.terraform.io/docs/backends/config.html>https://www.terraform.io/docs/backends/config.html</a>

194. What is the basic requirement when using partial configuration?

        When using partial configuration, Terraform requires at a minimum that an empty backend configuration is
        specified in one of the root Terraform configuration files, to specify the backend type.

        // Example

          terraform {
            backend "consul" {}
          }

195. Give an example of passing partial configuration with Command-lineKey/Value pairs?

        terraform init \
          -backend-config="address=demo.consul.io" \
          -backend-config="path=example_app/terraform_state" \
          -backend-config="scheme=https"

196. How to unconfigure a backend?

        If you no longer want to use any backend, you can simply remove the configuration from the file. Terraform
        will detect this like any other change and prompt you to reinitialize.
        As part of the reinitialization, Terraform will ask if you would like to migrate your state back down to
        normal local state. Once this is complete then Terraform is back to behaving as it does by default.

197. How do you encrypt sensitive data in the state?

        Terraform Cloud always encrypts state at rest and protects it with TLS in transit. Terraform Cloud also
        knows the identity of the user requesting state and maintains a history of state changes. This can be used
        to control access and track activity. Terraform Enterprise also supports detailed audit logging.
        The S3 backend supports encryption at rest when the encrypt option is enabled. IAM policies and logging
        can be used to identify any invalid access. Requests for the state go over a TLS connection.

198. Backends are completely optional. Is this true?

        Backends are completely optional. You can successfully use Terraform without ever having to learn or use
        backends. However, they do solve pain points that afflict teams at a certain scale. If you are an individual,
        you can likely get away with never using backends.

199. What are the benefits of Backends?

        Working in a team: Backends can store their state remotely and protect that state with locks to prevent
                corruption. Some backends such as Terraform Cloud even automatically store a history of all state
                revisions.

        Keeping sensitive information off disk: State is retrieved from backends on demand and only stored in memory.
                If you are using a backend such as Amazon S3, the only location the state ever is persisted is in S3.

        Remote operations: For larger infrastructures or certain changes, terraform apply can take a long, long time.
                Some backends support remote operations which enable the operation to execute remotely. You can then
                turn off your computer and your operation will still complete. Paired with remote state storage and
                locking above, this also helps in team environments.

200. Why should you be very careful with the Force unlocking the state?

        Terraform has a "force-unlock" command to manually unlock the state if unlocking failed.

        Be very careful with this command. If you unlock the state when someone else is holding the lock it could
        cause multiple writers. Force unlock should only be used to unlock your own lock in the situation where
        automatic unlocking failed.

        To protect you, the "force-unlock" command requires a unique lock ID. Terraform will output this lock ID
        if unlocking fails. This lock ID acts as a nonce , ensuring that locks and unlocks target the correct lock.

201. You should only use force unlock command when automatic unlocking fails. Isthis true?

        True
          
202. How do you define a variable?

        variable "region" {
          default = "us-east-1"
        }

        This defines the region variable within your Terraform configuration.

203. How do you access the variable in the configuration?

        // accessing a variable
          provider "aws" {
            region = var.region
          }

204. How many ways you can assign variables in the configuration?

        1. Command-line flags:
            terraform apply -var 'region=us-east-1'

        2. From a file:
            To persist variable values, create a file and assign variables within this file. Create a file named
            terraform.tfvars with the following contents:
              
            region = "us-east-1"

            terraform apply \
              -var-file="secret.tfvars" \
              -var-file="production.tfvars"

        3. From environment varibles:
            Terraform will read environment variables in the form of "TF_VAR_name" to find the value for a variable.
            For example, the "TF_VAR_region" variable can be set in the shell to set the region variable in Terraform.

        4. UI input:
            If you execute "terraform apply" with any variable unspecified, Terraform will ask you to input the 
            values interactively. These values are not saved, but this provides a convenient workflow when getting
            started with Terraform. UI input is not recommended for everyday use of Terraform.

205. Does environment variables support List and map types?

        No

        Environment variables can only populate string-type variables. List and map type variables must be
        populated via one of the other mechanisms.

206. How do you provision infrastructure in a staging environment or a productionenvironment using the same Terraform configuration?

        You can use different varible files with the same configuration

        // Example

        // For development
          terraform apply -var-file="dev.tfvars"

        // For test
          terraform apply -var-file="test.tfvars"

207. How do you assign default values to variables?

        If no value is assigned to a variable via any of these methods and the variable has a default key in its
        declaration, that value will be used for the variable.

        variable "region" {
            default = "us-east-1"
        }

208. What are the data types for the variables?

        string
        number
        boolian
        list(<TYPE>)
        set(<TYPE>)
        map(<TYPE>)
        object({<ATTR NAME> = <TYPE>, ... })
        tuple([<TYPE>, ...])

209. Give an example of data type List variables?

        Lists are defined either explicitly or implicitly.

        variable "availability_zone_names" {
          type = list(string)
          default = ["us-west-1a"]
        }

210. Give an example of data type Map variables?

        variable "region" {}
        variable "amis" {
          type = map(string)
        }

        amis = {
          "us-east-1" = "ami-abc123"
          "us-west-2" = "ami-def456"
        }

        // accessing
          resource "aws_instance" "example" {
              ami = var.amis[var.region]
              instance_type = "t2.micro"
          }

211. What is the Variable Definition Precedence?

        The above mechanisms for setting variables can be used together in any combination. If the same variable is
        assigned multiple values, Terraform uses the last value it finds, overriding any previous values. Note that
        the same variable cannot be assigned multiple values within a single source.

        Terraform loads variables in the following order, with later sources taking precedence over earlier ones:

        * Environment variables
        * The terraform.tfvars file, if present.
        * The terraform.tfvars.json file, if present.
        * Any "*.auto.tfvars" or "*.auto.tfvars.json" files, processed in lexical order of their filenames.
        * Any -var and -var-file options on the command line, in the order they are provided. (This includes
          variables set by a Terraform Cloud workspace.)

212. What are the output variables?

        output variables as a way to organize data to be easily queried and shown back to the Terraform user.
        Outputs are a way to tell Terraform what data is important. This data is outputted when apply is called,
        and can be queried using the terraform output command.

213. Hoe do you define an output variable?

        output "ip" {
          value = aws_eip.ip.public_ip
        }

        Multiple output blocks can be defined to specify multiple output variables.

214. How do you view outputs and queries them?

        You will see the output when you run the command "terraform apply"
        You can query the output with the command "terraform output ip"

215. What are the dynamic blocks?

        Some resource types include repeatable nested blocks in their arguments, which do not accept expressions.
        You can dynamically construct repeatable nested blocks like setting using a special dynamic block type,
        which is supported inside resource, data, provider, and provisioner blocks.

        A dynamic block acts much like a for expression, but produces nested blocks instead of a complex typed
        value. It iterates over a given complex value, and generates a nested block for each element of that 
        complex value.

        Example using dynamic blocks:

        resource "aws_elastic_beanstalk_environment" "tfenvtest" {
          name = "tf-test-name"
          application = "${aws_elastic_beanstalk_application.tftest.name}"
          solution_stack_name = "64bit Amazon Linux 2018.03 v2.11.4 running Go 1.12.6"

          dynamic "setting" {
           for_each = var.settings
           content {
             namespace = setting.value["namespace"]
             name = setting.value["name"]
             value = setting.value["value"]
           }
         }
        }
      Ref: <a target="_blank" href=https://www.terraform.io/docs/configuration/expressions.html#dynamic-blocks>https://www.terraform.io/docs/configuration/expressions.html#dynamic-blocks</a>

216. What are the best practices for dynamic blocks?

        Overuse of dynamic blocks can make configuration hard to read and maintain, so we recommend using them only
        when you need to hide details in order to build a clean user interface for a re-usable module. Always write
        nested blocks out literally where possible.

217. What are the Built-in Functions?

        The Terraform language includes a number of built-in functions that you can call from within expressions to
        transform and combine values.

          max(5, 12, 9)

218. Does Terraform language support user-defined functions?

        No

        The Terraform language does not support user-defined functions, and so only the functions built in to the
        language are available for use.

219. What is the built-in function to change string to a number?

        parseint parses the given string as a representation of an integer in the specified base and returns the
        resulting number. The base must be between 2 and 62 inclusive.

        > parseint("100", 10)
          100

      More Number Functions are listed here <a target="_blank" href=https://www.terraform.io/docs/configuration/functions/abs.html>https://www.terraform.io/docs/configuration/functions/abs.html</a>

220. What is the built-in function to evaluates given expression and returns aboolean whether the expression produced a result without any errors?

        can

        condition = can(formatdate("", var.timestamp))

      Ref: <a target="_blank" href=https://www.terraform.io/docs/configuration/functions/can.html>https://www.terraform.io/docs/configuration/functions/can.html</a>

221. What is the built-in function to evaluates all of its argument expressions inturn and returns the result of the first one that does not produce any errors?

        try

        locals {
          example = try(
            [tostring(var.example)],
            tolist(var.example),
            )
        }

222. What is Resource Address?

        A Resource Address is a string that references a specific resource in a larger infrastructure. An address is
        made up of two parts:

        [module path][resource spec]

223. What is the Module path?

        A module path addresses a module within the tree of modules. It takes the form:

        module.A.module.B.module.C...

        Multiple modules in a path indicate nesting. If a module path is specified without a resource spec, the address
        applies to every resource within the module. If the module path is omitted, this addresses the root module.

224. What is the Resource spec?

        A resource spec addresses a specific resource in the config. It takes the form:

        resource_type.resource_name[resource index]

        * resource_type - Type of the resource being addressed.
        * resource_name - User-defined name of the resource.
        * [resource index] - an optional index into a resource with multiple instances, surrounded by square brace
          characters ([ and ]).

        // Examples
          resource "aws_instance" "web" {
            # ...
            count = 4
          }

          aws_instance.web[3]  // Refers to only last instance
          aws_instance.web     // Refers to all four "web" instances.

          resource "aws_instance" "web" {
            # ...
            for_each = {
              "terraform": "value1",
              "resource": "value2",
              "indexing": "value3",
              "example": "value4",
            }
          }

          aws_instance.web["example"] //Refers to only the "example" instance in the config.

225. What are complex types and what are the collection types Terraform supports?

        A complex type is a type that groups multiple values into a single value.

        There are two categories of complex types:
          1. collection types (for grouping similar values)

            * list(...): a sequence of values identified by consecutive whole numbers starting with zero.
            * map(...): a collection of values where each is identified by a string label.
            * set(...): a collection of unique values that do not have any secondary identifiers or ordering.

          2. structural types (for grouping potentially dissimilar values).

            * object(...): a collection of named attributes that each have their own type.
            * tuple(...): a sequence of elements identified by consecutive whole numbers starting with zero, where
              each element has its own type.

226. What are the named values available and how do we refer to?

        Terraform makes several kinds of named values available. Each of these names is an expression that references
        the associated value; you can use them as standalone expressions, or combine them with other expressions to
        compute new values.

          * <RESOURCE TYPE>.<NAME> is an object representing a managed resource of the given type and name.
            The attributes of the resource can be accessed using dot or square bracket notation.

          * var.<NAME> is the value of the input variable of the given name.

          * local.<NAME> is the value of the local value of the given name.

          * module.<MODULE NAME>.<OUTPUT NAME> is the value of the specified output value from a child module called
            by the current module.

          * data.<DATA TYPE>.<NAME> is an object representing a data resource of the given data source type and name.
            If the resource has the count argument set, the value is a list of objects representing its instances.
            If the resource has the for_each argument set, the value is a map of objects representing its instances.

          * path.module is the filesystem path of the module where the expression is placed.

          * path.root is the filesystem path of the root module of the configuration.

          * path.cwd is the filesystem path of the current working directory. In normal use of Terraform this is
            the same as path.root, but some advanced uses of Terraform run it from a directory other than the root
            module directory, causing these paths to be different.

          * terraform.workspace is the name of the currently selected workspace.

227. What is the built-in function that reads the contents of a file at the given pathand returns them as a base64-encoded string?

        filebase64(path)
      Ref: <a target="_blank" href=https://www.terraform.io/docs/configuration/functions/filebase64.html>https://www.terraform.io/docs/configuration/functions/filebase64.html</a>

228. What is the built-in function that converts a timestamp into a different timeformat?

        formatdate(spec, timestamp)
      Ref: <a target="_blank" href=https://www.terraform.io/docs/configuration/functions/formatdate.html>https://www.terraform.io/docs/configuration/functions/formatdate.html</a>

229. What is the built-in function encodes a given value to a string using JSONsyntax?

        jsonencode({"hello"="world"})
      Ref: <a target="_blank" href=https://www.terraform.io/docs/configuration/functions/jsonencode.html>https://www.terraform.io/docs/configuration/functions/jsonencode.html</a>

230. What is the built-in function that calculates a full host IP address for a givenhost number within a given IP network address prefix?

        > cidrhost("10.12.127.0/20", 16)
          10.12.112.16

      Ref: <a target="_blank" href=https://www.terraform.io/docs/configuration/functions/cidrhost.html>href=https://www.terraform.io/docs/configuration/functions/cidrhost.html</a>

231. What is Sentinel?

        Sentinel is an embedded policy-as-code framework integrated with the HashiCorp Enterprise products. It
        enables fine-grained, logic-based policy decisions, and can be extended to use information from external
        sources.

232. What is the benefit of Sentinel?

        Codifying policy removes the need for ticketing queues, without sacrificing enforcement.
        One of the other benefits of Sentinel is that it also has a full testing framework.
        Avoiding a ticketing workflow allows organizations to provide more self-service capabilities and end-to-end
        automation, minimizing the friction for developers and operators.

      Ref: <a target="_blank" href=https://www.hashicorp.com/blog/why-policy-as-code/>https://www.hashicorp.com/blog/why-policy-as-code</a>

233. What is the Private Module Registry?

        Terraform Cloud's private module registry helps you share Terraform modules across your organization. It
        includes support for module versioning, a searchable and filterable list of available modules, and a
        configuration designer to help you build new workspaces faster.

234. What is the difference between public and private module registries whendefined source?

        The public registry uses a three-part <NAMESPACE>/<MODULE NAME>/<PROVIDER> format.
        The private modules use a four-part <HOSTNAME>/<ORGANIZATION>/<MODULE NAME>/<PROVIDER> format.

        // example

          module "vpc" {
            source = "app.terraform.io/example_corp/vpc/aws"
            version = "1.0.4"
          }

235. Where is the Terraform Module Registry available at?

        https://registry.terraform.io/

236. What is a workspace?

        A workspace contains everything Terraform needs to manage a given collection of infrastructure, and separate
        workspaces function like completely separate working directories.

237. What are the benefits of workspaces?

        https://www.hashicorp.com/resources/terraform-enterprise-understanding-workspaces-and-modules/

238. You are configuring a remote backend in the terraform cloud. You didn’t createan organization before you do terraform init. Does it work?

        While the organization defined in the backend stanza must already exist.

239. You are configuring a remote backend in the terraform cloud. You didn’t create a workspace before you do terraform init. Does it work?

        Terraform Cloud will create it if necessary. If you opt to use a workspace that already exists, the workspace
        must not have any existing states.

240. Terraform workspaces when you are working with CLI and Terraformworkspaces in the Terraform cloud. Is this correct?

        If you are familiar with running Terraform using the CLI, you may have used Terraform workspaces. Terraform
        Cloud workspaces behave differently than Terraform CLI workspaces. Terraform CLI workspaces allow multiple
        state files to exist within a single directory, enabling you to use one configuration for multiple
        environments. Terraform Cloud workspaces contain everything needed to manage a given set of infrastructure,
        and function like separate working directories.

241. How do you authenticate the CLI with the terraform cloud?

        Newer Versions:

          1. terraform login
          2. it will open the terraform cloud and generate the token
          3. paste that token back in the CLI
          https://learn.hashicorp.com/terraform/tfc/tfc_login


        Older versions:

          keep the following token in the CLI configuration file:

          credentials "app.terraform.io" {
            token = "xxxxxx.atlasv1.zzzzzzzzzzzzz"
          }

      Ref: <a target="_blank" href=https://www.terraform.io/docs/commands/cli-config.html#credentials><https://www.terraform.io/docs/commands/cli-config.html#credentials</a>

242. You are building infrastructure on your local machine and you changed yourbackend to remote backend with the Terraform cloud. What should you do tomigrate the state to the remote backend?

        terraform init

        Once you have authenticated the remote backend, you are ready to migrate your local state file to Terraform
        Cloud. To begin the migration, reinitialize. This causes Terraform to recognize your changed backend
        configuration.

        During reinitialization, Terraform presents a prompt saying that it will copy the state file to the new
        backend. Enter "yes" and Terraform will migrate the state from your local machine to Terraform Cloud.

      Ref: <a target="_blank" href=https://learn.hashicorp.com/terraform/tfc/tfc_migration#migrate-the-state-file>https://learn.hashicorp.com/terraform/tfc/tfc_migration#migrate-the-state-file</a>

243. How do you configure remote backend with the terraform cloud?

        You need to configure in the terraform block

        terraform {
          backend "remote" {
            hostname = "app.terraform.io"
            organization = "<YOUR-ORG-NAME>"
            workspaces {
              name = "state-migration"
            }
          }
        }

244. What is Run Triggers?

        Terraform Cloud’s run triggers allow you to link workspaces so that a successful apply in a source workspace
        will queue a run in the workspace linked to it with a run trigger. For example, adding new subnets to your
        network configuration could trigger an update to your application configuration to rebalance servers across
        the new subnets.

245. What is the benefit of Run Triggers?

        When managing complex infrastructure with Terraform Cloud, organizing your configuration into different
        workspaces helps you to better manage and design your infrastructure.
        Configuring run triggers between workspaces allows you to set up infrastructure pipelines as part of your
        overall deployment strategy.

246. What are the available permissions that terraform clouds can have?

        Terraform Cloud teams can have read, plan, write, or admin permissions on individual workspaces.

247. Who can grant permissions on the workspaces?

        Organization owners grant permissions by grouping users into teams and giving those teams priviliges based
        on their need for access to individual workspaces.

248. Which plan do you need to manage teams on Terraform cloud?

        Team Plan

249. How can you add users to an organization?

        You can add users to an organization by inviting them using their email address. Even if your team member
        has not signed up for Terraform Cloud yet, they can still accept the invitation and create a new account.

250. The Terraform Cloud Team plan charges you on a per-user basis. Is this true?

        Yes. The Terraform Cloud Team plan is charged on a per-user basis so adding new users to your organization
        incurs cost.


---

<br>
<br>
{!footer.md!}
