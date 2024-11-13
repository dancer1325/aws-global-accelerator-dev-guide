# What is AWS Global Accelerator?<a name="what-is-global-accelerator"></a>

* AWS Global Accelerator
  * := global service / 
    * allow
      * creating *accelerators*
        * -- to improve the -- performance of your applications for local & global users /
          * if there are changes | health or configuration -> react immediately -- to ensure that internet traffic -- is ALWAYS directed to -- healthy endpoints
        * types
          * standard accelerator
            * allows
              * improve availability of your internet applications / used by a global audience
              * traffic -- is directed, over the AWS global network, to -- endpoints | most optimal Region to the client
                * optimal -- is based on --
                  * health
                  * client location
                  * policies / you configure
            * type of endpoints / supported
              * Network Load Balancers,
              * Application Load Balancers,
              * Amazon EC2 instances,
              * Elastic IP addresses  
          * custom routing accelerator
            * allows
              * \>=1 users -- can be mapped to a -- specific destination
            * type of endpoints / supported
              * VPC subnet endpoint types
                * -> ONLY support, -- route traffic to -- VPC subnet's private IP addresses 
    * supports
      * endpoints | MULTIPLE AWS Regions
    * provide
      * by default,
        * static IP addresses / 
          * you -- associate with your -- accelerator
          * ANYCAST -- from the -- AWS edge network
          * if 
            * IPv4, -> 2 static IPv4 addresses 
              * you can configure it / | your own IP address ranges
            * dual-stack, -> 2 static IPv4 addresses + 2 static IPv6 addresses
              * IPv4 addresses -- can be configured -- / | your own IP address ranges
            * you disable the accelerator -> static IP addresses 
              * -- remain assigned to -- your accelerator
              * NO longer accepts or routes traffic
            * you *delete* the accelerator -> static IP addresses
              * is lost
              * NO longer route traffic 
    * see
      * [AWS Regional Services List](http://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/)
      * [ABAC with Global Accelerator](security_iam_service-with-iam.md#security_iam_service-with-iam-tags)
    * actions | it -- are limited via -- IAM policies

**Topics**
+ [AWS Global Accelerator components](introduction-components.md)
+ [How AWS Global Accelerator works](introduction-how-it-works.md)
+ [Types of accelerators](introduction-accelerator-types.md)
+ [Location and IP address ranges of Global Accelerator Edge servers](introduction-ip-ranges.md)
+ [AWS Global Accelerator use cases](introduction-benefits-of-migrating.md)
+ [AWS Global Accelerator Speed Comparison Tool](introduction-speed-comparison-tool.md)
+ [How to get started with AWS Global Accelerator](introduction-get-started.md)
+ [Tagging in AWS Global Accelerator](tagging-in-global-accelerator.md)
+ [Pricing for AWS Global Accelerator](introduction-pricing.md)