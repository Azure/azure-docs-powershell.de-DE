---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847155"
---
# <span data-ttu-id="02a6d-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="02a6d-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="02a6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="02a6d-103">Erstellt ein Dataset in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="02a6d-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="02a6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02a6d-104">SYNTAX</span></span>

### <span data-ttu-id="02a6d-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="02a6d-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02a6d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02a6d-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a6d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02a6d-107">DESCRIPTION</span></span>
<span data-ttu-id="02a6d-108">Das Set-AzDataFactoryV2Dataset-Cmdlet erstellt ein Dataset in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="02a6d-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="02a6d-109">Wenn Sie einen Namen für ein DataSet angeben, das bereits vorhanden ist, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor das DataSet ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="02a6d-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="02a6d-110">Wenn Sie den Parameter Force angeben, wird das vorhandene DataSet ohne Bestätigung durch das Cmdlet ersetzt.</span><span class="sxs-lookup"><span data-stu-id="02a6d-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="02a6d-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:--Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="02a6d-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="02a6d-112">--Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="02a6d-112">-- Create linked services.</span></span>
<span data-ttu-id="02a6d-113">--Erstellen von Datasets.</span><span class="sxs-lookup"><span data-stu-id="02a6d-113">-- Create datasets.</span></span>
<span data-ttu-id="02a6d-114">--Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="02a6d-114">-- Create a pipeline.</span></span>
<span data-ttu-id="02a6d-115">Wenn bereits ein DataSet mit dem gleichen Namen in der Data Factory vorhanden ist, werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, ob das vorhandene DataSet mit dem neuen DataSet überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="02a6d-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="02a6d-116">Wenn Sie bestätigen, dass das vorhandene DataSet überschrieben werden soll, wird auch die DataSet-Definition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="02a6d-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="02a6d-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02a6d-117">EXAMPLES</span></span>

### <span data-ttu-id="02a6d-118">Beispiel 1: Erstellen eines Datasets</span><span class="sxs-lookup"><span data-stu-id="02a6d-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="02a6d-119">Dieser Befehl erstellt ein DataSet mit dem Namen DA_WikipediaClickEvents in der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="02a6d-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="02a6d-120">Der Befehl unterstützt das Dataset auf Informationen in der DAWikipediaClickEvents.jsfür die Datei.</span><span class="sxs-lookup"><span data-stu-id="02a6d-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="02a6d-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="02a6d-121">PARAMETERS</span></span>

### <span data-ttu-id="02a6d-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="02a6d-122">-DataFactoryName</span></span>
<span data-ttu-id="02a6d-123">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="02a6d-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="02a6d-124">Dieses Cmdlet erstellt ein Dataset in der Data Factory, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="02a6d-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="02a6d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a6d-125">-DefaultProfile</span></span>
<span data-ttu-id="02a6d-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02a6d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02a6d-127">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="02a6d-127">-DefinitionFile</span></span>
<span data-ttu-id="02a6d-128">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="02a6d-128">The JSON file path.</span></span>

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

### <span data-ttu-id="02a6d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="02a6d-129">-Force</span></span>
<span data-ttu-id="02a6d-130">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="02a6d-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="02a6d-131">-Name</span><span class="sxs-lookup"><span data-stu-id="02a6d-131">-Name</span></span>
<span data-ttu-id="02a6d-132">Gibt den Namen des zu erstellenden Datasets an.</span><span class="sxs-lookup"><span data-stu-id="02a6d-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="02a6d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a6d-133">-ResourceGroupName</span></span>
<span data-ttu-id="02a6d-134">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="02a6d-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="02a6d-135">Mit diesem Cmdlet wird ein Dataset in der Gruppe erstellt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="02a6d-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="02a6d-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="02a6d-136">-ResourceId</span></span>
<span data-ttu-id="02a6d-137">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="02a6d-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="02a6d-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02a6d-138">-Confirm</span></span>
<span data-ttu-id="02a6d-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02a6d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a6d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a6d-140">-WhatIf</span></span>
<span data-ttu-id="02a6d-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02a6d-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="02a6d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a6d-142">CommonParameters</span></span>
<span data-ttu-id="02a6d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a6d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a6d-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a6d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a6d-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02a6d-145">INPUTS</span></span>

### <span data-ttu-id="02a6d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="02a6d-146">System.String</span></span>

## <span data-ttu-id="02a6d-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02a6d-147">OUTPUTS</span></span>

### <span data-ttu-id="02a6d-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="02a6d-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="02a6d-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="02a6d-149">NOTES</span></span>
<span data-ttu-id="02a6d-150">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="02a6d-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="02a6d-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02a6d-151">RELATED LINKS</span></span>

[<span data-ttu-id="02a6d-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="02a6d-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="02a6d-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="02a6d-153">Remove-AzDataFactoryV2Dataset</span></span>]()
