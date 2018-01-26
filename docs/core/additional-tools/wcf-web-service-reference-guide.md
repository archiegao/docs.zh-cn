---
title: "Microsoft WCF Web Service Reference Provider 工具"
description: "Microsoft WCF Web Service Reference Provider 工具概述，该工具添加了 .NET Core 和 ASP.NET Core 项目的功能，类似于 .NET Framework 项目的添加服务引用。"
author: mlacouture
manager: wpickett
ms.author: johalex
ms.date: 01/19/2018
ms.topic: article
ms.prod: .net-core
ms.custom: mvc
ms.openlocfilehash: 210f0a9bbf393055ebcd582d3accb3d77b1c9539
ms.sourcegitcommit: 8bde7a3432f30fc771079744955c75c58c4eb393
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/20/2018
---
# <a name="microsoft-wcf-web-service-reference-provider-tool"></a><span data-ttu-id="effe8-103">Microsoft WCF Web Service Reference Provider 工具</span><span class="sxs-lookup"><span data-stu-id="effe8-103">Microsoft WCF Web Service Reference Provider Tool</span></span>

<span data-ttu-id="effe8-104">多年来，许多 Visual Studio 开发者在其. NET Framework 项目需要访问 Web 服务时，都享受到了[添加服务引用](../../visualstudio/data-tools/how-to-add-update-or-remove-a-wcf-data-service-reference)工具所带来的工作效率。</span><span class="sxs-lookup"><span data-stu-id="effe8-104">Over the years, many Visual Studio developers have enjoyed the productivity that the [**Add Service Reference**](../../visualstudio/data-tools/how-to-add-update-or-remove-a-wcf-data-service-reference) tool provided when their .NET Framework projects needed to access web services.</span></span>  <span data-ttu-id="effe8-105">WCF Web 服务引用工具是 Visual Studio 连接服务的扩展，提供了类似于 .NET Core 和 ASP.NET Core 项目的“添加服务引用”功能的体验。</span><span class="sxs-lookup"><span data-stu-id="effe8-105">The **WCF Web Service Reference** tool is a Visual Studio connected service extension that provides an experience like the Add Service Reference functionality for .NET Core and ASP.NET Core projects.</span></span> <span data-ttu-id="effe8-106">此工具可从网络位置的当前解决方案的 web 服务中或从 WSDL 文件中检索元数据，并生成包含可用于访问 web 服务的 Windows Communication Foundation (WCF) 客户端代理代码的可兼容 .NET Core 的源文件。</span><span class="sxs-lookup"><span data-stu-id="effe8-106">This tool retrieves metadata from a web service in the current solution, on a network location, or from a WSDL file, and generates a .NET Core compatible source file containing Windows Communication Foundation (WCF) client proxy code that you can use to access the web service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="effe8-107">应仅从受信任源引用服务。</span><span class="sxs-lookup"><span data-stu-id="effe8-107">You should only reference services from a trusted source.</span></span> <span data-ttu-id="effe8-108">从不受信任的源添加引用可能会危及安全性。</span><span class="sxs-lookup"><span data-stu-id="effe8-108">Adding references from an untrusted source may compromise security.</span></span> 

## <a name="how-to-use-the-extension"></a><span data-ttu-id="effe8-109">如何使用扩展</span><span class="sxs-lookup"><span data-stu-id="effe8-109">How to use the extension</span></span>

> [!NOTE]
> <span data-ttu-id="effe8-110">“WCF Web 服务引用”选项适用于使用以下项目模板创建的项目：</span><span class="sxs-lookup"><span data-stu-id="effe8-110">The **WCF Web Service Reference** option is applicable to projects created using the following project templates:</span></span>
> * <span data-ttu-id="effe8-111">Visual C# > .NET Core</span><span class="sxs-lookup"><span data-stu-id="effe8-111">**Visual C#** > **.NET Core**</span></span>
> * <span data-ttu-id="effe8-112">Visual C# > .NET Standard</span><span class="sxs-lookup"><span data-stu-id="effe8-112">**Visual C#** > **.NET Standard**</span></span>
> * <span data-ttu-id="effe8-113">Visual C# > Web > ASP.NET Core Web 应用程序</span><span class="sxs-lookup"><span data-stu-id="effe8-113">**Visual C#** > **Web** > **ASP.NET Core Web Application**</span></span>

<span data-ttu-id="effe8-114">以“ASP.NET 核心 Web 应用程序”项目模板为例，本文将介绍如何向该项目中添加 WCF 服务引用：</span><span class="sxs-lookup"><span data-stu-id="effe8-114">Using the **ASP.NET Core Web Application** project template as an example, this article walks you through adding a WCF service reference to the project:</span></span>

1. <span data-ttu-id="effe8-115">在解决方案资源管理器中，双击项目的“连接的服务”节点（对于 .NET Core 或 .NET Standard 项目，当在解决方案资源管理器中右键单击项目的“依赖项”节点时，该选项可用）。</span><span class="sxs-lookup"><span data-stu-id="effe8-115">In Solution Explorer, double-click the **Connected Services** node of the project (for a .NET Core or .NET Standard project this option is available when you right-click on the **Dependencies** node of the project in Solution Explorer).</span></span>

<span data-ttu-id="effe8-116">随即显示“连接的服务”页，如下图所示：</span><span class="sxs-lookup"><span data-stu-id="effe8-116">The **Connected Services** page appears as shown in the following image:</span></span>

![“连接的服务”选项卡](./media/wcf-web-service-reference-guide/wcfcs-ConnectedServicesPage.png)

2. <span data-ttu-id="effe8-118">在“连接的服务”页上，单击“Microsoft WCF Web Service Reference Provider”。</span><span class="sxs-lookup"><span data-stu-id="effe8-118">On the **Connected Services** page, click **Microsoft WCF Web Service Reference Provider**.</span></span> <span data-ttu-id="effe8-119">此操作将显示“配置 WCF Web 服务引用”向导：</span><span class="sxs-lookup"><span data-stu-id="effe8-119">This brings up the **Configure WCF Web Service Reference** wizard:</span></span>

![“服务终结点”选项卡](./media/wcf-web-service-reference-guide/wcfcs-ServiceEndpointPage.png)

3. <span data-ttu-id="effe8-121">选择服务。</span><span class="sxs-lookup"><span data-stu-id="effe8-121">Select a service.</span></span>

    <span data-ttu-id="effe8-122">3a.</span><span class="sxs-lookup"><span data-stu-id="effe8-122">3a.</span></span> <span data-ttu-id="effe8-123">“配置 WCF Web 服务引用”向导中提供了多个服务搜索选项：</span><span class="sxs-lookup"><span data-stu-id="effe8-123">There are several services search options available within the **Configure WCF Web Service Reference** wizard:</span></span>
    
     * <span data-ttu-id="effe8-124">要搜索当前解决方案中定义的服务，请单击“发现”按钮。</span><span class="sxs-lookup"><span data-stu-id="effe8-124">To search for services defined in the current solution, click the **Discover** button.</span></span> 
     * <span data-ttu-id="effe8-125">要搜索在指定地址托管的服务，请在“地址”框中输入服务 URL，然后单击“转到”按钮。</span><span class="sxs-lookup"><span data-stu-id="effe8-125">To search for services hosted at a specified address, enter a service URL in the **Address** box and click the **Go** button.</span></span>
     * <span data-ttu-id="effe8-126">要选择包含 Web 服务元数据信息的 WSDL 文件，请单击“浏览”按钮。</span><span class="sxs-lookup"><span data-stu-id="effe8-126">To select a WSDL file that contains the web service metadata information, click the **Browse** button.</span></span> 
     
    <span data-ttu-id="effe8-127">3b.</span><span class="sxs-lookup"><span data-stu-id="effe8-127">3b.</span></span> <span data-ttu-id="effe8-128">从“服务”框内的搜索结果列表中选择服务。</span><span class="sxs-lookup"><span data-stu-id="effe8-128">Select the service from the search results list in the **Services** box.</span></span> <span data-ttu-id="effe8-129">如果需要，请在相应的“名称空间”文本框中为生成的代码输入命名空间。</span><span class="sxs-lookup"><span data-stu-id="effe8-129">If needed, enter the namespace for the generated code in the corresponding **Namespace** text box.</span></span>
    
    <span data-ttu-id="effe8-130">3c.</span><span class="sxs-lookup"><span data-stu-id="effe8-130">3c.</span></span> <span data-ttu-id="effe8-131">单击“下一步”按钮，打开“数据类型选项”页和“客户端选项”页。</span><span class="sxs-lookup"><span data-stu-id="effe8-131">Click the **Next** button to open the **Data Type Options** and the **Client Options** pages.</span></span> <span data-ttu-id="effe8-132">或者，单击“完成”按钮，使用默认选项。</span><span class="sxs-lookup"><span data-stu-id="effe8-132">Alternatively, click the **Finish** button to use the default options.</span></span>


4. <span data-ttu-id="effe8-133">“数据类型选项”窗体可用于优化生成的服务引用配置设置：</span><span class="sxs-lookup"><span data-stu-id="effe8-133">The **Data Type Options** form enables you to refine the generated service reference configuration settings:</span></span>

![“数据类型选项”选项卡](./media/wcf-web-service-reference-guide/wcfcs-DataTypesPage.png)

> [!NOTE]
> <span data-ttu-id="effe8-135">如果在项目的引用程序集中定义了服务引用代码生成所需的数据类型，则“重新使用引用程序集中的类型”复选框选项将非常有用。</span><span class="sxs-lookup"><span data-stu-id="effe8-135">The **Reuse types in referenced assemblies** check box option is useful when data types needed for service reference code generation are defined in one of your project's referenced assemblies.</span></span>  <span data-ttu-id="effe8-136">重新使用这些现有数据类型，从而避免编译时类型冲突或运行时问题，这是非常重要的。</span><span class="sxs-lookup"><span data-stu-id="effe8-136">It's important to reuse those existing data types to avoid compile-time type clash or runtime issues.</span></span>

<span data-ttu-id="effe8-137">加载类型信息时可能会有延迟，具体取决于项目依赖项和其他系统性能因素的数量。</span><span class="sxs-lookup"><span data-stu-id="effe8-137">There may be a delay while type information is loaded, depending on the number of project dependencies and other system performance factors.</span></span> <span data-ttu-id="effe8-138">加载过程中，“完成”按钮被禁用，除非未选中“重新使用引用程序集中的类型”复选框。</span><span class="sxs-lookup"><span data-stu-id="effe8-138">The **Finish** button is disabled during loading unless the **Reuse types in referenced assemblies** check box is unchecked.</span></span>

5. <span data-ttu-id="effe8-139">完成后，单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="effe8-139">Click **Finish** when you are done.</span></span>


<span data-ttu-id="effe8-140">在显示进度的同时，工具：</span><span class="sxs-lookup"><span data-stu-id="effe8-140">While displaying progress, the tool:</span></span>

* <span data-ttu-id="effe8-141">从 WCF 服务下载元数据。</span><span class="sxs-lookup"><span data-stu-id="effe8-141">Downloads metadata from the WCF service.</span></span> 
* <span data-ttu-id="effe8-142">在名为“reference.cs”的文件中生成服务引用代码，并将其添加到“连接的服务”节点下的项目。</span><span class="sxs-lookup"><span data-stu-id="effe8-142">Generates the service reference code in a file named *reference.cs*, and adds it to your project under the **Connected Services** node.</span></span> 
* <span data-ttu-id="effe8-143">使用在目标平台上编译和运行所需的 NuGet 包引用更新项目文件 (.csproj)。</span><span class="sxs-lookup"><span data-stu-id="effe8-143">Updates the project file (.csproj) with NuGet package references required to compile and run on the target platform.</span></span>

![进度窗口](./media/wcf-web-service-reference-guide/wcfcs-ProgressWindow.png)

<span data-ttu-id="effe8-145">进度完成后，可创建生成的 WCF 客户端类型的实例并调用服务操作。</span><span class="sxs-lookup"><span data-stu-id="effe8-145">When these processes complete, you can create an instance of the generated WCF client type and invoke the service operations.</span></span>

## <a name="next-steps"></a><span data-ttu-id="effe8-146">后续步骤</span><span class="sxs-lookup"><span data-stu-id="effe8-146">Next steps</span></span>

### <a name="feedback--questions"></a><span data-ttu-id="effe8-147">反馈和问题</span><span class="sxs-lookup"><span data-stu-id="effe8-147">Feedback & questions</span></span>
<span data-ttu-id="effe8-148">如果有任何问题或反馈，请[在 GitHub 上提问](https://github.com/dotnet/wcf/issues/new)。</span><span class="sxs-lookup"><span data-stu-id="effe8-148">If you have any questions or feedback, [open an issue on GitHub](https://github.com/dotnet/wcf/issues/new).</span></span> <span data-ttu-id="effe8-149">也可以在 [GitHub 上的 WCF 存储库](https://github.com/dotnet/wcf/issues?utf8=%E2%9C%93&q=is:issue%20label:tooling)中查看任何现有问题。</span><span class="sxs-lookup"><span data-stu-id="effe8-149">You can also review any existing questions or issues [at the WCF repo on GitHub](https://github.com/dotnet/wcf/issues?utf8=%E2%9C%93&q=is:issue%20label:tooling).</span></span>

### <a name="release-notes"></a><span data-ttu-id="effe8-150">发行说明</span><span class="sxs-lookup"><span data-stu-id="effe8-150">Release notes</span></span>
* <span data-ttu-id="effe8-151">请参阅[发行说明](https://github.com/dotnet/wcf/blob/master/release-notes/WCF-Web-Service-Reference-notes.md)，了解更新的版本信息（包括已知问题）。</span><span class="sxs-lookup"><span data-stu-id="effe8-151">Refer to the [Release notes](https://github.com/dotnet/wcf/blob/master/release-notes/WCF-Web-Service-Reference-notes.md) for updated release information, including known issues.</span></span> 