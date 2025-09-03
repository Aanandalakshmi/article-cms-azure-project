# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

A Virtual Machine offers complete control over the operating system and environment, allowing the installation of any required software or custom configurations. However, this comes at a higher cost since the VM must be provisioned and maintained continuously, including expenses for compute, storage, and licensing. Additionally, scalability with VMs is slower and often requires manual setup of scale sets and load balancers. Ensuring high availability also demands more effort, as multiple VMs and supporting infrastructure must be managed. On the other hand, Azure App Service provides a managed environment that is specifically optimized for hosting web applications. It follows a tier-based pay-as-you-go model, making it more cost-effective for a CMS app. App Service also includes built-in autoscaling, high availability, and seamless integration with CI/CD pipelines such as GitHub Actions. This eliminates the overhead of managing servers and allows the development team to focus on the application itself. 
Considering these factors, Azure App Service is the most appropriate solution for deploying the CMS application. It offers better cost efficiency, scalability, and workflow automation, while abstracting the complexity of infrastructure management that would otherwise burden the team.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
Although App Service is the best option for the current CMS application, the decision could change if the application requirements evolve. If the app required specialized software, custom operating system configurations, or dependencies not supported by App Service, then a Virtual Machine would be more suitable. Similarly, if the application demanded strict compliance measures, advanced OS-level security hardening, or complex networking rules, a VM would provide the necessary control. In cases where the CMS grows into a multi-tier system involving multiple services or background workers beyond the web tier, a more flexible solution like Virtual Machines or even Azure Kubernetes Service (AKS) would be appropriate. Furthermore, if the application required high-performance computing, GPU support, or extensive customizations at the infrastructure level, App Service might no longer be sufficient. In such scenarios, deploying the app on a VM would offer the flexibility and performance needed. Thus, while App Service is ideal for the current web-based CMS, changes in complexity, compliance, or performance requirements could shift the decision towards VMs or container-based solutions.
