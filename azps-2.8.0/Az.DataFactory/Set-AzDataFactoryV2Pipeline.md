---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 45a291a5b1ac7fe9474d85f61d656def1fb5c787
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651666"
---
# <span data-ttu-id="08c99-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="08c99-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="08c99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08c99-102">SYNOPSIS</span></span>
<span data-ttu-id="08c99-103">Erstellt eine Pipeline in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="08c99-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="08c99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08c99-104">SYNTAX</span></span>

### <span data-ttu-id="08c99-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="08c99-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08c99-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="08c99-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08c99-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08c99-107">DESCRIPTION</span></span>
<span data-ttu-id="08c99-108">Das Set-AzDataFactoryV2Pipeline-Cmdlet erstellt eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="08c99-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="08c99-109">Wenn Sie einen Namen für eine Pipeline angeben, die bereits vorhanden ist, werden Sie vom Cmdlet zur Bestätigung aufgefordert, bevor Sie die Pipeline ersetzt.</span><span class="sxs-lookup"><span data-stu-id="08c99-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="08c99-110">Wenn Sie den Parameter Force angeben, ersetzt das Cmdlet die vorhandene Pipeline ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="08c99-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="08c99-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:--Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="08c99-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="08c99-112">--Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="08c99-112">-- Create linked services.</span></span>
<span data-ttu-id="08c99-113">--Erstellen von Datasets.</span><span class="sxs-lookup"><span data-stu-id="08c99-113">-- Create datasets.</span></span>
<span data-ttu-id="08c99-114">--Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="08c99-114">-- Create a pipeline.</span></span>
<span data-ttu-id="08c99-115">Wenn bereits eine Pipeline mit demselben Namen in der Data Factory vorhanden ist, werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, ob die vorhandene Pipeline mit der neuen Pipeline überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="08c99-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="08c99-116">Wenn Sie bestätigen, dass die vorhandene Pipeline überschrieben werden soll, wird auch die Pipeline Definition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="08c99-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="08c99-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08c99-117">EXAMPLES</span></span>

### <span data-ttu-id="08c99-118">Beispiel 1: Erstellen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="08c99-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="08c99-119">Dieser Befehl erstellt eine Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen ADF.</span><span class="sxs-lookup"><span data-stu-id="08c99-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="08c99-120">Der Befehl basiert auf Informationen in der DPWikisample.jsfür die Datei.</span><span class="sxs-lookup"><span data-stu-id="08c99-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="08c99-121">Diese Datei enthält Informationen zu Aktivitäten wie Kopier Aktivitäten und HDInsight-Aktivitäten in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="08c99-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="08c99-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="08c99-122">PARAMETERS</span></span>

### <span data-ttu-id="08c99-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="08c99-123">-DataFactoryName</span></span>
<span data-ttu-id="08c99-124">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="08c99-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="08c99-125">Dieses Cmdlet erstellt eine Pipeline für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="08c99-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="08c99-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c99-126">-DefaultProfile</span></span>
<span data-ttu-id="08c99-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08c99-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08c99-128">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="08c99-128">-DefinitionFile</span></span>
<span data-ttu-id="08c99-129">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="08c99-129">The JSON file path.</span></span>

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

### <span data-ttu-id="08c99-130">-Force</span><span class="sxs-lookup"><span data-stu-id="08c99-130">-Force</span></span>
<span data-ttu-id="08c99-131">Gibt an, dass dieses Cmdlet eine vorhandene Pipeline ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="08c99-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="08c99-132">-Name</span><span class="sxs-lookup"><span data-stu-id="08c99-132">-Name</span></span>
<span data-ttu-id="08c99-133">Gibt den Namen der zu erstellende Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="08c99-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="08c99-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08c99-134">-ResourceGroupName</span></span>
<span data-ttu-id="08c99-135">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="08c99-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="08c99-136">Dieses Cmdlet erstellt eine Pipeline für die Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="08c99-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="08c99-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="08c99-137">-ResourceId</span></span>
<span data-ttu-id="08c99-138">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="08c99-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="08c99-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08c99-139">-Confirm</span></span>
<span data-ttu-id="08c99-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08c99-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08c99-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08c99-141">-WhatIf</span></span>
<span data-ttu-id="08c99-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08c99-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="08c99-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c99-143">CommonParameters</span></span>
<span data-ttu-id="08c99-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c99-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c99-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c99-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c99-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08c99-146">INPUTS</span></span>

### <span data-ttu-id="08c99-147">System. String</span><span class="sxs-lookup"><span data-stu-id="08c99-147">System.String</span></span>

## <span data-ttu-id="08c99-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08c99-148">OUTPUTS</span></span>

### <span data-ttu-id="08c99-149">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="08c99-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="08c99-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="08c99-150">NOTES</span></span>
<span data-ttu-id="08c99-151">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="08c99-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="08c99-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08c99-152">RELATED LINKS</span></span>

[<span data-ttu-id="08c99-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="08c99-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="08c99-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="08c99-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="08c99-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="08c99-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
