---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: fff6145adaa909bcadde90f36802072b812ba0ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004364"
---
# <span data-ttu-id="21943-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="21943-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="21943-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21943-102">SYNOPSIS</span></span>
<span data-ttu-id="21943-103">Aktualisiert den vorhandenen Bereitstellungsbereich in PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="21943-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="21943-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21943-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21943-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21943-105">DESCRIPTION</span></span>
<span data-ttu-id="21943-106">Das Cmdlet **Update-AzApiManagementRegion** aktualisiert eine vorhandene Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** in einer Sammlung von **AdditionalRegions** -Objekten einer bereitgestellten Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="21943-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="21943-107">Dieses Cmdlet stellt nichts bereit, sondern aktualisiert eine Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="21943-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="21943-108">Verwenden Sie zum Aktualisieren einer Bereitstellung einer API-Verwaltung das geänderte **PsApiManagementInstance** -Cmdlet für das Set-AzApiManagement-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21943-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="21943-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21943-109">EXAMPLES</span></span>

### <span data-ttu-id="21943-110">Beispiel 1: erhöht die Kapazität des zusätzlichen Bereichs in einer PsApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="21943-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="21943-111">Dieser Befehl ruft den API-Management-Premium-SKU-Dienst ab, wobei Regionen in Süd-Zentralamerika und Nord-Zentralamerika enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="21943-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="21943-112">Sie erhöht dann die Kapazität der Nord zentralen US-Region auf 2 mit dem **AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="21943-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="21943-113">Das nächste Cmdlet **-Satz-AzApiManagement** wendet die Konfigurationsänderung auf den API-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="21943-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="21943-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="21943-114">PARAMETERS</span></span>

### <span data-ttu-id="21943-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="21943-115">-ApiManagement</span></span>
<span data-ttu-id="21943-116">Gibt die **PsApiManagement** -Instanz an, in der ein vorhandener Bereitstellungsbereich aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="21943-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="21943-117">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="21943-117">-Capacity</span></span>
<span data-ttu-id="21943-118">Gibt den neuen SKU-Kapazitätswert für den Bereitstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="21943-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="21943-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21943-119">-DefaultProfile</span></span>
<span data-ttu-id="21943-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21943-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21943-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="21943-121">-Location</span></span>
<span data-ttu-id="21943-122">Gibt den Speicherort des Bereitstellungsbereichs an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="21943-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="21943-123">Gibt den Speicherort des neuen Bereitstellungsbereichs zwischen dem unterstützten Bereich für den API-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="21943-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="21943-124">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="21943-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="21943-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="21943-125">-Sku</span></span>
<span data-ttu-id="21943-126">Gibt den neuen Stufenwert für den Bereitstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="21943-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="21943-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="21943-127">Valid values are:</span></span>
- <span data-ttu-id="21943-128">Entwickler</span><span class="sxs-lookup"><span data-stu-id="21943-128">Developer</span></span>
- <span data-ttu-id="21943-129">Standard</span><span class="sxs-lookup"><span data-stu-id="21943-129">Standard</span></span>
- <span data-ttu-id="21943-130">Premium</span><span class="sxs-lookup"><span data-stu-id="21943-130">Premium</span></span>

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

### <span data-ttu-id="21943-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="21943-131">-VirtualNetwork</span></span>
<span data-ttu-id="21943-132">Gibt eine virtuelle Netzwerkkonfiguration für den Bereitstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="21943-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="21943-133">Durch Übergabe von $NULL wird die Konfiguration des virtuellen Netzwerks für den Bereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="21943-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="21943-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21943-134">CommonParameters</span></span>
<span data-ttu-id="21943-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21943-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21943-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21943-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21943-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21943-137">INPUTS</span></span>

### <span data-ttu-id="21943-138">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="21943-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="21943-139">System. String</span><span class="sxs-lookup"><span data-stu-id="21943-139">System.String</span></span>

### <span data-ttu-id="21943-140">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="21943-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="21943-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="21943-141">System.Int32</span></span>

### <span data-ttu-id="21943-142">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="21943-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="21943-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21943-143">OUTPUTS</span></span>

### <span data-ttu-id="21943-144">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="21943-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="21943-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="21943-145">NOTES</span></span>

## <span data-ttu-id="21943-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21943-146">RELATED LINKS</span></span>

[<span data-ttu-id="21943-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="21943-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="21943-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="21943-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="21943-149">Satz-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="21943-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
