# Azure Cloud Native Solution Architect

## Run
### Running Azure Functions Locally
Follow this: https://docs.microsoft.com/en-us/azure/azure-functions/durable/durable-functions-create-first-csharp?pivots=code-editor-vscode

Dependencies:
* Azure Functions Core Tools - lets you develop and test your functions on your local computer from the command prompt or terminal
* .NET Core SDK verson 6

Then from the root of the folder, e.g. /Users/bobbylei/Desktop/learn/The-Azure-Cloud-Native-Architecture-Mapbook/Chapter02/code/PacktOrchestrationDemo run the command 'func start'

## Notes
* DIKW Pyramind
  * data: 31,3,3000
  * information: day 31, month March, visits 3000
  * knowledge: upto 3000 user visits on our website on March 31, which is way above our daily average of 650. 31 March seems like a busy day of the year
  * wisdom: we will make sure to restock our warehouses before March 31
* Cloud native's defense in depth primarily relies on identity, while traditional defense in depth relies heavily on the network perimeter. This gap is often a source of tension between the cloud and non-cloud worlds.
* Infrastructure architects play a prominent role in setting up hybrid infrastructures, which bridge both the cloud and the on-premises world. Their diagrams reflect an infrastructure-only view, often related to the concept of a landing zone, which consists of defining how and where business assets will be hosted.
* Typical transversal drivers (when moving to the cloud) are cost optimization and a faster time to market
  * Cost optimization can be achieved by leveraging the economies of scale from multi-tenant infrastructures
  * A faster time to market is conceived by maximizing outsourcing from the cloud provider
* Most of the time, the cloud makes companies transition from CAPEX to OPEX
  * Before the cloud, organizations only had one way to pay for their IT infrastructure, which was upfront and as a capital expense (CapEx).
  * IT managers would have to research everything from servers to racks to everything involved in the storage, and then procure them before they could start to think about implementation.
  * So, before they even turned it on, they incurred tens of thousands of dollars in CapEx
  * It was because of this, IT had earned the reputation of being a cost center of most companies because it was a necessary cost but didn’t add much value to the business.
* Cloud migration enablers (based on COBIT governance framework)
  * Principles, Policies, and Frameworks: This could be summarized as such: what is clearly thought is clearly expressed. You should identify your core principles and policies that are in line with the business drivers. These will be later shared and reused by all involved parties. Writing a mission statement is also something that may help everyone to understand the big picture.
  * Processes: The actual means to executing policies and transforming the principles into tangible outcomes.
  * Organizational Structures: A key enabler to putting the organization in motion toward the business and IT goals. This is where management and sponsorship play an important role. Defining a team (or virtual cloud team), a stakeholder map, and, first and foremost, a platform owner, accountable for everything that happens in the cloud, who can steer activities.
  * Culture, Ethics, and Behavior: This is the DNA of the company. Is it a risk-adverse company? Are they early adopters? The mindset of people working in the company has a serious impact on the journey. Sometimes, the DNA is even inherited from the industry (banking, military, and so on) that the company operates in. With a bit of experience, it is easy to anticipate most of the obstacles you will be facing just by knowing the industry practices.
  * Information: This enabler leverages information practices as a way to spread new practices in a more efficient way.
  * Services, Infrastructure, and Applications: Designing and defining services is not an easy thing. It is important to re-think your processes and services to be more cloud-native, and not just lift and shift them as is.
  * People, Skills, and Competencies: Skills are always a problem when you start a cloud journey. You might rely on different sourcing strategies: in-staffing, outsourcing, ..., but overall, you should always try to answer the question everyone is asking themselves: what's in it for me in that cloud journey? In large organizations, a real change management program is required to accompany people on that journey.
* Examples of cloud migration principles (business drivers: time to market, new capabilities enabled by technology, cost optimization)
  * SaaS over FaaS over PaaS over CaaS over IaaS: In a nutshell, this principle means that we should buy instead of building first, since it is usually faster to buy than build. If we build, we should start from the most provider-managed service model to the most self-managed flavor. Here again, the idea is to gain time by delegating most of the infrastructure and operational burden to the provider, which does not mean that there is nothing left to do as a cloud consumer. This should help address both the time-to-market driver, as well as the exponential growth of the operational teams. From left to right, the service models are also ordered from the most to the least cloud-native. CaaS is an exception to this, but the level of operational work remains quite important, which could play against our main driver here.
  * Best of suite versus best of breed: This principle aims at forcing people to first check what is native to the platform before bringing their own solutions. Bringing on-premises solutions to the cloud inevitably impacts time. Best of suite ensures a higher compatibility and integration with the rest of the ecosystem. Following this principle will surely lock you in more to the cloud provider, but leveraging built-in solutions is more cost- and time-efficient.
  * Aim at multi-cloud but start with one: In the longer run, aim at multi-cloud to avoid vendor locking. However, start with one cloud. The journey will already be difficult, so it's important to concentrate the efforts and stay focused on the objectives. In the short term, try to make smart choices that do not impact cost and time: do not miss low hanging fruit.
  * Design with security in mind: This principle should always be applied, even on-premises, but the cloud makes it a primary concern. With this principle, you should make sure to involve all the security stakeholders from the start, so as to avoid any unpleasant surprises.
  * Leverage automation: Launching faster means having an efficient CI/CD toolchain. The cloud offers unique infrastructure-as-code capabilities that help deploy faster.
  * Multi-tenant over privatization: While privatization might give you more control, it also means a risk of reintroducing your on-premises practices to the cloud. Given the audit reports we had, we see that this might not be a good idea. Leveraging multi-tenant PaaS services that have been designed for millions of organizations worldwide is a better response to the business drivers.

## Book Source Code
https://github.com/PacktPublishing/The-Azure-Cloud-Native-Architecture-Mapbook

## Upto
Page 86

Looking at the code in action

Follow this to see how you can run Azure Durable Functions locally using C#
https://docs.microsoft.com/en-us/azure/azure-functions/durable/durable-functions-create-first-csharp?pivots=code-editor-vscode
