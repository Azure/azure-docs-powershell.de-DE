---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: dcdf7cdf9de6de23a3178fe8cbb4ac0f67f43d30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504438"
---
# <span data-ttu-id="0b828-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0b828-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="0b828-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b828-102">SYNOPSIS</span></span>
<span data-ttu-id="0b828-103">Erstellt eine Pipeline in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0b828-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b828-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b828-104">SYNTAX</span></span>

### <span data-ttu-id="0b828-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b828-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b828-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b828-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b828-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b828-107">DESCRIPTION</span></span>
<span data-ttu-id="0b828-108">Das Set-AzureRmDataFactoryV2Pipeline-Cmdlet erstellt eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0b828-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="0b828-109">Wenn Sie einen Namen für eine Pipeline angeben, die bereits vorhanden ist, werden Sie vom Cmdlet zur Bestätigung aufgefordert, bevor Sie die Pipeline ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0b828-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="0b828-110">Wenn Sie den Parameter Force angeben, ersetzt das Cmdlet die vorhandene Pipeline ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="0b828-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="0b828-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:--Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0b828-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="0b828-112">--Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="0b828-112">-- Create linked services.</span></span>
<span data-ttu-id="0b828-113">--Erstellen von Datasets.</span><span class="sxs-lookup"><span data-stu-id="0b828-113">-- Create datasets.</span></span>
<span data-ttu-id="0b828-114">--Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b828-114">-- Create a pipeline.</span></span>
<span data-ttu-id="0b828-115">Wenn bereits eine Pipeline mit demselben Namen in der Data Factory vorhanden ist, werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, ob die vorhandene Pipeline mit der neuen Pipeline überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b828-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="0b828-116">Wenn Sie bestätigen, dass die vorhandene Pipeline überschrieben werden soll, wird auch die Pipeline Definition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0b828-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="0b828-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b828-117">EXAMPLES</span></span>

### <span data-ttu-id="0b828-118">Beispiel 1: Erstellen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="0b828-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="0b828-119">Dieser Befehl erstellt eine Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen ADF.</span><span class="sxs-lookup"><span data-stu-id="0b828-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="0b828-120">Der Befehl basiert auf Informationen in der DPWikisample.jsfür die Datei.</span><span class="sxs-lookup"><span data-stu-id="0b828-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="0b828-121">Diese Datei enthält Informationen zu Aktivitäten wie Kopier Aktivitäten und HDInsight-Aktivitäten in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b828-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="0b828-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b828-122">PARAMETERS</span></span>

### <span data-ttu-id="0b828-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0b828-123">-DataFactoryName</span></span>
<span data-ttu-id="0b828-124">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="0b828-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0b828-125">Dieses Cmdlet erstellt eine Pipeline für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0b828-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b828-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b828-126">-DefaultProfile</span></span>
<span data-ttu-id="0b828-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b828-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b828-128">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="0b828-128">-DefinitionFile</span></span>
<span data-ttu-id="0b828-129">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="0b828-129">The JSON file path.</span></span>

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

### <span data-ttu-id="0b828-130">-Force</span><span class="sxs-lookup"><span data-stu-id="0b828-130">-Force</span></span>
<span data-ttu-id="0b828-131">Gibt an, dass dieses Cmdlet eine vorhandene Pipeline ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0b828-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0b828-132">-Name</span><span class="sxs-lookup"><span data-stu-id="0b828-132">-Name</span></span>
<span data-ttu-id="0b828-133">Gibt den Namen der zu erstellende Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="0b828-133">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b828-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b828-134">-ResourceGroupName</span></span>
<span data-ttu-id="0b828-135">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0b828-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0b828-136">Dieses Cmdlet erstellt eine Pipeline für die Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0b828-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b828-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0b828-137">-ResourceId</span></span>
<span data-ttu-id="0b828-138">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0b828-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0b828-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b828-139">-Confirm</span></span>
<span data-ttu-id="0b828-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b828-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b828-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b828-141">-WhatIf</span></span>
<span data-ttu-id="0b828-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b828-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0b828-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b828-143">CommonParameters</span></span>
<span data-ttu-id="0b828-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b828-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b828-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b828-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b828-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b828-146">INPUTS</span></span>

### <span data-ttu-id="0b828-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0b828-147">System.String</span></span>

## <span data-ttu-id="0b828-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b828-148">OUTPUTS</span></span>

### <span data-ttu-id="0b828-149">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="0b828-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="0b828-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b828-150">NOTES</span></span>
<span data-ttu-id="0b828-151">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="0b828-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0b828-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b828-152">RELATED LINKS</span></span>

[<span data-ttu-id="0b828-153">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0b828-153">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0b828-154">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0b828-154">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0b828-155">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0b828-155">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
