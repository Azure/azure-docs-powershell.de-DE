---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009467"
---
# <span data-ttu-id="cb927-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="cb927-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="cb927-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb927-102">SYNOPSIS</span></span>
<span data-ttu-id="cb927-103">Fügt neue Bereitstellungsbereiche zu einer PsApiManagement-Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb927-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="cb927-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb927-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb927-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb927-105">DESCRIPTION</span></span>
<span data-ttu-id="cb927-106">Das **Add-AzApiManagementRegion-** Cmdlet fügt der Sammlung von **AdditionalRegions** der bereitgestellten Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement** eine neue Instanz des Typs **PsApiManagementRegion** hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb927-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="cb927-107">Dieses Cmdlet stellt nichts für sich bereit, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cb927-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="cb927-108">Wenn Sie eine Bereitstellung einer API-Verwaltung aktualisieren möchten, übergeben Sie die geänderte **PsApiManagement** -Instanz an "AzApiManagement".</span><span class="sxs-lookup"><span data-stu-id="cb927-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="cb927-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb927-109">EXAMPLES</span></span>

### <span data-ttu-id="cb927-110">Beispiel 1: Hinzufügen neuer Bereitstellungsbereiche zu einer PsApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="cb927-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="cb927-111">Dieser Befehl addiert zwei Premium-SKU-Einheiten und die Region "East US" zur **PsApiManagement** -Instanz.</span><span class="sxs-lookup"><span data-stu-id="cb927-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="cb927-112">Beispiel 2: Hinzufügen neuer Bereitstellungsbereiche zu einer PsApiManagement-Instanz und anschließendes Aktualisieren der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="cb927-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="cb927-113">Dieser Befehl ruft ein **PsApiManagement** -Objekt ab, addiert zwei Premium-SKU-Einheiten für die Region mit dem Namen East US und aktualisiert dann die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="cb927-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="cb927-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb927-114">PARAMETERS</span></span>

### <span data-ttu-id="cb927-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb927-115">-ApiManagement</span></span>
<span data-ttu-id="cb927-116">Gibt die **PsApiManagement** -Instanz an, der dieses Cmdlet zusätzliche Bereitstellungsbereiche hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="cb927-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="cb927-117">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="cb927-117">-Capacity</span></span>
<span data-ttu-id="cb927-118">Gibt die SKU-Kapazität des Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="cb927-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="cb927-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb927-119">-DefaultProfile</span></span>
<span data-ttu-id="cb927-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb927-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb927-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="cb927-121">-Location</span></span>
<span data-ttu-id="cb927-122">Gibt den Speicherort des neuen Bereitstellungsbereichs zwischen dem unterstützten Bereich für den API-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="cb927-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="cb927-123">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="cb927-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="cb927-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="cb927-124">-Sku</span></span>
<span data-ttu-id="cb927-125">Gibt die Ebene des Bereitstellungsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="cb927-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="cb927-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="cb927-126">Valid values are:</span></span> 
- <span data-ttu-id="cb927-127">Entwickler</span><span class="sxs-lookup"><span data-stu-id="cb927-127">Developer</span></span>
- <span data-ttu-id="cb927-128">Standard</span><span class="sxs-lookup"><span data-stu-id="cb927-128">Standard</span></span>
- <span data-ttu-id="cb927-129">Premium</span><span class="sxs-lookup"><span data-stu-id="cb927-129">Premium</span></span>

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

### <span data-ttu-id="cb927-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cb927-130">-VirtualNetwork</span></span>
<span data-ttu-id="cb927-131">Gibt eine virtuelle Netzwerkkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="cb927-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="cb927-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb927-132">CommonParameters</span></span>
<span data-ttu-id="cb927-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb927-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb927-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb927-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb927-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb927-135">INPUTS</span></span>

### <span data-ttu-id="cb927-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb927-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="cb927-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb927-137">OUTPUTS</span></span>

### <span data-ttu-id="cb927-138">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb927-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="cb927-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb927-139">NOTES</span></span>
* <span data-ttu-id="cb927-140">Das Cmdlet schreibt eine aktualisierte **PsApiManagement** -Instanz in Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb927-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="cb927-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb927-141">RELATED LINKS</span></span>

[<span data-ttu-id="cb927-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="cb927-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="cb927-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="cb927-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="cb927-144">Satz-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb927-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


