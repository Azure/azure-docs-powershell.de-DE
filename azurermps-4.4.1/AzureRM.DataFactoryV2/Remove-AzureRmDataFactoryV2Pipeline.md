---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: cc43b2982ff2269a1e0e72da065a806895cc798e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505986"
---
# <span data-ttu-id="a9c03-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a9c03-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="a9c03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9c03-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c03-103">Entfernt eine Pipeline aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a9c03-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9c03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9c03-104">SYNTAX</span></span>

### <span data-ttu-id="a9c03-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9c03-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a9c03-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a9c03-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a9c03-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9c03-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a9c03-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9c03-108">DESCRIPTION</span></span>
<span data-ttu-id="a9c03-109">Das Remove-AzureRmDataFactoryV2Pipeline-Cmdlet entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a9c03-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="a9c03-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9c03-110">EXAMPLES</span></span>

### <span data-ttu-id="a9c03-111">Beispiel 1: Entfernen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="a9c03-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="a9c03-112">Dieses Cmdlet entfernt die Pipeline mit dem Namen DPWikisample aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a9c03-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="a9c03-113">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="a9c03-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="a9c03-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9c03-114">PARAMETERS</span></span>

### <span data-ttu-id="a9c03-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9c03-115">-Confirm</span></span>
<span data-ttu-id="a9c03-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9c03-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c03-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a9c03-117">-DataFactoryName</span></span>
<span data-ttu-id="a9c03-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="a9c03-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a9c03-119">Dieses Cmdlet entfernt eine Pipeline aus der Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a9c03-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c03-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a9c03-120">-Force</span></span>
<span data-ttu-id="a9c03-121">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="a9c03-121">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c03-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a9c03-122">-Name</span></span>
<span data-ttu-id="a9c03-123">Gibt den Namen der zu entfernenden Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="a9c03-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c03-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9c03-124">-InputObject</span></span>
<span data-ttu-id="a9c03-125">Gibt ein Pipeline Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a9c03-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="a9c03-126">Dieses Cmdlet entfernt die von diesem Parameter festgelegte Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9c03-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c03-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c03-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9c03-128">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a9c03-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a9c03-129">Dieses Cmdlet entfernt eine Pipeline aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a9c03-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c03-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a9c03-130">-ResourceId</span></span>
<span data-ttu-id="a9c03-131">Die Azure-Ressourcen-ID der zu entfernenden Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9c03-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c03-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c03-132">-WhatIf</span></span>
<span data-ttu-id="a9c03-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9c03-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a9c03-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9c03-134">INPUTS</span></span>

### <span data-ttu-id="a9c03-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="a9c03-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="a9c03-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a9c03-136">System.String</span></span>


## <span data-ttu-id="a9c03-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9c03-137">OUTPUTS</span></span>

### <span data-ttu-id="a9c03-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="a9c03-138">System.Object</span></span>

## <span data-ttu-id="a9c03-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9c03-139">NOTES</span></span>
<span data-ttu-id="a9c03-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="a9c03-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a9c03-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9c03-141">RELATED LINKS</span></span>
[<span data-ttu-id="a9c03-142">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a9c03-142">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a9c03-143">Satz-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a9c03-143">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a9c03-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a9c03-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

