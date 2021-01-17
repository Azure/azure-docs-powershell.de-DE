---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381925"
---
# <span data-ttu-id="860ba-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="860ba-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="860ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="860ba-102">SYNOPSIS</span></span>
<span data-ttu-id="860ba-103">Entfernt einen vorhandenen Bereitstellungsbereich aus der PsApiManagement-Instanz.</span><span class="sxs-lookup"><span data-stu-id="860ba-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="860ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="860ba-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="860ba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="860ba-105">DESCRIPTION</span></span>
<span data-ttu-id="860ba-106">Mit dem Cmdlet **"Remove-AzApiManagementRegion"** wird eine Instanz des Typs **"Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion"** aus einer Sammlung von **"AdditionalRegions"** der bereitgestellten Instanz des Typs **"Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement"** entfernt.</span><span class="sxs-lookup"><span data-stu-id="860ba-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="860ba-107">Dieses Cmdlet ändert die Bereitstellung nicht allein, sondern aktualisiert die Instanz von **PsApiManagement** im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="860ba-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="860ba-108">Um eine Bereitstellung einer API Management zu aktualisieren, übergeben Sie die geänderte **"PsApiManagementInstance"** an **Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="860ba-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="860ba-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="860ba-109">EXAMPLES</span></span>

### <span data-ttu-id="860ba-110">Beispiel 1: Entfernen einer Region aus einer Instanz "PsApiManagement"</span><span class="sxs-lookup"><span data-stu-id="860ba-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="860ba-111">Mit diesem Befehl wird die Region "Ost US" aus der Instanz **"PsApiManagement"** entfernt.</span><span class="sxs-lookup"><span data-stu-id="860ba-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="860ba-112">Beispiel 2: Entfernen einer Region aus einer "PsApiManagement"-Instanz mithilfe einer Reihe von Befehlen</span><span class="sxs-lookup"><span data-stu-id="860ba-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="860ba-113">Dieser erste Befehl ruft eine Instanz von **"PsApiManagement" aus** der Ressourcengruppe "Contoso" namens "ContosoApi" ab.</span><span class="sxs-lookup"><span data-stu-id="860ba-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="860ba-114">Der letzte Befehl entfernt dann die Region mit dem Namen "OST US" aus dieser Instanz und aktualisiert dann die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="860ba-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="860ba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="860ba-115">PARAMETERS</span></span>

### <span data-ttu-id="860ba-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="860ba-116">-ApiManagement</span></span>
<span data-ttu-id="860ba-117">Gibt die **Instanz "PsApiManagement"** an, aus der dieses Cmdlet den zusätzlichen Bereitstellungsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="860ba-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="860ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860ba-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="860ba-119">-Location</span><span class="sxs-lookup"><span data-stu-id="860ba-119">-Location</span></span>
<span data-ttu-id="860ba-120">Gibt den Speicherort der Region an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="860ba-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="860ba-121">Gibt den Speicherort der neuen Bereitstellungsregion unter der unterstützten Region für den Api-Verwaltungsdienst an.</span><span class="sxs-lookup"><span data-stu-id="860ba-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="860ba-122">Verwenden Sie zum Abrufen gültiger Speicherorte das Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | dabei {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object von Speicherorten</span><span class="sxs-lookup"><span data-stu-id="860ba-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="860ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860ba-123">CommonParameters</span></span>
<span data-ttu-id="860ba-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="860ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860ba-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="860ba-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860ba-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="860ba-126">INPUTS</span></span>

### <span data-ttu-id="860ba-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="860ba-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="860ba-128">System.String</span><span class="sxs-lookup"><span data-stu-id="860ba-128">System.String</span></span>

## <span data-ttu-id="860ba-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="860ba-129">OUTPUTS</span></span>

### <span data-ttu-id="860ba-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="860ba-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="860ba-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="860ba-131">NOTES</span></span>

## <span data-ttu-id="860ba-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="860ba-132">RELATED LINKS</span></span>

[<span data-ttu-id="860ba-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="860ba-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="860ba-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="860ba-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


