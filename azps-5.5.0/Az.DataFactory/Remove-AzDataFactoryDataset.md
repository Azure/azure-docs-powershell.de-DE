---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153489"
---
# <span data-ttu-id="a1898-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="a1898-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="a1898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1898-102">SYNOPSIS</span></span>
<span data-ttu-id="a1898-103">Entfernt ein Dataset aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a1898-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="a1898-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1898-104">SYNTAX</span></span>

### <span data-ttu-id="a1898-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1898-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1898-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a1898-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1898-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1898-107">DESCRIPTION</span></span>
<span data-ttu-id="a1898-108">Das **Cmdlet "Remove-AzDataFactoryDataset"** entfernt ein Dataset aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a1898-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="a1898-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a1898-109">EXAMPLES</span></span>

### <span data-ttu-id="a1898-110">Beispiel 1: Entfernen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="a1898-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="a1898-111">Mit diesem Befehl wird das Dataset mit dem Namen DAWikiAggregatedData aus der Daten factory namens WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="a1898-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="a1898-112">Der Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="a1898-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="a1898-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1898-113">PARAMETERS</span></span>

### <span data-ttu-id="a1898-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a1898-114">-DataFactory</span></span>
<span data-ttu-id="a1898-115">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="a1898-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a1898-116">Dieses Cmdlet entfernt ein Dataset aus der Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a1898-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1898-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a1898-117">-DataFactoryName</span></span>
<span data-ttu-id="a1898-118">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="a1898-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a1898-119">Dieses Cmdlet entfernt ein Dataset aus der Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a1898-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1898-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1898-120">-DefaultProfile</span></span>
<span data-ttu-id="a1898-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a1898-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1898-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a1898-122">-Force</span></span>
<span data-ttu-id="a1898-123">Gibt an, dass mit diesem Cmdlet ein Dataset entfernt wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="a1898-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a1898-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a1898-124">-Name</span></span>
<span data-ttu-id="a1898-125">Gibt den Namen des zu entfernenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="a1898-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="a1898-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1898-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1898-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a1898-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a1898-128">Dieses Cmdlet entfernt ein Dataset aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a1898-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1898-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1898-129">-Confirm</span></span>
<span data-ttu-id="a1898-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1898-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1898-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a1898-131">-WhatIf</span></span>
<span data-ttu-id="a1898-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1898-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1898-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1898-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1898-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1898-134">CommonParameters</span></span>
<span data-ttu-id="a1898-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1898-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1898-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1898-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1898-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a1898-137">INPUTS</span></span>

### <span data-ttu-id="a1898-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a1898-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a1898-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a1898-139">System.String</span></span>

## <span data-ttu-id="a1898-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a1898-140">OUTPUTS</span></span>

### <span data-ttu-id="a1898-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="a1898-141">System.Void</span></span>

## <span data-ttu-id="a1898-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a1898-142">NOTES</span></span>
* <span data-ttu-id="a1898-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="a1898-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a1898-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a1898-144">RELATED LINKS</span></span>

[<span data-ttu-id="a1898-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="a1898-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="a1898-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="a1898-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


