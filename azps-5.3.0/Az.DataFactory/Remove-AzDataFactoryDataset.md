---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470560"
---
# <span data-ttu-id="0894a-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="0894a-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="0894a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0894a-102">SYNOPSIS</span></span>
<span data-ttu-id="0894a-103">Entfernt ein Dataset aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0894a-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="0894a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0894a-104">SYNTAX</span></span>

### <span data-ttu-id="0894a-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0894a-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0894a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0894a-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0894a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0894a-107">DESCRIPTION</span></span>
<span data-ttu-id="0894a-108">Das **Cmdlet "Remove-AzDataFactoryDataset"** entfernt ein Dataset aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0894a-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="0894a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0894a-109">EXAMPLES</span></span>

### <span data-ttu-id="0894a-110">Beispiel 1: Entfernen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="0894a-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="0894a-111">Mit diesem Befehl wird das Dataset mit dem Namen DAWikiAggregatedData aus der Daten factory namens WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="0894a-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="0894a-112">Der Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="0894a-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="0894a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0894a-113">PARAMETERS</span></span>

### <span data-ttu-id="0894a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0894a-114">-DataFactory</span></span>
<span data-ttu-id="0894a-115">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="0894a-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0894a-116">Dieses Cmdlet entfernt ein Dataset aus der Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0894a-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0894a-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0894a-117">-DataFactoryName</span></span>
<span data-ttu-id="0894a-118">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="0894a-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0894a-119">Dieses Cmdlet entfernt ein Dataset aus der Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0894a-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0894a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0894a-120">-DefaultProfile</span></span>
<span data-ttu-id="0894a-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0894a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0894a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0894a-122">-Force</span></span>
<span data-ttu-id="0894a-123">Zeigt an, dass mit diesem Cmdlet ein Dataset entfernt wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0894a-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0894a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0894a-124">-Name</span></span>
<span data-ttu-id="0894a-125">Gibt den Namen des zu entfernenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="0894a-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0894a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0894a-126">-ResourceGroupName</span></span>
<span data-ttu-id="0894a-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0894a-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0894a-128">Dieses Cmdlet entfernt ein Dataset aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0894a-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0894a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0894a-129">-Confirm</span></span>
<span data-ttu-id="0894a-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0894a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0894a-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0894a-131">-WhatIf</span></span>
<span data-ttu-id="0894a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0894a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0894a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0894a-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0894a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0894a-134">CommonParameters</span></span>
<span data-ttu-id="0894a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0894a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0894a-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0894a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0894a-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0894a-137">INPUTS</span></span>

### <span data-ttu-id="0894a-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0894a-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="0894a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0894a-139">System.String</span></span>

## <span data-ttu-id="0894a-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0894a-140">OUTPUTS</span></span>

### <span data-ttu-id="0894a-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="0894a-141">System.Void</span></span>

## <span data-ttu-id="0894a-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0894a-142">NOTES</span></span>
* <span data-ttu-id="0894a-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="0894a-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0894a-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0894a-144">RELATED LINKS</span></span>

[<span data-ttu-id="0894a-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="0894a-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="0894a-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="0894a-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


