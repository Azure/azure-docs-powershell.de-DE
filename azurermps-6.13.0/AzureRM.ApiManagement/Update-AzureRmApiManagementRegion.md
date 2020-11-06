---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: ed26538e54cef189837bd36bf9e6f561df3541f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478009"
---
# <span data-ttu-id="827f5-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="827f5-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="827f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="827f5-102">SYNOPSIS</span></span>
<span data-ttu-id="827f5-103">Aktualisiert den vorhandenen Bereitstellungsbereich in PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="827f5-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="827f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="827f5-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="827f5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="827f5-105">DESCRIPTION</span></span>
<span data-ttu-id="827f5-106">Das Cmdlet **Update-AzureRmApiManagementRegion** aktualisiert eine vorhandene Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** in einer Sammlung von **AdditionalRegions** -Objekten einer bereitgestellten Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="827f5-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="827f5-107">Dieses Cmdlet stellt nichts bereit, sondern aktualisiert eine Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="827f5-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="827f5-108">Verwenden Sie zum Aktualisieren einer Bereitstellung einer API-Verwaltung das geänderte **PsApiManagementInstance** -Cmdlet für das Update-AzureRmApiManagementDeployment-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="827f5-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="827f5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="827f5-109">EXAMPLES</span></span>

## <span data-ttu-id="827f5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="827f5-110">PARAMETERS</span></span>

### <span data-ttu-id="827f5-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="827f5-111">-ApiManagement</span></span>
<span data-ttu-id="827f5-112">Gibt die **PsApiManagement** -Instanz an, in der ein vorhandener Bereitstellungsbereich aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="827f5-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="827f5-113">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="827f5-113">-Capacity</span></span>
<span data-ttu-id="827f5-114">Gibt den neuen SKU-Kapazitätswert für den Bereitstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="827f5-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="827f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827f5-115">-DefaultProfile</span></span>
<span data-ttu-id="827f5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="827f5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="827f5-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="827f5-117">-Location</span></span>
<span data-ttu-id="827f5-118">Gibt den Speicherort des Bereitstellungsbereichs an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="827f5-118">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="827f5-119">Gibt den Speicherort des neuen Bereitstellungsbereichs zwischen dem unterstützten Bereich für den API-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="827f5-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="827f5-120">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="827f5-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="827f5-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="827f5-121">-Sku</span></span>
<span data-ttu-id="827f5-122">Gibt den neuen Stufenwert für den Bereitstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="827f5-122">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="827f5-123">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="827f5-123">Valid values are:</span></span>
- <span data-ttu-id="827f5-124">Entwickler</span><span class="sxs-lookup"><span data-stu-id="827f5-124">Developer</span></span>
- <span data-ttu-id="827f5-125">Standard</span><span class="sxs-lookup"><span data-stu-id="827f5-125">Standard</span></span>
- <span data-ttu-id="827f5-126">Premium</span><span class="sxs-lookup"><span data-stu-id="827f5-126">Premium</span></span>

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

### <span data-ttu-id="827f5-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="827f5-127">-VirtualNetwork</span></span>
<span data-ttu-id="827f5-128">Gibt eine virtuelle Netzwerkkonfiguration für den Bereitstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="827f5-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="827f5-129">Durch Übergabe von $NULL wird die Konfiguration des virtuellen Netzwerks für den Bereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="827f5-129">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="827f5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827f5-130">CommonParameters</span></span>
<span data-ttu-id="827f5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="827f5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827f5-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="827f5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827f5-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="827f5-133">INPUTS</span></span>

### <span data-ttu-id="827f5-134">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="827f5-134">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="827f5-135">Parameter: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="827f5-135">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="827f5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="827f5-136">System.String</span></span>

### <span data-ttu-id="827f5-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="827f5-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="827f5-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="827f5-138">System.Int32</span></span>

### <span data-ttu-id="827f5-139">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="827f5-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="827f5-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="827f5-140">OUTPUTS</span></span>

### <span data-ttu-id="827f5-141">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="827f5-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="827f5-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="827f5-142">NOTES</span></span>

## <span data-ttu-id="827f5-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="827f5-143">RELATED LINKS</span></span>

[<span data-ttu-id="827f5-144">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="827f5-144">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="827f5-145">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="827f5-145">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="827f5-146">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="827f5-146">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
