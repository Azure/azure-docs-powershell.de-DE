---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: ca40a9b74dd92b7bcdecdde87e4763f044b3272f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658173"
---
# <span data-ttu-id="bc9e8-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="bc9e8-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="bc9e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc9e8-102">SYNOPSIS</span></span>
<span data-ttu-id="bc9e8-103">Entfernt einen vorhandenen Bereitstellungsbereich aus der PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="bc9e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc9e8-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc9e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc9e8-105">DESCRIPTION</span></span>
<span data-ttu-id="bc9e8-106">Das Cmdlet **Remove-AzApiManagementRegion** entfernt eine Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** aus einer Sammlung von **AdditionalRegions** , die die Instanz des Typs **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement** bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="bc9e8-107">Dieses Cmdlet ändert die Bereitstellung nicht selbst, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="bc9e8-108">Wenn Sie eine Bereitstellung einer API-Verwaltung aktualisieren möchten, übergeben Sie den geänderten **PsApiManagementInstance** an **AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="bc9e8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc9e8-109">EXAMPLES</span></span>

### <span data-ttu-id="bc9e8-110">Beispiel 1: Entfernen eines Bereichs aus einer PsApiManagement-Instanz</span><span class="sxs-lookup"><span data-stu-id="bc9e8-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="bc9e8-111">Mit diesem Befehl wird die Region East US aus der **PsApiManagement** -Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="bc9e8-112">Beispiel 2: Entfernen eines Bereichs aus einer PsApiManagement-Instanz mithilfe einer Reihe von Befehlen</span><span class="sxs-lookup"><span data-stu-id="bc9e8-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="bc9e8-113">Dieser erste Befehl ruft eine Instanz von **PsApiManagement** aus der Ressourcengruppe namens Contoso mit dem Namen ContosoApi ab.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="bc9e8-114">Der endgültige Befehl entfernt dann die Region mit dem Namen East US aus dieser Instanz und aktualisiert dann die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="bc9e8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc9e8-115">PARAMETERS</span></span>

### <span data-ttu-id="bc9e8-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bc9e8-116">-ApiManagement</span></span>
<span data-ttu-id="bc9e8-117">Gibt die **PsApiManagement** -Instanz an, aus der dieses Cmdlet den zusätzlichen Bereitstellungsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="bc9e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc9e8-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="bc9e8-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="bc9e8-119">-Location</span></span>
<span data-ttu-id="bc9e8-120">Gibt den Speicherort des Bereichs an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="bc9e8-121">Gibt den Speicherort des neuen Bereitstellungsbereichs zwischen dem unterstützten Bereich für den API-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="bc9e8-122">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | wobei {$ _. Hilfswerte [0]. "-EQ"-Dienst "} | Select-Object Standorte</span><span class="sxs-lookup"><span data-stu-id="bc9e8-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="bc9e8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc9e8-123">CommonParameters</span></span>
<span data-ttu-id="bc9e8-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc9e8-125">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc9e8-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc9e8-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc9e8-126">INPUTS</span></span>

### <span data-ttu-id="bc9e8-127">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="bc9e8-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="bc9e8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bc9e8-128">System.String</span></span>

## <span data-ttu-id="bc9e8-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc9e8-129">OUTPUTS</span></span>

### <span data-ttu-id="bc9e8-130">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="bc9e8-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="bc9e8-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc9e8-131">NOTES</span></span>

## <span data-ttu-id="bc9e8-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc9e8-132">RELATED LINKS</span></span>

[<span data-ttu-id="bc9e8-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="bc9e8-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="bc9e8-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="bc9e8-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


