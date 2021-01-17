---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471525"
---
# <span data-ttu-id="234f1-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="234f1-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="234f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="234f1-102">SYNOPSIS</span></span>
<span data-ttu-id="234f1-103">Fügt einer "PsApiManagement"-Instanz neue Bereitstellungsregionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="234f1-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="234f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="234f1-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="234f1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="234f1-105">DESCRIPTION</span></span>
<span data-ttu-id="234f1-106">Das **Cmdlet "Add-AzApiManagementRegion"** fügt der Sammlung **"AdditionalRegions"** der bereitgestellten Instanz des Typs **"Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement"** eine neue Instanz des Typs **"PsApiManagementRegion"** hinzu.</span><span class="sxs-lookup"><span data-stu-id="234f1-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="234f1-107">Dieses Cmdlet stellt nichts allein zur Verfügung, sondern aktualisiert die Instanz **von PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="234f1-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="234f1-108">Um eine Bereitstellung einer API Management zu aktualisieren, übergeben Sie die geänderte **"PsApiManagement"-Instanz** an "Set-AzApiManagement".</span><span class="sxs-lookup"><span data-stu-id="234f1-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="234f1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="234f1-109">EXAMPLES</span></span>

### <span data-ttu-id="234f1-110">Beispiel 1: Hinzufügen neuer Bereitstellungsregionen zu einer Instanz "PsApiManagement"</span><span class="sxs-lookup"><span data-stu-id="234f1-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="234f1-111">Mit diesem Befehl werden der Instanz **"PsApiManagement"** zwei Premium-SKU-Einheiten und die Region "Ost US" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="234f1-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="234f1-112">Beispiel 2: Hinzufügen neuer Bereitstellungsregionen zu einer Instanz "PsApiManagement" und anschließendes Aktualisieren der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="234f1-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="234f1-113">Dieser Befehl ruft ein **"PsApiManagement"-Objekt** ab, fügt zwei Premium-SKU-Einheiten für die Region "Ost-USA" hinzu und aktualisiert dann die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="234f1-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="234f1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="234f1-114">PARAMETERS</span></span>

### <span data-ttu-id="234f1-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="234f1-115">-ApiManagement</span></span>
<span data-ttu-id="234f1-116">Gibt die **Instanz "PsApiManagement"** an, der dieses Cmdlet weitere Bereitstellungsregionen hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="234f1-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="234f1-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="234f1-117">-Capacity</span></span>
<span data-ttu-id="234f1-118">Gibt die SKU-Kapazität des Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="234f1-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="234f1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="234f1-119">-DefaultProfile</span></span>
<span data-ttu-id="234f1-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="234f1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="234f1-121">-Location</span><span class="sxs-lookup"><span data-stu-id="234f1-121">-Location</span></span>
<span data-ttu-id="234f1-122">Gibt den Speicherort der neuen Bereitstellungsregion unter der unterstützten Region für den Api-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="234f1-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="234f1-123">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | dabei {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object von Speicherorten</span><span class="sxs-lookup"><span data-stu-id="234f1-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="234f1-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="234f1-124">-Sku</span></span>
<span data-ttu-id="234f1-125">Gibt die Stufe der Bereitstellungsregion an.</span><span class="sxs-lookup"><span data-stu-id="234f1-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="234f1-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="234f1-126">Valid values are:</span></span> 
- <span data-ttu-id="234f1-127">Entwickler</span><span class="sxs-lookup"><span data-stu-id="234f1-127">Developer</span></span>
- <span data-ttu-id="234f1-128">Standard</span><span class="sxs-lookup"><span data-stu-id="234f1-128">Standard</span></span>
- <span data-ttu-id="234f1-129">Premium</span><span class="sxs-lookup"><span data-stu-id="234f1-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="234f1-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="234f1-130">-VirtualNetwork</span></span>
<span data-ttu-id="234f1-131">Gibt eine virtuelle Netzwerkkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="234f1-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="234f1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="234f1-132">CommonParameters</span></span>
<span data-ttu-id="234f1-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="234f1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="234f1-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="234f1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="234f1-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="234f1-135">INPUTS</span></span>

### <span data-ttu-id="234f1-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="234f1-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="234f1-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="234f1-137">OUTPUTS</span></span>

### <span data-ttu-id="234f1-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="234f1-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="234f1-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="234f1-139">NOTES</span></span>
* <span data-ttu-id="234f1-140">Das Cmdlet schreibt die aktualisierte **Instanz "PsApiManagement"** in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="234f1-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="234f1-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="234f1-141">RELATED LINKS</span></span>

[<span data-ttu-id="234f1-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="234f1-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="234f1-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="234f1-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="234f1-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="234f1-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


