---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472665"
---
# <span data-ttu-id="14999-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="14999-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="14999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14999-102">SYNOPSIS</span></span>
<span data-ttu-id="14999-103">Erstellt ein Dataset in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="14999-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="14999-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14999-104">SYNTAX</span></span>

### <span data-ttu-id="14999-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="14999-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14999-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="14999-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14999-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14999-107">DESCRIPTION</span></span>
<span data-ttu-id="14999-108">Das **Cmdlet "New-AzDataFactoryDataset"** erstellt ein Dataset in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="14999-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="14999-109">Wenn Sie einen Namen für ein bereits vorhandenes Dataset angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor das Dataset ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="14999-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="14999-110">Wenn Sie den Parameter *"Force"* angeben, ersetzt das Cmdlet das vorhandene Dataset ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="14999-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="14999-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="14999-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="14999-112">Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="14999-112">Create a data factory.</span></span> 
- <span data-ttu-id="14999-113">Erstellen verknüpfter Dienste</span><span class="sxs-lookup"><span data-stu-id="14999-113">Create linked services.</span></span> 
- <span data-ttu-id="14999-114">Erstellen sie Datasets.</span><span class="sxs-lookup"><span data-stu-id="14999-114">Create datasets.</span></span> 
- <span data-ttu-id="14999-115">Erstellen sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="14999-115">Create a pipeline.</span></span>
<span data-ttu-id="14999-116">Wenn in der Daten factory bereits ein Dataset mit demselben Namen vorhanden ist, werden Sie von diesem Cmdlet aufgefordert zu bestätigen, ob das vorhandene Dataset mit dem neuen Dataset überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="14999-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="14999-117">Wenn Sie bestätigen, dass das vorhandene Dataset überschrieben wird, wird auch die Datasetdefinition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="14999-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="14999-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14999-118">EXAMPLES</span></span>

### <span data-ttu-id="14999-119">Beispiel 1: Erstellen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="14999-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="14999-120">Dieser Befehl erstellt ein Dataset namens DA_WikipediaClickEvents in der Daten factory namens WikiADF.</span><span class="sxs-lookup"><span data-stu-id="14999-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="14999-121">Der Befehl basiert auf Informationen im Dataset, DAWikipediaClickEvents.jsdateibasiert sind.</span><span class="sxs-lookup"><span data-stu-id="14999-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="14999-122">Beispiel 2: Anzeigen der Verfügbarkeit eines neuen Datasets</span><span class="sxs-lookup"><span data-stu-id="14999-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="14999-123">Der erste Befehl erstellt wie im vorherigen Beispiel ein Dataset namens DA_WikipediaClickEvents und weist dieses Dataset dann der Variablen $Dataset zu.</span><span class="sxs-lookup"><span data-stu-id="14999-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="14999-124">Der zweite Befehl verwendet die standardmäßige Punktformatierung, um Details zur Verfügbarkeitseigenschaft des Datasets anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="14999-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="14999-125">Beispiel 3: Anzeigen des Speicherorts für ein neues Dataset</span><span class="sxs-lookup"><span data-stu-id="14999-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="14999-126">Der erste Befehl erstellt wie im vorherigen Beispiel ein Dataset namens DA_WikipediaClickEvents und weist dieses Dataset dann der Variablen $Dataset zu.</span><span class="sxs-lookup"><span data-stu-id="14999-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="14999-127">Der zweite Befehl zeigt Details zur Eigenschaft "Location" des Datasets an.</span><span class="sxs-lookup"><span data-stu-id="14999-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="14999-128">Beispiel 4: Anzeigen von Gültigkeitsprüfungsregeln für ein neues Dataset</span><span class="sxs-lookup"><span data-stu-id="14999-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="14999-129">Der erste Befehl erstellt wie im vorherigen Beispiel ein Dataset namens DA_WikipediaClickEvents und weist dieses Dataset dann der Variablen $Dataset zu.</span><span class="sxs-lookup"><span data-stu-id="14999-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="14999-130">Der zweite Befehl ruft Details zu den Gültigkeitsprüfungsregeln für das Dataset ab und übergibt sie dann mithilfe des Pipelineoperators Format-List an das cmdlet "Format-List".</span><span class="sxs-lookup"><span data-stu-id="14999-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="14999-131">Auf Windows PowerShell cmdlet werden die Ergebnisse formatiert.</span><span class="sxs-lookup"><span data-stu-id="14999-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="14999-132">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Format-List` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="14999-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="14999-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14999-133">PARAMETERS</span></span>

### <span data-ttu-id="14999-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="14999-134">-DataFactory</span></span>
<span data-ttu-id="14999-135">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="14999-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="14999-136">Dieses Cmdlet erstellt ein Dataset in der Daten factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="14999-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="14999-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="14999-137">-DataFactoryName</span></span>
<span data-ttu-id="14999-138">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="14999-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="14999-139">Dieses Cmdlet erstellt ein Dataset in der Daten factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="14999-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="14999-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14999-140">-DefaultProfile</span></span>
<span data-ttu-id="14999-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="14999-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14999-142">-File</span><span class="sxs-lookup"><span data-stu-id="14999-142">-File</span></span>
<span data-ttu-id="14999-143">Gibt den vollständigen Pfad der JavaScript Object Notation (JSON)-Datei an, die die Beschreibung des Datasets enthält.</span><span class="sxs-lookup"><span data-stu-id="14999-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14999-144">-Force</span><span class="sxs-lookup"><span data-stu-id="14999-144">-Force</span></span>
<span data-ttu-id="14999-145">Gibt an, dass dieses Cmdlet ein vorhandenes Dataset ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="14999-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="14999-146">-Name</span><span class="sxs-lookup"><span data-stu-id="14999-146">-Name</span></span>
<span data-ttu-id="14999-147">Gibt den Namen des zu erstellenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="14999-147">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14999-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14999-148">-ResourceGroupName</span></span>
<span data-ttu-id="14999-149">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="14999-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="14999-150">Dieses Cmdlet erstellt ein Dataset in der Gruppe, das von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="14999-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="14999-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14999-151">-Confirm</span></span>
<span data-ttu-id="14999-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14999-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14999-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="14999-153">-WhatIf</span></span>
<span data-ttu-id="14999-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14999-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14999-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14999-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14999-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14999-156">CommonParameters</span></span>
<span data-ttu-id="14999-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14999-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14999-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14999-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14999-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14999-159">INPUTS</span></span>

### <span data-ttu-id="14999-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="14999-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="14999-161">System.String</span><span class="sxs-lookup"><span data-stu-id="14999-161">System.String</span></span>

## <span data-ttu-id="14999-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14999-162">OUTPUTS</span></span>

### <span data-ttu-id="14999-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="14999-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="14999-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="14999-164">NOTES</span></span>
* <span data-ttu-id="14999-165">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="14999-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="14999-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="14999-166">RELATED LINKS</span></span>

[<span data-ttu-id="14999-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="14999-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="14999-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="14999-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


