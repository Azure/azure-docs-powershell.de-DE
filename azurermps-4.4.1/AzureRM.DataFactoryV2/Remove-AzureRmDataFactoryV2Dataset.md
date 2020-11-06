---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 77cb56c08e29bd209ccf53fcdee42545b774c650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502750"
---
# <span data-ttu-id="662fd-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="662fd-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="662fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="662fd-102">SYNOPSIS</span></span>
<span data-ttu-id="662fd-103">Entfernt ein DataSet aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="662fd-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="662fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="662fd-104">SYNTAX</span></span>

### <span data-ttu-id="662fd-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="662fd-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="662fd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="662fd-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="662fd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="662fd-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="662fd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="662fd-108">DESCRIPTION</span></span>
<span data-ttu-id="662fd-109">Das Remove-AzureRmDataFactoryV2Dataset-Cmdlet entfernt ein DataSet aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="662fd-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="662fd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="662fd-110">EXAMPLES</span></span>

### <span data-ttu-id="662fd-111">Beispiel 1: Entfernen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="662fd-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="662fd-112">Dieser Befehl entfernt das DataSet mit dem Namen DAWikiAggregatedData aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="662fd-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="662fd-113">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="662fd-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="662fd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="662fd-114">PARAMETERS</span></span>

### <span data-ttu-id="662fd-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="662fd-115">-Confirm</span></span>
<span data-ttu-id="662fd-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="662fd-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="662fd-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="662fd-117">-DataFactoryName</span></span>
<span data-ttu-id="662fd-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="662fd-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="662fd-119">Dieses Cmdlet entfernt ein DataSet aus der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="662fd-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="662fd-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="662fd-120">-InputObject</span></span>
<span data-ttu-id="662fd-121">Gibt ein zu entfernendes DataSet-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="662fd-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="662fd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="662fd-122">-Force</span></span>
<span data-ttu-id="662fd-123">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="662fd-123">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="662fd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="662fd-124">-Name</span></span>
<span data-ttu-id="662fd-125">Gibt den Namen des zu entfernenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="662fd-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662fd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="662fd-126">-ResourceGroupName</span></span>
<span data-ttu-id="662fd-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="662fd-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="662fd-128">Mit diesem Cmdlet wird ein DataSet aus der Gruppe entfernt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="662fd-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="662fd-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="662fd-129">-ResourceId</span></span>
<span data-ttu-id="662fd-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="662fd-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="662fd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="662fd-131">-WhatIf</span></span>
<span data-ttu-id="662fd-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="662fd-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="662fd-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="662fd-133">INPUTS</span></span>

### <span data-ttu-id="662fd-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="662fd-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="662fd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="662fd-135">System.String</span></span>


## <span data-ttu-id="662fd-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="662fd-136">OUTPUTS</span></span>

### <span data-ttu-id="662fd-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="662fd-137">System.Object</span></span>

## <span data-ttu-id="662fd-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="662fd-138">NOTES</span></span>
<span data-ttu-id="662fd-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="662fd-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="662fd-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="662fd-140">RELATED LINKS</span></span>
[<span data-ttu-id="662fd-141">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="662fd-141">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="662fd-142">Satz-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="662fd-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()
