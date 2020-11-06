---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: c3612f30df1977ffa43887322cf4002dde2e35e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481285"
---
# <span data-ttu-id="80e07-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="80e07-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="80e07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80e07-102">SYNOPSIS</span></span>
<span data-ttu-id="80e07-103">Erstellt eine Pipeline in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="80e07-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80e07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80e07-104">SYNTAX</span></span>

### <span data-ttu-id="80e07-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="80e07-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80e07-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="80e07-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80e07-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80e07-107">DESCRIPTION</span></span>
<span data-ttu-id="80e07-108">Das Set-AzureRmDataFactoryV2Pipeline-Cmdlet erstellt eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="80e07-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="80e07-109">Wenn Sie einen Namen für eine Pipeline angeben, die bereits vorhanden ist, werden Sie vom Cmdlet zur Bestätigung aufgefordert, bevor Sie die Pipeline ersetzt.</span><span class="sxs-lookup"><span data-stu-id="80e07-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="80e07-110">Wenn Sie den Parameter Force angeben, ersetzt das Cmdlet die vorhandene Pipeline ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="80e07-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="80e07-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="80e07-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="80e07-112">Wenn bereits eine Pipeline mit demselben Namen in der Data Factory vorhanden ist, werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, ob die vorhandene Pipeline mit der neuen Pipeline überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="80e07-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="80e07-113">Wenn Sie bestätigen, dass die vorhandene Pipeline überschrieben werden soll, wird auch die Pipeline Definition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="80e07-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="80e07-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80e07-114">EXAMPLES</span></span>

### <span data-ttu-id="80e07-115">Beispiel 1: Erstellen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="80e07-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="80e07-116">Dieser Befehl erstellt eine Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen ADF.</span><span class="sxs-lookup"><span data-stu-id="80e07-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="80e07-117">Der Befehl basiert auf Informationen in der DPWikisample.jsfür die Datei.</span><span class="sxs-lookup"><span data-stu-id="80e07-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="80e07-118">Diese Datei enthält Informationen zu Aktivitäten wie Kopier Aktivitäten und HDInsight-Aktivitäten in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="80e07-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="80e07-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="80e07-119">PARAMETERS</span></span>

### <span data-ttu-id="80e07-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="80e07-120">-DataFactoryName</span></span>
<span data-ttu-id="80e07-121">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="80e07-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="80e07-122">Dieses Cmdlet erstellt eine Pipeline für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="80e07-122">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="80e07-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e07-123">-DefaultProfile</span></span>
<span data-ttu-id="80e07-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80e07-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e07-125">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="80e07-125">-DefinitionFile</span></span>
<span data-ttu-id="80e07-126">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="80e07-126">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e07-127">-Force</span><span class="sxs-lookup"><span data-stu-id="80e07-127">-Force</span></span>
<span data-ttu-id="80e07-128">Gibt an, dass dieses Cmdlet eine vorhandene Pipeline ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="80e07-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="80e07-129">-Name</span><span class="sxs-lookup"><span data-stu-id="80e07-129">-Name</span></span>
<span data-ttu-id="80e07-130">Gibt den Namen der zu erstellende Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="80e07-130">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e07-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e07-131">-ResourceGroupName</span></span>
<span data-ttu-id="80e07-132">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="80e07-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="80e07-133">Dieses Cmdlet erstellt eine Pipeline für die Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="80e07-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="80e07-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="80e07-134">-ResourceId</span></span>
<span data-ttu-id="80e07-135">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="80e07-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="80e07-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80e07-136">-Confirm</span></span>
<span data-ttu-id="80e07-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80e07-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80e07-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80e07-138">-WhatIf</span></span>
<span data-ttu-id="80e07-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80e07-139">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="80e07-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e07-140">CommonParameters</span></span>
<span data-ttu-id="80e07-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80e07-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e07-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80e07-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e07-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80e07-143">INPUTS</span></span>

### <span data-ttu-id="80e07-144">System. String</span><span class="sxs-lookup"><span data-stu-id="80e07-144">System.String</span></span>

## <span data-ttu-id="80e07-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80e07-145">OUTPUTS</span></span>

### <span data-ttu-id="80e07-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="80e07-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="80e07-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="80e07-147">NOTES</span></span>
<span data-ttu-id="80e07-148">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="80e07-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="80e07-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80e07-149">RELATED LINKS</span></span>

[<span data-ttu-id="80e07-150">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="80e07-150">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="80e07-151">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="80e07-151">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="80e07-152">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="80e07-152">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
