---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477386"
---
# <span data-ttu-id="f480b-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f480b-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="f480b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f480b-102">SYNOPSIS</span></span>
<span data-ttu-id="f480b-103">Aktualisiert den vorhandenen Bereitstellungsbereich in PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="f480b-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f480b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f480b-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f480b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f480b-105">DESCRIPTION</span></span>
<span data-ttu-id="f480b-106">Das Cmdlet **Update-AzureRmApiManagementRegion** aktualisiert eine vorhandene Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** in einer Sammlung von **AdditionalRegions** -Objekten einer bereitgestellten Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="f480b-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="f480b-107">Dieses Cmdlet stellt nichts bereit, sondern aktualisiert eine Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f480b-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="f480b-108">Verwenden Sie zum Aktualisieren einer Bereitstellung einer API-Verwaltung das geänderte **PsApiManagementInstance** -Cmdlet für das Update-AzureRmApiManagementDeployment-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f480b-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="f480b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f480b-109">EXAMPLES</span></span>

## <span data-ttu-id="f480b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f480b-110">PARAMETERS</span></span>

### <span data-ttu-id="f480b-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f480b-111">-ApiManagement</span></span>
<span data-ttu-id="f480b-112">Gibt die **PsApiManagement** -Instanz an, in der ein vorhandener Bereitstellungsbereich aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f480b-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="f480b-113">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="f480b-113">-Capacity</span></span>
<span data-ttu-id="f480b-114">Gibt den neuen SKU-Kapazitätswert für den Bereitstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="f480b-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="f480b-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="f480b-115">-Location</span></span>
<span data-ttu-id="f480b-116">Gibt den Speicherort des Bereitstellungsbereichs an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f480b-116">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="f480b-117">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f480b-117">Valid values are:</span></span>

- <span data-ttu-id="f480b-118">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="f480b-118">North Central US</span></span>
- <span data-ttu-id="f480b-119">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="f480b-119">South Central US</span></span>
- <span data-ttu-id="f480b-120">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="f480b-120">Central US</span></span>
- <span data-ttu-id="f480b-121">West Europa</span><span class="sxs-lookup"><span data-stu-id="f480b-121">West Europe</span></span>
- <span data-ttu-id="f480b-122">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="f480b-122">North Europe</span></span>
- <span data-ttu-id="f480b-123">West-US</span><span class="sxs-lookup"><span data-stu-id="f480b-123">West US</span></span>
- <span data-ttu-id="f480b-124">East US</span><span class="sxs-lookup"><span data-stu-id="f480b-124">East US</span></span>
- <span data-ttu-id="f480b-125">East US 2</span><span class="sxs-lookup"><span data-stu-id="f480b-125">East US 2</span></span>
- <span data-ttu-id="f480b-126">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="f480b-126">Japan East</span></span>
- <span data-ttu-id="f480b-127">Japan West</span><span class="sxs-lookup"><span data-stu-id="f480b-127">Japan West</span></span>
- <span data-ttu-id="f480b-128">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="f480b-128">Brazil South</span></span>
- <span data-ttu-id="f480b-129">Südostasien</span><span class="sxs-lookup"><span data-stu-id="f480b-129">Southeast Asia</span></span>
- <span data-ttu-id="f480b-130">Ostasien</span><span class="sxs-lookup"><span data-stu-id="f480b-130">East Asia</span></span>
- <span data-ttu-id="f480b-131">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="f480b-131">Australia East</span></span>
- <span data-ttu-id="f480b-132">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="f480b-132">Australia Southeast</span></span>

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

### <span data-ttu-id="f480b-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="f480b-133">-Sku</span></span>
<span data-ttu-id="f480b-134">Gibt den neuen Stufenwert für den Bereitstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="f480b-134">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="f480b-135">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f480b-135">Valid values are:</span></span>

- <span data-ttu-id="f480b-136">Entwickler</span><span class="sxs-lookup"><span data-stu-id="f480b-136">Developer</span></span>
- <span data-ttu-id="f480b-137">Standard</span><span class="sxs-lookup"><span data-stu-id="f480b-137">Standard</span></span>
- <span data-ttu-id="f480b-138">Premium</span><span class="sxs-lookup"><span data-stu-id="f480b-138">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f480b-139">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f480b-139">-VirtualNetwork</span></span>
<span data-ttu-id="f480b-140">Gibt eine virtuelle Netzwerkkonfiguration für den Bereitstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="f480b-140">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="f480b-141">Durch Übergabe von $NULL wird die Konfiguration des virtuellen Netzwerks für den Bereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="f480b-141">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="f480b-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f480b-142">-DefaultProfile</span></span>
<span data-ttu-id="f480b-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f480b-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f480b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f480b-144">CommonParameters</span></span>
<span data-ttu-id="f480b-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f480b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f480b-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f480b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f480b-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f480b-147">INPUTS</span></span>

### <span data-ttu-id="f480b-148">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f480b-148">PsApiManagement</span></span>
<span data-ttu-id="f480b-149">Der Parameter "ApiManagement" akzeptiert den Wert vom Typ "PsApiManagement" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f480b-149">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="f480b-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f480b-150">OUTPUTS</span></span>

### <span data-ttu-id="f480b-151">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="f480b-151">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f480b-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="f480b-152">NOTES</span></span>

## <span data-ttu-id="f480b-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f480b-153">RELATED LINKS</span></span>

[<span data-ttu-id="f480b-154">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f480b-154">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="f480b-155">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f480b-155">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="f480b-156">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f480b-156">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
