---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ea4b734eba1ed1a37a72e756c32acc3d6ad2a32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498558"
---
# <span data-ttu-id="e99d5-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e99d5-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="e99d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e99d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e99d5-103">Fügt neue Bereitstellungsbereiche zu einer PsApiManagement-Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="e99d5-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e99d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e99d5-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e99d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e99d5-105">DESCRIPTION</span></span>
<span data-ttu-id="e99d5-106">Das **Add-AzureRmApiManagementRegion-** Cmdlet fügt der Sammlung von **AdditionalRegions** der bereitgestellten Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement** eine neue Instanz des Typs **PsApiManagementRegion** hinzu.</span><span class="sxs-lookup"><span data-stu-id="e99d5-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="e99d5-107">Dieses Cmdlet stellt nichts für sich bereit, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e99d5-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="e99d5-108">Um eine Bereitstellung einer API-Verwaltung zu aktualisieren, übergeben Sie die geänderte **PsApiManagement** -Instanz an Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="e99d5-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="e99d5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e99d5-109">EXAMPLES</span></span>

### <span data-ttu-id="e99d5-110">Beispiel 1: Hinzufügen neuer Bereitstellungsbereiche zu einer PsApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="e99d5-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="e99d5-111">Dieser Befehl addiert zwei Premium-SKU-Einheiten und die Region "East US" zur **PsApiManagement** -Instanz.</span><span class="sxs-lookup"><span data-stu-id="e99d5-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="e99d5-112">Beispiel 2: Hinzufügen neuer Bereitstellungsbereiche zu einer PsApiManagement-Instanz und anschließendes Aktualisieren der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="e99d5-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="e99d5-113">Dieser Befehl ruft ein **PsApiManagement** -Objekt ab, addiert zwei Premium-SKU-Einheiten für die Region mit dem Namen East US und aktualisiert dann die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="e99d5-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="e99d5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e99d5-114">PARAMETERS</span></span>

### <span data-ttu-id="e99d5-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e99d5-115">-ApiManagement</span></span>
<span data-ttu-id="e99d5-116">Gibt die **PsApiManagement** -Instanz an, der dieses Cmdlet zusätzliche Bereitstellungsbereiche hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="e99d5-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="e99d5-117">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="e99d5-117">-Capacity</span></span>
<span data-ttu-id="e99d5-118">Gibt die SKU-Kapazität des Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="e99d5-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="e99d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99d5-119">-DefaultProfile</span></span>
<span data-ttu-id="e99d5-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e99d5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e99d5-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="e99d5-121">-Location</span></span>
<span data-ttu-id="e99d5-122">Gibt den Speicherort des neuen Bereitstellungsbereichs zwischen dem unterstützten Bereich für den API-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="e99d5-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="e99d5-123">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="e99d5-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="e99d5-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="e99d5-124">-Sku</span></span>
<span data-ttu-id="e99d5-125">Gibt die Ebene des Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="e99d5-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="e99d5-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="e99d5-126">Valid values are:</span></span> 
- <span data-ttu-id="e99d5-127">Entwickler</span><span class="sxs-lookup"><span data-stu-id="e99d5-127">Developer</span></span>
- <span data-ttu-id="e99d5-128">Standard</span><span class="sxs-lookup"><span data-stu-id="e99d5-128">Standard</span></span>
- <span data-ttu-id="e99d5-129">Premium</span><span class="sxs-lookup"><span data-stu-id="e99d5-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e99d5-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e99d5-130">-VirtualNetwork</span></span>
<span data-ttu-id="e99d5-131">Gibt eine virtuelle Netzwerkkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="e99d5-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="e99d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99d5-132">CommonParameters</span></span>
<span data-ttu-id="e99d5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e99d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99d5-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e99d5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99d5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e99d5-135">INPUTS</span></span>

### <span data-ttu-id="e99d5-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e99d5-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="e99d5-137">Parameter: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e99d5-137">Parameters: ApiManagement (ByValue)</span></span>

## <span data-ttu-id="e99d5-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e99d5-138">OUTPUTS</span></span>

### <span data-ttu-id="e99d5-139">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e99d5-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e99d5-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="e99d5-140">NOTES</span></span>
* <span data-ttu-id="e99d5-141">Das Cmdlet schreibt eine aktualisierte **PsApiManagement** -Instanz in Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e99d5-141">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="e99d5-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e99d5-142">RELATED LINKS</span></span>

[<span data-ttu-id="e99d5-143">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e99d5-143">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="e99d5-144">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e99d5-144">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="e99d5-145">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="e99d5-145">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


