---
title: Verwalten von Azure-Ressourcen mit Invoke-AzRestMethod
description: Hier erfahren Sie, wie Sie Azure PowerShell zum Verwalten von Ressourcen mit dem Cmdlet „Invoke-AzRestMethod“ verwenden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5fdb8543630198d141d42626dc3a8b85f0bcdaa7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012016"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a><span data-ttu-id="e474b-103">Verwalten von Azure-Ressourcen mit Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="e474b-103">Manage Azure resources with Invoke-AzRestMethod</span></span>

<span data-ttu-id="e474b-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) ist ein Azure PowerShell-Cmdlet, das in Version 4.4.0 des Az PowerShell-Moduls eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e474b-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) is an Azure PowerShell cmdlet that was introduced in Az PowerShell module version 4.4.0.</span></span> <span data-ttu-id="e474b-105">Mit diesem Cmdlet können Sie benutzerdefinierte HTTP-Anforderungen unter Verwendung des Az-Kontexts an den ARM-Endpunkt (Azure Resource Manager) senden.</span><span class="sxs-lookup"><span data-stu-id="e474b-105">It allows you to make custom HTTP requests to the Azure Resource Management (ARM) endpoint using the Az context.</span></span>

<span data-ttu-id="e474b-106">Dieses Cmdlet ist nützlich, wenn Sie Azure-Dienste im Hinblick auf Features verwalten möchten, die im Az PowerShell-Modul noch nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e474b-106">This cmdlet is useful when you want to manage Azure services for features that aren't yet available in the Az PowerShell module.</span></span>

## <a name="how-to-use-invoke-azrestmethod"></a><span data-ttu-id="e474b-107">Verwenden von „Invoke-AzRestMethod“</span><span class="sxs-lookup"><span data-stu-id="e474b-107">How to use Invoke-AzRestMethod</span></span>

<span data-ttu-id="e474b-108">Sie können beispielsweise Zugriff auf Azure Container Registry (ACR) ausschließlich für bestimmte Netzwerke zulassen oder den öffentlichen Zugriff verweigern.</span><span class="sxs-lookup"><span data-stu-id="e474b-108">As an example, you can allow access to Azure Container Registry (ACR) only for specific networks or deny public access.</span></span> <span data-ttu-id="e474b-109">Ab Version 4.5.0 des Az PowerShell-Moduls ist dieses Feature im [PowerShell-Modul „Az.ContainerRegistry“](/powershell/module/Az.ContainerRegistry/) noch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e474b-109">As of Az PowerShell module version 4.5.0, that feature isn't available yet in the [Az.ContainerRegistry PowerShell module](/powershell/module/Az.ContainerRegistry/).</span></span> <span data-ttu-id="e474b-110">Es kann in der Zwischenzeit jedoch mit `Invoke-AzRestMethod` verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e474b-110">However, it can be managed in the interim with `Invoke-AzRestMethod`.</span></span>

## <a name="using-invoke-azrestmethod-with-get-operations"></a><span data-ttu-id="e474b-111">Verwenden von „Invoke-AzRestMethod“ mit GET-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="e474b-111">Using Invoke-AzRestMethod with GET operations</span></span>

<span data-ttu-id="e474b-112">Im folgenden Beispiel wird die Verwendung des Cmdlets `Invoke-AzRestMethod` in Verbindung mit einem GET-Vorgang veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="e474b-112">The following example demonstrates how to use the `Invoke-AzRestMethod` cmdlet with a GET operation:</span></span>

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

<span data-ttu-id="e474b-113">Um maximale Flexibilität zu ermöglichen, ist der Großteil der Parameter für `Invoke-AzRestMethod` optional.</span><span class="sxs-lookup"><span data-stu-id="e474b-113">To allow maximum flexibility, most of the parameters for `Invoke-AzRestMethod` are optional.</span></span>
<span data-ttu-id="e474b-114">Wenn Sie jedoch Ressourcen innerhalb einer Ressourcengruppe verwalten, müssen Sie wahrscheinlich entweder die vollständige ID für die Ressource oder Parameter wie Ressourcengruppe, Ressourcenanbieter und Ressourcentyp angeben.</span><span class="sxs-lookup"><span data-stu-id="e474b-114">However, when you're managing resources within a resource group, you'll most likely need to provide either the full ID to the resource or parameters like resource group, resource provider, and resource type.</span></span>

<span data-ttu-id="e474b-115">Die Parameter `ResourceType` und `Name` können bei Ressourcen, die mehr als einen Namen erfordern, mehrere Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="e474b-115">The `ResourceType` and `Name` parameters can take multiple values when targeting resources that require more than one name.</span></span> <span data-ttu-id="e474b-116">Zum Bearbeiten einer gespeicherten Suche in einem Log Analytics-Arbeitsbereich sehen die Parameter etwa wie im folgenden Beispiel aus: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span><span class="sxs-lookup"><span data-stu-id="e474b-116">For example, to manipulate a saved search in a Log Analytics workspace, the parameters look like the following example: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span></span>

<span data-ttu-id="e474b-117">Das Cmdlet erstellt mithilfe einer Zuordnung, die auf der Position im Array basiert, die folgende Ressource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span><span class="sxs-lookup"><span data-stu-id="e474b-117">Using a mapping based on the position in the array, the cmdlet constructs the following resource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span></span>

<span data-ttu-id="e474b-118">Mit dem Parameter `APIVersion` können Sie eine bestimmte API-Version (einschließlich Vorschauversionen) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e474b-118">The `APIVersion` parameter allows you to use a specific API version, including preview ones.</span></span> <span data-ttu-id="e474b-119">Die unterstützten API-Versionen für Azure-Ressourcenanbieter finden Sie im GitHub-Repository [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs).</span><span class="sxs-lookup"><span data-stu-id="e474b-119">The supported API versions for Azure Resource providers can be found in the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub repository.</span></span>

<span data-ttu-id="e474b-120">Die Definition für die ACR-Version „2019-12-01-preview“ befindet sich an folgendem Speicherort: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span><span class="sxs-lookup"><span data-stu-id="e474b-120">You can find the definition for the 2019-12-01-preview version of ACR in the following location: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span></span>

## <a name="using-invoke-azrestmethod-with-patch-operations"></a><span data-ttu-id="e474b-121">Verwenden von „Invoke-AzRestMethod“ mit PATCH-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="e474b-121">Using Invoke-AzRestMethod with PATCH operations</span></span>

<span data-ttu-id="e474b-122">Sie können den öffentlichen Zugriff auf die vorhandene ACR-Instanz `myacr` in der Ressourcengruppe `myresourcegroup` mithilfe des Cmdlets `Invoke-AzRestMethod` deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e474b-122">You can disable public access to the existing ACR named `myacr` in the `myresourcegroup` resource group using the `Invoke-AzRestMethod` cmdlet.</span></span>

<span data-ttu-id="e474b-123">Wenn Sie den Zugriff auf das öffentliche Netzwerk deaktivieren möchten, senden Sie einen **PATCH**-Aufruf an die API, der den Wert des Parameters `publicNetwokAccess` wie im folgenden Beispiel gezeigt ändert:</span><span class="sxs-lookup"><span data-stu-id="e474b-123">To disable the public network access, you need to make a **PATCH** call to the API that changes the value of the `publicNetwokAccess` parameter as shown in the following example:</span></span>

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

<span data-ttu-id="e474b-124">Bei der Eigenschaft `Payload` handelt es sich um eine JSON-Zeichenfolge, die den Pfad der zu ändernden Eigenschaft zeigt.</span><span class="sxs-lookup"><span data-stu-id="e474b-124">The `Payload` property is a JSON string that shows the path of the property to be modified.</span></span>

<span data-ttu-id="e474b-125">Alle Parameter für diese API sind in der Datei **rest-api-spec** für diese API beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e474b-125">All the parameters for this API are described in the **rest-api-spec** file associated with this API.</span></span>
<span data-ttu-id="e474b-126">Die spezifische Definition für den publicNetworkAccess-Parameter finden Sie in der [JSON-Datei der Containerregistrierung](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) für die Vorschauversion „2019-12-01“ der API.</span><span class="sxs-lookup"><span data-stu-id="e474b-126">The specific definition for the publicNetworkAccess parameter can be found in the [container registry JSON file](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) for the 2019-12-01 preview version of the API.</span></span>

<span data-ttu-id="e474b-127">Wenn Sie den Zugriff auf die Registrierung nur von einer bestimmten IP-Adresse aus zulassen möchten, muss die Nutzlast wie im folgenden Beispiel gezeigt geändert werden:</span><span class="sxs-lookup"><span data-stu-id="e474b-127">To only allow access to the registry from a specific IP address, the payload needs to be modified as shown in the following example:</span></span>

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a><span data-ttu-id="e474b-128">Vergleich mit „Get-AzResource“, „New-AzResource“ und „Remove-AzResource“</span><span class="sxs-lookup"><span data-stu-id="e474b-128">Comparison to Get-AzResource, New-AzResource, and Remove-AzResource</span></span>

<span data-ttu-id="e474b-129">Mit den `*-AzResource`-Cmdlets können Sie den REST-API-Aufruf an Azure anpassen, indem Sie den Ressourcentyp, die API-Version und die zu aktualisierenden Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="e474b-129">The `*-AzResource` cmdlets allow you to customize the REST API call to Azure by specifying the resource type, the API version, and the properties to be updated.</span></span> <span data-ttu-id="e474b-130">Die Eigenschaften müssen jedoch zuerst als `PSObject` erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e474b-130">However, the properties need to be created first as a `PSObject`.</span></span> <span data-ttu-id="e474b-131">Dieser Vorgang erhöht die Komplexität und kann kompliziert werden.</span><span class="sxs-lookup"><span data-stu-id="e474b-131">This process adds an additional level of complexity and can easily become complicated.</span></span>

<span data-ttu-id="e474b-132">Mit `Invoke-AzRestMethod` lassen sich Azure-Ressourcen einfach verwalten.</span><span class="sxs-lookup"><span data-stu-id="e474b-132">`Invoke-AzRestMethod` offers a simple way to manage Azure resources.</span></span> <span data-ttu-id="e474b-133">Wie im vorherigen Beispiel gezeigt, können Sie eine JSON-Zeichenfolge erstellen und diese zum Anpassen des REST-API-Aufrufs verwenden, ohne vorab `PSObjects` erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="e474b-133">As shown in the previous example, you can build a JSON string and use it to customize the REST API call without having to precreate any `PSObjects`.</span></span>

<span data-ttu-id="e474b-134">Wenn Sie bereits mit den `*-AzResource`-Cmdlets vertraut sind, können Sie sie weiterhin verwenden.</span><span class="sxs-lookup"><span data-stu-id="e474b-134">If you're already familiar with the `*-AzResource` cmdlets, you can continue using them.</span></span> <span data-ttu-id="e474b-135">Es ist nicht geplant, ihre Unterstützung einzustellen.</span><span class="sxs-lookup"><span data-stu-id="e474b-135">We have no plans to stop supporting them.</span></span> <span data-ttu-id="e474b-136">Mit `Invoke-AzRestMethod` wurde dem Toolkit ein neues Cmdlet hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e474b-136">With `Invoke-AzRestMethod`, we have added a new cmdlet to your toolkit.</span></span>

## <a name="see-also"></a><span data-ttu-id="e474b-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e474b-137">See Also</span></span>

* [<span data-ttu-id="e474b-138">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="e474b-138">Get-AzResource</span></span>](/powershell/module/az.resources/get-azresource)
* [<span data-ttu-id="e474b-139">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="e474b-139">New-AzResource</span></span>](/powershell/module/az.resources/new-azresource)
* [<span data-ttu-id="e474b-140">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="e474b-140">Remove-AzResource</span></span>](/powershell/module/az.resources/remove-azresource)
