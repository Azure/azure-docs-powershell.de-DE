---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 7db88488ccf60865654169233bb19025eae080d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372292"
---
# <span data-ttu-id="9df74-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9df74-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="9df74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9df74-102">SYNOPSIS</span></span>
<span data-ttu-id="9df74-103">Entfernt ein Dataset aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9df74-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="9df74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9df74-104">SYNTAX</span></span>

### <span data-ttu-id="9df74-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9df74-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9df74-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9df74-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9df74-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9df74-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9df74-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9df74-108">DESCRIPTION</span></span>
<span data-ttu-id="9df74-109">Das Remove-AzDataFactoryV2Dataset cmdlet entfernt ein Dataset aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9df74-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="9df74-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9df74-110">EXAMPLES</span></span>

### <span data-ttu-id="9df74-111">Beispiel 1: Entfernen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="9df74-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="9df74-112">Mit diesem Befehl wird das Dataset mit dem Namen DAWikiAggregatedData aus der Daten factory namens WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="9df74-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="9df74-113">Der Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="9df74-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="9df74-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9df74-114">PARAMETERS</span></span>

### <span data-ttu-id="9df74-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9df74-115">-DataFactoryName</span></span>
<span data-ttu-id="9df74-116">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="9df74-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9df74-117">Dieses Cmdlet entfernt ein Dataset aus der Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9df74-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9df74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df74-118">-DefaultProfile</span></span>
<span data-ttu-id="9df74-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9df74-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9df74-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9df74-120">-Force</span></span>
<span data-ttu-id="9df74-121">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="9df74-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9df74-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9df74-122">-InputObject</span></span>
<span data-ttu-id="9df74-123">Gibt ein zu entfernende Dataset-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9df74-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9df74-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9df74-124">-Name</span></span>
<span data-ttu-id="9df74-125">Gibt den Namen des zu entfernenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="9df74-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df74-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9df74-126">-ResourceGroupName</span></span>
<span data-ttu-id="9df74-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9df74-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9df74-128">Dieses Cmdlet entfernt ein Dataset aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9df74-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9df74-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9df74-129">-ResourceId</span></span>
<span data-ttu-id="9df74-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9df74-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df74-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9df74-131">-Confirm</span></span>
<span data-ttu-id="9df74-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9df74-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df74-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9df74-133">-WhatIf</span></span>
<span data-ttu-id="9df74-134">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9df74-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df74-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df74-135">CommonParameters</span></span>
<span data-ttu-id="9df74-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9df74-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df74-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9df74-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df74-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9df74-138">INPUTS</span></span>

### <span data-ttu-id="9df74-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="9df74-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="9df74-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9df74-140">System.String</span></span>

## <span data-ttu-id="9df74-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9df74-141">OUTPUTS</span></span>

### <span data-ttu-id="9df74-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="9df74-142">System.Void</span></span>

## <span data-ttu-id="9df74-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9df74-143">NOTES</span></span>
<span data-ttu-id="9df74-144">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="9df74-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9df74-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9df74-145">RELATED LINKS</span></span>

[<span data-ttu-id="9df74-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9df74-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="9df74-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9df74-147">Set-AzDataFactoryV2Dataset</span></span>]()
