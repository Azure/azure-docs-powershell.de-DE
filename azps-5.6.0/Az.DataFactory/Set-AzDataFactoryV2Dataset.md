---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5ea766b4c35e23a62a0764320a2f0491ea151586
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946193"
---
# <span data-ttu-id="62416-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="62416-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="62416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62416-102">SYNOPSIS</span></span>
<span data-ttu-id="62416-103">Erstellt ein Dataset in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="62416-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="62416-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62416-104">SYNTAX</span></span>

### <span data-ttu-id="62416-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="62416-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62416-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="62416-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62416-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62416-107">DESCRIPTION</span></span>
<span data-ttu-id="62416-108">Das Set-AzDataFactoryV2Dataset-Cmdlet erstellt ein Dataset in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="62416-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="62416-109">Wenn Sie einen Namen für ein bereits vorhandenes Dataset angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es das Dataset ersetzt.</span><span class="sxs-lookup"><span data-stu-id="62416-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="62416-110">Wenn Sie den Parameter Erzwingen angeben, ersetzt das Cmdlet das vorhandene Dataset ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="62416-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="62416-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus: -- Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="62416-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="62416-112">-- Erstellen sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="62416-112">-- Create linked services.</span></span>
<span data-ttu-id="62416-113">- Erstellen Sie Datasets.</span><span class="sxs-lookup"><span data-stu-id="62416-113">-- Create datasets.</span></span>
<span data-ttu-id="62416-114">- Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="62416-114">-- Create a pipeline.</span></span>
<span data-ttu-id="62416-115">Wenn in der Daten factory bereits ein Dataset mit demselben Namen vorhanden ist, werden Sie in diesem Cmdlet aufgefordert zu bestätigen, ob das vorhandene Dataset mit dem neuen Dataset überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="62416-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="62416-116">Wenn Sie bestätigen, dass das vorhandene Dataset überschrieben wird, wird auch die Datasetdefinition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="62416-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="62416-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="62416-117">EXAMPLES</span></span>

### <span data-ttu-id="62416-118">Beispiel 1: Erstellen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="62416-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="62416-119">Mit diesem Befehl wird ein Dataset DA_WikipediaClickEvents in der Daten factory mit dem Namen WikiADF erstellt.</span><span class="sxs-lookup"><span data-stu-id="62416-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="62416-120">Der Befehl basiert auf Informationen in DAWikipediaClickEvents.jsDatei.</span><span class="sxs-lookup"><span data-stu-id="62416-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="62416-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="62416-121">PARAMETERS</span></span>

### <span data-ttu-id="62416-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="62416-122">-DataFactoryName</span></span>
<span data-ttu-id="62416-123">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="62416-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="62416-124">Dieses Cmdlet erstellt ein Dataset in der Daten factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="62416-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="62416-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62416-125">-DefaultProfile</span></span>
<span data-ttu-id="62416-126">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62416-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62416-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="62416-127">-DefinitionFile</span></span>
<span data-ttu-id="62416-128">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="62416-128">The JSON file path.</span></span>

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

### <span data-ttu-id="62416-129">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="62416-129">-Force</span></span>
<span data-ttu-id="62416-130">Führt das Cmdlet aus, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="62416-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="62416-131">-Name</span><span class="sxs-lookup"><span data-stu-id="62416-131">-Name</span></span>
<span data-ttu-id="62416-132">Gibt den Namen des zu erstellenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="62416-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="62416-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62416-133">-ResourceGroupName</span></span>
<span data-ttu-id="62416-134">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="62416-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="62416-135">Dieses Cmdlet erstellt ein Dataset in der Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="62416-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="62416-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62416-136">-ResourceId</span></span>
<span data-ttu-id="62416-137">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="62416-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="62416-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="62416-138">-Confirm</span></span>
<span data-ttu-id="62416-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62416-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62416-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62416-140">-WhatIf</span></span>
<span data-ttu-id="62416-141">Zeigt, was geschieht, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62416-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="62416-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62416-142">CommonParameters</span></span>
<span data-ttu-id="62416-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62416-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62416-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62416-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62416-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="62416-145">INPUTS</span></span>

### <span data-ttu-id="62416-146">System.String</span><span class="sxs-lookup"><span data-stu-id="62416-146">System.String</span></span>

## <span data-ttu-id="62416-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="62416-147">OUTPUTS</span></span>

### <span data-ttu-id="62416-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="62416-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="62416-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="62416-149">NOTES</span></span>
<span data-ttu-id="62416-150">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="62416-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="62416-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="62416-151">RELATED LINKS</span></span>

[<span data-ttu-id="62416-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="62416-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="62416-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="62416-153">Remove-AzDataFactoryV2Dataset</span></span>]()
