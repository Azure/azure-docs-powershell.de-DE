---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: c2e01d4a3f6ee3466151202a1c1d681c9f4e5486
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944303"
---
# <span data-ttu-id="73b1a-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="73b1a-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="73b1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="73b1a-103">Aktualisiert den vorhandenen Bereitstellungsbereich in der PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="73b1a-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="73b1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73b1a-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73b1a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73b1a-105">DESCRIPTION</span></span>
<span data-ttu-id="73b1a-106">Das **Update-AzApiManagementRegion-Cmdlet** aktualisiert eine vorhandene Instanz vom Typ **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in einer Sammlung von **AdditionalRegions-Objekten** eines bereitgestellten Instanzentyps vom Typ **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="73b1a-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="73b1a-107">Dieses Cmdlet stellt nichts mehr zur Verfügung, sondern aktualisiert eine Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="73b1a-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="73b1a-108">Zum Aktualisieren einer Bereitstellung einer API-Verwaltung verwenden Sie die geänderte **PsApiManagementInstance** für das Set-AzApiManagement cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73b1a-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="73b1a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73b1a-109">EXAMPLES</span></span>

### <span data-ttu-id="73b1a-110">Beispiel 1: Erhöht die Kapazität der zusätzlichen Region in einer PsApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="73b1a-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="73b1a-111">Dieser Befehl ruft den API Management Premium SKU-Dienst ab, der Regionen in Süd-Zentral-USA und Nord-Zentral-USA hat.</span><span class="sxs-lookup"><span data-stu-id="73b1a-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="73b1a-112">Anschließend wird die Kapazität der Region "Usa, Norden, Mitte" mithilfe von **Set-AzApiManagement** auf 2 erhöht.</span><span class="sxs-lookup"><span data-stu-id="73b1a-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="73b1a-113">Das nächste Cmdlet **Set-AzApiManagement** wendet die Konfigurationsänderung auf den Api-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="73b1a-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

### <span data-ttu-id="73b1a-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="73b1a-114">Example 2</span></span>

<span data-ttu-id="73b1a-115">Aktualisiert den vorhandenen Bereitstellungsbereich in der PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="73b1a-115">Updates existing deployment region in PsApiManagement instance.</span></span> <span data-ttu-id="73b1a-116">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="73b1a-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## <span data-ttu-id="73b1a-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="73b1a-117">PARAMETERS</span></span>

### <span data-ttu-id="73b1a-118">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="73b1a-118">-ApiManagement</span></span>
<span data-ttu-id="73b1a-119">Gibt die **PsApiManagement-Instanz** zum Aktualisieren eines vorhandenen Bereitstellungsbereichs in an.</span><span class="sxs-lookup"><span data-stu-id="73b1a-119">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="73b1a-120">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="73b1a-120">-Capacity</span></span>
<span data-ttu-id="73b1a-121">Gibt den neuen SKU-Kapazitätswert für die Bereitstellungsregion an.</span><span class="sxs-lookup"><span data-stu-id="73b1a-121">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="73b1a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73b1a-122">-DefaultProfile</span></span>
<span data-ttu-id="73b1a-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73b1a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73b1a-124">-Location</span><span class="sxs-lookup"><span data-stu-id="73b1a-124">-Location</span></span>
<span data-ttu-id="73b1a-125">Gibt den Speicherort des zu aktualisierenden Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="73b1a-125">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="73b1a-126">Gibt den Speicherort der neuen Bereitstellungsregion unter der unterstützten Region für den Api-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="73b1a-126">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="73b1a-127">Um gültige Speicherorte zu erhalten, verwenden Sie das cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | wobei {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object Speicherorte</span><span class="sxs-lookup"><span data-stu-id="73b1a-127">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="73b1a-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="73b1a-128">-Sku</span></span>
<span data-ttu-id="73b1a-129">Gibt den neuen Wert der Ebene für den Bereitstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="73b1a-129">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="73b1a-130">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="73b1a-130">Valid values are:</span></span>
- <span data-ttu-id="73b1a-131">Entwickler</span><span class="sxs-lookup"><span data-stu-id="73b1a-131">Developer</span></span>
- <span data-ttu-id="73b1a-132">Standard</span><span class="sxs-lookup"><span data-stu-id="73b1a-132">Standard</span></span>
- <span data-ttu-id="73b1a-133">Premium</span><span class="sxs-lookup"><span data-stu-id="73b1a-133">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b1a-134">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73b1a-134">-VirtualNetwork</span></span>
<span data-ttu-id="73b1a-135">Gibt eine virtuelle Netzwerkkonfiguration für die Bereitstellungsregion an.</span><span class="sxs-lookup"><span data-stu-id="73b1a-135">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="73b1a-136">Durch $null werden virtuelle Netzwerkkonfigurationen für die Region entfernt.</span><span class="sxs-lookup"><span data-stu-id="73b1a-136">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="73b1a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73b1a-137">CommonParameters</span></span>
<span data-ttu-id="73b1a-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73b1a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73b1a-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73b1a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73b1a-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73b1a-140">INPUTS</span></span>

### <span data-ttu-id="73b1a-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="73b1a-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="73b1a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="73b1a-142">System.String</span></span>

### <span data-ttu-id="73b1a-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="73b1a-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="73b1a-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="73b1a-144">System.Int32</span></span>

### <span data-ttu-id="73b1a-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73b1a-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="73b1a-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73b1a-146">OUTPUTS</span></span>

### <span data-ttu-id="73b1a-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="73b1a-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="73b1a-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="73b1a-148">NOTES</span></span>

## <span data-ttu-id="73b1a-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="73b1a-149">RELATED LINKS</span></span>

[<span data-ttu-id="73b1a-150">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="73b1a-150">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="73b1a-151">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="73b1a-151">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="73b1a-152">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="73b1a-152">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
