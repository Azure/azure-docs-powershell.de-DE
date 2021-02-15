---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 3f9c88177d3f791acdd0be5c81eec2fb5bc6911c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400704"
---
# <span data-ttu-id="cf113-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="cf113-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="cf113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf113-102">SYNOPSIS</span></span>
<span data-ttu-id="cf113-103">Aktualisiert die vorhandene Bereitstellungsregion in der PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="cf113-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="cf113-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf113-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf113-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf113-105">DESCRIPTION</span></span>
<span data-ttu-id="cf113-106">Das **Cmdlet "Update-AzApiManagementRegion"** aktualisiert eine vorhandene Instanz des Typs **"Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion"** in einer Sammlung von **"AdditionalRegions"-Objekten** einer bereitgestellten Instanz des Typs **"Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement".**</span><span class="sxs-lookup"><span data-stu-id="cf113-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="cf113-107">Mit diesem Cmdlet wird nichts bereitgestellt, sondern eine Instanz von **PsApiManagement** im Arbeitsspeicher aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cf113-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="cf113-108">Um eine Bereitstellung einer API Management zu aktualisieren, verwenden Sie die geänderte **PsApiManagementInstance** für das Set-AzApiManagement Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf113-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="cf113-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf113-109">EXAMPLES</span></span>

### <span data-ttu-id="cf113-110">Beispiel 1: Erhöht die Kapazität der zusätzlichen Region in einer PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="cf113-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="cf113-111">Mit diesem Befehl wird der API Management Premium-SKU-Dienst mit Regionen in der Mitte Süden und der Mitte des Nordens der USA bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cf113-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="cf113-112">Anschließend erhöht sie die Kapazität der Region "USA, Nord-Mitte" mithilfe von **"Update-AzApiManagementRegion"** auf 2.</span><span class="sxs-lookup"><span data-stu-id="cf113-112">It then increases the Capacity of the North Central US region to 2 using the **Update-AzApiManagementRegion**.</span></span> <span data-ttu-id="cf113-113">Das nächste Cmdlet Set-AzApiManagement die Konfigurationsänderung auf den Api-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="cf113-113">The next cmdlet Set-AzApiManagement applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="cf113-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf113-114">PARAMETERS</span></span>

### <span data-ttu-id="cf113-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cf113-115">-ApiManagement</span></span>
<span data-ttu-id="cf113-116">Gibt die **Instanz "PsApiManagement"** an, in der eine vorhandene Bereitstellungsregion aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf113-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="cf113-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="cf113-117">-Capacity</span></span>
<span data-ttu-id="cf113-118">Gibt den neuen SKU-Kapazitätswert für die Bereitstellungsregion an.</span><span class="sxs-lookup"><span data-stu-id="cf113-118">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf113-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf113-119">-DefaultProfile</span></span>
<span data-ttu-id="cf113-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf113-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf113-121">-Location</span><span class="sxs-lookup"><span data-stu-id="cf113-121">-Location</span></span>
<span data-ttu-id="cf113-122">Gibt den Speicherort der zu aktualisierenden Bereitstellungsregion an.</span><span class="sxs-lookup"><span data-stu-id="cf113-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="cf113-123">Gibt den Speicherort der neuen Bereitstellungsregion unter der unterstützten Region für den Api-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="cf113-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="cf113-124">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | dabei {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object von Speicherorten</span><span class="sxs-lookup"><span data-stu-id="cf113-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf113-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="cf113-125">-Sku</span></span>
<span data-ttu-id="cf113-126">Gibt den neuen Tierwert für die Bereitstellungsregion an.</span><span class="sxs-lookup"><span data-stu-id="cf113-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="cf113-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="cf113-127">Valid values are:</span></span>
- <span data-ttu-id="cf113-128">Entwickler</span><span class="sxs-lookup"><span data-stu-id="cf113-128">Developer</span></span>
- <span data-ttu-id="cf113-129">Standard</span><span class="sxs-lookup"><span data-stu-id="cf113-129">Standard</span></span>
- <span data-ttu-id="cf113-130">Premium</span><span class="sxs-lookup"><span data-stu-id="cf113-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf113-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf113-131">-VirtualNetwork</span></span>
<span data-ttu-id="cf113-132">Gibt eine virtuelle Netzwerkkonfiguration für die Bereitstellungsregion an.</span><span class="sxs-lookup"><span data-stu-id="cf113-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="cf113-133">Durch $null werden virtuelle Netzwerkkonfigurationen für die Region entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf113-133">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf113-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf113-134">CommonParameters</span></span>
<span data-ttu-id="cf113-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf113-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf113-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf113-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf113-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf113-137">INPUTS</span></span>

### <span data-ttu-id="cf113-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="cf113-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="cf113-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cf113-139">System.String</span></span>

### <span data-ttu-id="cf113-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="cf113-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="cf113-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="cf113-141">System.Int32</span></span>

### <span data-ttu-id="cf113-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf113-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="cf113-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf113-143">OUTPUTS</span></span>

### <span data-ttu-id="cf113-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="cf113-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="cf113-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cf113-145">NOTES</span></span>

## <span data-ttu-id="cf113-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cf113-146">RELATED LINKS</span></span>

[<span data-ttu-id="cf113-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="cf113-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="cf113-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="cf113-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="cf113-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cf113-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
