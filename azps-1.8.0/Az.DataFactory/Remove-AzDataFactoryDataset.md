---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: ac17206073ff9992c8569da884d1d53c385bccbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661340"
---
# <span data-ttu-id="07af3-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="07af3-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="07af3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07af3-102">SYNOPSIS</span></span>
<span data-ttu-id="07af3-103">Entfernt ein DataSet aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="07af3-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="07af3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07af3-104">SYNTAX</span></span>

### <span data-ttu-id="07af3-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="07af3-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07af3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="07af3-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07af3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07af3-107">DESCRIPTION</span></span>
<span data-ttu-id="07af3-108">Das Cmdlet **Remove-AzDataFactoryDataset** entfernt ein DataSet aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="07af3-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="07af3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07af3-109">EXAMPLES</span></span>

### <span data-ttu-id="07af3-110">Beispiel 1: Entfernen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="07af3-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="07af3-111">Dieser Befehl entfernt das DataSet mit dem Namen DAWikiAggregatedData aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="07af3-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="07af3-112">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="07af3-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="07af3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="07af3-113">PARAMETERS</span></span>

### <span data-ttu-id="07af3-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="07af3-114">-DataFactory</span></span>
<span data-ttu-id="07af3-115">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="07af3-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="07af3-116">Dieses Cmdlet entfernt ein DataSet aus der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="07af3-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="07af3-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="07af3-117">-DataFactoryName</span></span>
<span data-ttu-id="07af3-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="07af3-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="07af3-119">Dieses Cmdlet entfernt ein DataSet aus der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="07af3-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="07af3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07af3-120">-DefaultProfile</span></span>
<span data-ttu-id="07af3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="07af3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07af3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="07af3-122">-Force</span></span>
<span data-ttu-id="07af3-123">Gibt an, dass dieses Cmdlet ein Dataset entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="07af3-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="07af3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="07af3-124">-Name</span></span>
<span data-ttu-id="07af3-125">Gibt den Namen des zu entfernenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="07af3-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="07af3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07af3-126">-ResourceGroupName</span></span>
<span data-ttu-id="07af3-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="07af3-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="07af3-128">Mit diesem Cmdlet wird ein DataSet aus der Gruppe entfernt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="07af3-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="07af3-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07af3-129">-Confirm</span></span>
<span data-ttu-id="07af3-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07af3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07af3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07af3-131">-WhatIf</span></span>
<span data-ttu-id="07af3-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07af3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07af3-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07af3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07af3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07af3-134">CommonParameters</span></span>
<span data-ttu-id="07af3-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07af3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07af3-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07af3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07af3-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07af3-137">INPUTS</span></span>

### <span data-ttu-id="07af3-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="07af3-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="07af3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="07af3-139">System.String</span></span>

## <span data-ttu-id="07af3-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07af3-140">OUTPUTS</span></span>

### <span data-ttu-id="07af3-141">System. void</span><span class="sxs-lookup"><span data-stu-id="07af3-141">System.Void</span></span>

## <span data-ttu-id="07af3-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="07af3-142">NOTES</span></span>
* <span data-ttu-id="07af3-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="07af3-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="07af3-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07af3-144">RELATED LINKS</span></span>

[<span data-ttu-id="07af3-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="07af3-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="07af3-146">Neu – AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="07af3-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


