---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ccd7379a07b83b3ed45eff5f8095b950868810c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663714"
---
# <span data-ttu-id="a6af7-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a6af7-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="a6af7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6af7-102">SYNOPSIS</span></span>
<span data-ttu-id="a6af7-103">Entfernt einen vorhandenen Bereitstellungsbereich aus der PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="a6af7-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6af7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6af7-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6af7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6af7-105">DESCRIPTION</span></span>
<span data-ttu-id="a6af7-106">Das Cmdlet **Remove-AzureRmApiManagementRegion** entfernt eine Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** aus einer Sammlung von **AdditionalRegions** , die die Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement** bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="a6af7-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="a6af7-107">Dieses Cmdlet ändert die Bereitstellung nicht selbst, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a6af7-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="a6af7-108">Wenn Sie eine Bereitstellung einer API-Verwaltung aktualisieren möchten, übergeben Sie den geänderten **PsApiManagementInstance** an **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="a6af7-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="a6af7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6af7-109">EXAMPLES</span></span>

### <span data-ttu-id="a6af7-110">Beispiel 1: Entfernen eines Bereichs aus einer PsApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="a6af7-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="a6af7-111">Mit diesem Befehl wird die Region East US aus der **PsApiManagement** -Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="a6af7-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="a6af7-112">Beispiel 2: Entfernen eines Bereichs aus einer PsApiManagement-Instanz mithilfe einer Reihe von Befehlen</span><span class="sxs-lookup"><span data-stu-id="a6af7-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="a6af7-113">Dieser erste Befehl ruft eine Instanz von **PsApiManagement** aus der Ressourcengruppe namens Contoso mit dem Namen ContosoApi ab.</span><span class="sxs-lookup"><span data-stu-id="a6af7-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="a6af7-114">Der endgültige Befehl entfernt dann die Region mit dem Namen East US aus dieser Instanz und aktualisiert dann die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="a6af7-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="a6af7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6af7-115">PARAMETERS</span></span>

### <span data-ttu-id="a6af7-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6af7-116">-ApiManagement</span></span>
<span data-ttu-id="a6af7-117">Gibt die **PsApiManagement** -Instanz an, aus der dieses Cmdlet den zusätzlichen Bereitstellungsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="a6af7-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="a6af7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6af7-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="a6af7-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="a6af7-119">-Location</span></span>
<span data-ttu-id="a6af7-120">Gibt den Speicherort des Bereichs an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="a6af7-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="a6af7-121">Gibt den Speicherort des neuen Bereitstellungsbereichs zwischen dem unterstützten Bereich für den API-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="a6af7-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="a6af7-122">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="a6af7-122">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="a6af7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6af7-123">CommonParameters</span></span>
<span data-ttu-id="a6af7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6af7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6af7-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6af7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6af7-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6af7-126">INPUTS</span></span>

### <span data-ttu-id="a6af7-127">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6af7-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="a6af7-128">Parameter: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a6af7-128">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="a6af7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a6af7-129">System.String</span></span>

## <span data-ttu-id="a6af7-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6af7-130">OUTPUTS</span></span>

### <span data-ttu-id="a6af7-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a6af7-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a6af7-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6af7-132">NOTES</span></span>

## <span data-ttu-id="a6af7-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6af7-133">RELATED LINKS</span></span>

[<span data-ttu-id="a6af7-134">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a6af7-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="a6af7-135">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a6af7-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


