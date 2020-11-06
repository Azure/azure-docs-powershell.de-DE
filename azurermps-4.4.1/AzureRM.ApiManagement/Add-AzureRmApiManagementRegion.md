---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503321"
---
# <span data-ttu-id="9a5c8-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9a5c8-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="9a5c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5c8-103">Fügt neue Bereitstellungsbereiche zu einer PsApiManagement-Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a5c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a5c8-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a5c8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="9a5c8-106">Das **Add-AzureRmApiManagementRegion-** Cmdlet fügt der Sammlung von **AdditionalRegions** der bereitgestellten Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement** eine neue Instanz des Typs **PsApiManagementRegion** hinzu.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="9a5c8-107">Dieses Cmdlet stellt nichts für sich bereit, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="9a5c8-108">Um eine Bereitstellung einer API-Verwaltung zu aktualisieren, übergeben Sie die geänderte **PsApiManagement** -Instanz an Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="9a5c8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a5c8-109">EXAMPLES</span></span>

### <span data-ttu-id="9a5c8-110">Beispiel 1: Hinzufügen neuer Bereitstellungsbereiche zu einer PsApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="9a5c8-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="9a5c8-111">Dieser Befehl addiert zwei Premium-SKU-Einheiten und die Region "East US" zur **PsApiManagement** -Instanz.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="9a5c8-112">Beispiel 2: Hinzufügen neuer Bereitstellungsbereiche zu einer PsApiManagement-Instanz und anschließendes Aktualisieren der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="9a5c8-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="9a5c8-113">Dieser Befehl ruft ein **PsApiManagement** -Objekt ab, addiert zwei Premium-SKU-Einheiten für die Region mit dem Namen East US und aktualisiert dann die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="9a5c8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a5c8-114">PARAMETERS</span></span>

### <span data-ttu-id="9a5c8-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a5c8-115">-ApiManagement</span></span>
<span data-ttu-id="9a5c8-116">Gibt die **PsApiManagement** -Instanz an, der dieses Cmdlet zusätzliche Bereitstellungsbereiche hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="9a5c8-117">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="9a5c8-117">-Capacity</span></span>
<span data-ttu-id="9a5c8-118">Gibt die SKU-Kapazität des Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="9a5c8-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="9a5c8-119">-Location</span></span>
<span data-ttu-id="9a5c8-120">Gibt den Speicherort des neuen Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-120">Specifies the location of the new deployment region.</span></span>

<span data-ttu-id="9a5c8-121">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9a5c8-121">Valid values are:</span></span> 

- <span data-ttu-id="9a5c8-122">Nord-Zentral-USA</span><span class="sxs-lookup"><span data-stu-id="9a5c8-122">North Central US</span></span>
- <span data-ttu-id="9a5c8-123">Süd-Mittelamerika</span><span class="sxs-lookup"><span data-stu-id="9a5c8-123">South Central US</span></span>
- <span data-ttu-id="9a5c8-124">Zentral-US</span><span class="sxs-lookup"><span data-stu-id="9a5c8-124">Central US</span></span>
- <span data-ttu-id="9a5c8-125">West Europa</span><span class="sxs-lookup"><span data-stu-id="9a5c8-125">West Europe</span></span>
- <span data-ttu-id="9a5c8-126">Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="9a5c8-126">North Europe</span></span>
- <span data-ttu-id="9a5c8-127">West-US</span><span class="sxs-lookup"><span data-stu-id="9a5c8-127">West US</span></span>
- <span data-ttu-id="9a5c8-128">East US</span><span class="sxs-lookup"><span data-stu-id="9a5c8-128">East US</span></span>
- <span data-ttu-id="9a5c8-129">East US 2</span><span class="sxs-lookup"><span data-stu-id="9a5c8-129">East US 2</span></span>
- <span data-ttu-id="9a5c8-130">Japan (Ost)</span><span class="sxs-lookup"><span data-stu-id="9a5c8-130">Japan East</span></span>
- <span data-ttu-id="9a5c8-131">Japan West</span><span class="sxs-lookup"><span data-stu-id="9a5c8-131">Japan West</span></span>
- <span data-ttu-id="9a5c8-132">Brasilien Süd</span><span class="sxs-lookup"><span data-stu-id="9a5c8-132">Brazil South</span></span>
- <span data-ttu-id="9a5c8-133">Südostasien</span><span class="sxs-lookup"><span data-stu-id="9a5c8-133">Southeast Asia</span></span>
- <span data-ttu-id="9a5c8-134">Ostasien</span><span class="sxs-lookup"><span data-stu-id="9a5c8-134">East Asia</span></span>
- <span data-ttu-id="9a5c8-135">Australien (Ost)</span><span class="sxs-lookup"><span data-stu-id="9a5c8-135">Australia East</span></span>
- <span data-ttu-id="9a5c8-136">Australien südöstlich</span><span class="sxs-lookup"><span data-stu-id="9a5c8-136">Australia Southeast</span></span>

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

### <span data-ttu-id="9a5c8-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="9a5c8-137">-Sku</span></span>
<span data-ttu-id="9a5c8-138">Gibt die Ebene des Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-138">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="9a5c8-139">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9a5c8-139">Valid values are:</span></span> 

- <span data-ttu-id="9a5c8-140">Entwickler</span><span class="sxs-lookup"><span data-stu-id="9a5c8-140">Developer</span></span>
- <span data-ttu-id="9a5c8-141">Standard</span><span class="sxs-lookup"><span data-stu-id="9a5c8-141">Standard</span></span>
- <span data-ttu-id="9a5c8-142">Premium</span><span class="sxs-lookup"><span data-stu-id="9a5c8-142">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5c8-143">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9a5c8-143">-VirtualNetwork</span></span>
<span data-ttu-id="9a5c8-144">Gibt eine virtuelle Netzwerkkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-144">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="9a5c8-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5c8-145">-DefaultProfile</span></span>
<span data-ttu-id="9a5c8-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a5c8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5c8-147">CommonParameters</span></span>
<span data-ttu-id="9a5c8-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5c8-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a5c8-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5c8-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a5c8-150">INPUTS</span></span>

### <span data-ttu-id="9a5c8-151">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a5c8-151">PsApiManagement</span></span>
<span data-ttu-id="9a5c8-152">Der Parameter "ApiManagement" akzeptiert den Wert vom Typ "PsApiManagement" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-152">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="9a5c8-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a5c8-153">OUTPUTS</span></span>

### <span data-ttu-id="9a5c8-154">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9a5c8-154">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9a5c8-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a5c8-155">NOTES</span></span>
* <span data-ttu-id="9a5c8-156">Das Cmdlet schreibt eine aktualisierte **PsApiManagement** -Instanz in Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a5c8-156">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="9a5c8-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a5c8-157">RELATED LINKS</span></span>

[<span data-ttu-id="9a5c8-158">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9a5c8-158">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="9a5c8-159">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9a5c8-159">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="9a5c8-160">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="9a5c8-160">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


