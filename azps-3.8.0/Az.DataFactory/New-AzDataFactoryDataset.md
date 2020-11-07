---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847236"
---
# <span data-ttu-id="3c560-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3c560-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="3c560-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c560-102">SYNOPSIS</span></span>
<span data-ttu-id="3c560-103">Erstellt ein Dataset in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3c560-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="3c560-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c560-104">SYNTAX</span></span>

### <span data-ttu-id="3c560-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c560-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c560-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3c560-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c560-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c560-107">DESCRIPTION</span></span>
<span data-ttu-id="3c560-108">Das Cmdlet **New-AzDataFactoryDataset** erstellt ein Dataset in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3c560-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="3c560-109">Wenn Sie einen Namen für ein DataSet angeben, das bereits vorhanden ist, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor das DataSet ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="3c560-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="3c560-110">Wenn Sie den Parameter *Force* angeben, wird das vorhandene DataSet ohne Bestätigung durch das Cmdlet ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3c560-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="3c560-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="3c560-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="3c560-112">Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3c560-112">Create a data factory.</span></span> 
- <span data-ttu-id="3c560-113">Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="3c560-113">Create linked services.</span></span> 
- <span data-ttu-id="3c560-114">Erstellen von Datasets</span><span class="sxs-lookup"><span data-stu-id="3c560-114">Create datasets.</span></span> 
- <span data-ttu-id="3c560-115">Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3c560-115">Create a pipeline.</span></span>
<span data-ttu-id="3c560-116">Wenn bereits ein DataSet mit dem gleichen Namen in der Data Factory vorhanden ist, werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, ob das vorhandene DataSet mit dem neuen DataSet überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c560-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="3c560-117">Wenn Sie bestätigen, dass das vorhandene DataSet überschrieben werden soll, wird auch die DataSet-Definition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3c560-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="3c560-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c560-118">EXAMPLES</span></span>

### <span data-ttu-id="3c560-119">Beispiel 1: Erstellen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="3c560-119">Example 1: Create a dataset</span></span>
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

<span data-ttu-id="3c560-120">Dieser Befehl erstellt ein DataSet mit dem Namen DA_WikipediaClickEvents in der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3c560-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="3c560-121">Der Befehl unterstützt das Dataset auf Informationen in der DAWikipediaClickEvents.jsfür die Datei.</span><span class="sxs-lookup"><span data-stu-id="3c560-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="3c560-122">Beispiel 2: Anzeigen der Verfügbarkeit eines neuen Datasets</span><span class="sxs-lookup"><span data-stu-id="3c560-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="3c560-123">Der erste Befehl erstellt ein DataSet mit dem Namen DA_WikipediaClickEvents, wie in einem vorherigen Beispiel, und weist dann das DataSet der $DataSet Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="3c560-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="3c560-124">Der zweite Befehl verwendet die standardmäßige Punktnotation, um Details zur Verfügbarkeits Eigenschaft des Datasets anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3c560-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="3c560-125">Beispiel 3: Anzeigen des Speicherorts für ein neues DataSet</span><span class="sxs-lookup"><span data-stu-id="3c560-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="3c560-126">Der erste Befehl erstellt ein DataSet mit dem Namen DA_WikipediaClickEvents, wie in einem vorherigen Beispiel, und weist dann das DataSet der $DataSet Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="3c560-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="3c560-127">Der zweite Befehl zeigt Details zur Location-Eigenschaft des Datasets an.</span><span class="sxs-lookup"><span data-stu-id="3c560-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="3c560-128">Beispiel 4: Anzeigen von Gültigkeitsprüfungsregeln für ein neues DataSet</span><span class="sxs-lookup"><span data-stu-id="3c560-128">Example 4: View validation rules for a new dataset</span></span>
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

<span data-ttu-id="3c560-129">Der erste Befehl erstellt ein DataSet mit dem Namen DA_WikipediaClickEvents, wie in einem vorherigen Beispiel, und weist dann das DataSet der $DataSet Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="3c560-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="3c560-130">Der zweite Befehl ruft Details zu den Gültigkeitsprüfungsregeln für das DataSet ab und übergibt diese dann mithilfe des Pipelineoperators an das Format-List-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c560-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3c560-131">Das Windows PowerShell-Cmdlet formatiert die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="3c560-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="3c560-132">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="3c560-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="3c560-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c560-133">PARAMETERS</span></span>

### <span data-ttu-id="3c560-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3c560-134">-DataFactory</span></span>
<span data-ttu-id="3c560-135">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3c560-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3c560-136">Dieses Cmdlet erstellt ein Dataset in der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3c560-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c560-137">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3c560-137">-DataFactoryName</span></span>
<span data-ttu-id="3c560-138">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="3c560-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3c560-139">Dieses Cmdlet erstellt ein Dataset in der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3c560-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c560-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c560-140">-DefaultProfile</span></span>
<span data-ttu-id="3c560-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3c560-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c560-142">-Datei</span><span class="sxs-lookup"><span data-stu-id="3c560-142">-File</span></span>
<span data-ttu-id="3c560-143">Gibt den vollständigen Pfad der JSON-Datei (JavaScript Object Notation) an, die die Beschreibung des Datasets enthält.</span><span class="sxs-lookup"><span data-stu-id="3c560-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

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

### <span data-ttu-id="3c560-144">-Force</span><span class="sxs-lookup"><span data-stu-id="3c560-144">-Force</span></span>
<span data-ttu-id="3c560-145">Gibt an, dass dieses Cmdlet ein vorhandenes Dataset ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="3c560-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3c560-146">-Name</span><span class="sxs-lookup"><span data-stu-id="3c560-146">-Name</span></span>
<span data-ttu-id="3c560-147">Gibt den Namen des zu erstellenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="3c560-147">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="3c560-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c560-148">-ResourceGroupName</span></span>
<span data-ttu-id="3c560-149">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3c560-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3c560-150">Mit diesem Cmdlet wird ein Dataset in der Gruppe erstellt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3c560-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3c560-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c560-151">-Confirm</span></span>
<span data-ttu-id="3c560-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c560-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c560-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c560-153">-WhatIf</span></span>
<span data-ttu-id="3c560-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c560-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c560-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c560-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c560-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c560-156">CommonParameters</span></span>
<span data-ttu-id="3c560-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c560-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c560-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c560-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c560-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c560-159">INPUTS</span></span>

### <span data-ttu-id="3c560-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3c560-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="3c560-161">System. String</span><span class="sxs-lookup"><span data-stu-id="3c560-161">System.String</span></span>

## <span data-ttu-id="3c560-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c560-162">OUTPUTS</span></span>

### <span data-ttu-id="3c560-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="3c560-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="3c560-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c560-164">NOTES</span></span>
* <span data-ttu-id="3c560-165">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="3c560-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3c560-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c560-166">RELATED LINKS</span></span>

[<span data-ttu-id="3c560-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3c560-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="3c560-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3c560-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


