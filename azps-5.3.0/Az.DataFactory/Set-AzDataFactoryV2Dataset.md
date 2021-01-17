---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472637"
---
# <span data-ttu-id="3717f-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3717f-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="3717f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3717f-102">SYNOPSIS</span></span>
<span data-ttu-id="3717f-103">Erstellt ein Dataset in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3717f-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="3717f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3717f-104">SYNTAX</span></span>

### <span data-ttu-id="3717f-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3717f-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3717f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3717f-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3717f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3717f-107">DESCRIPTION</span></span>
<span data-ttu-id="3717f-108">Das Set-AzDataFactoryV2Dataset cmdlet erstellt ein Dataset in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3717f-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="3717f-109">Wenn Sie einen Namen für ein bereits vorhandenes Dataset angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor das Dataset ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="3717f-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="3717f-110">Wenn Sie den Parameter "Force" angeben, ersetzt das Cmdlet das vorhandene Dataset ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="3717f-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="3717f-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus: -- Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="3717f-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="3717f-112">- Verknüpfte Dienste erstellen.</span><span class="sxs-lookup"><span data-stu-id="3717f-112">-- Create linked services.</span></span>
<span data-ttu-id="3717f-113">– Erstellen sie Datasets.</span><span class="sxs-lookup"><span data-stu-id="3717f-113">-- Create datasets.</span></span>
<span data-ttu-id="3717f-114">– Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3717f-114">-- Create a pipeline.</span></span>
<span data-ttu-id="3717f-115">Wenn in der Daten factory bereits ein Dataset mit demselben Namen vorhanden ist, werden Sie von diesem Cmdlet aufgefordert zu bestätigen, ob das vorhandene Dataset mit dem neuen Dataset überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3717f-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="3717f-116">Wenn Sie bestätigen, dass das vorhandene Dataset überschrieben wird, wird auch die Datasetdefinition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3717f-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="3717f-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3717f-117">EXAMPLES</span></span>

### <span data-ttu-id="3717f-118">Beispiel 1: Erstellen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="3717f-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="3717f-119">Dieser Befehl erstellt ein Dataset namens DA_WikipediaClickEvents in der Daten factory namens WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3717f-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="3717f-120">Der Befehl basiert auf Informationen im Dataset, DAWikipediaClickEvents.jsdateibasiert sind.</span><span class="sxs-lookup"><span data-stu-id="3717f-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="3717f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3717f-121">PARAMETERS</span></span>

### <span data-ttu-id="3717f-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3717f-122">-DataFactoryName</span></span>
<span data-ttu-id="3717f-123">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="3717f-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3717f-124">Dieses Cmdlet erstellt ein Dataset in der Daten factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3717f-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3717f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3717f-125">-DefaultProfile</span></span>
<span data-ttu-id="3717f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3717f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3717f-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3717f-127">-DefinitionFile</span></span>
<span data-ttu-id="3717f-128">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="3717f-128">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3717f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="3717f-129">-Force</span></span>
<span data-ttu-id="3717f-130">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="3717f-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3717f-131">-Name</span><span class="sxs-lookup"><span data-stu-id="3717f-131">-Name</span></span>
<span data-ttu-id="3717f-132">Gibt den Namen des zu erstellenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="3717f-132">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3717f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3717f-133">-ResourceGroupName</span></span>
<span data-ttu-id="3717f-134">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3717f-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3717f-135">Dieses Cmdlet erstellt ein Dataset in der Gruppe, das von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3717f-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3717f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3717f-136">-ResourceId</span></span>
<span data-ttu-id="3717f-137">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3717f-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3717f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3717f-138">-Confirm</span></span>
<span data-ttu-id="3717f-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3717f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3717f-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3717f-140">-WhatIf</span></span>
<span data-ttu-id="3717f-141">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3717f-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3717f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3717f-142">CommonParameters</span></span>
<span data-ttu-id="3717f-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3717f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3717f-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3717f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3717f-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3717f-145">INPUTS</span></span>

### <span data-ttu-id="3717f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="3717f-146">System.String</span></span>

## <span data-ttu-id="3717f-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3717f-147">OUTPUTS</span></span>

### <span data-ttu-id="3717f-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="3717f-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="3717f-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3717f-149">NOTES</span></span>
<span data-ttu-id="3717f-150">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="3717f-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3717f-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3717f-151">RELATED LINKS</span></span>

[<span data-ttu-id="3717f-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3717f-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="3717f-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3717f-153">Remove-AzDataFactoryV2Dataset</span></span>]()
