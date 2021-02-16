---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170880"
---
# <span data-ttu-id="72271-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="72271-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="72271-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72271-102">SYNOPSIS</span></span>
<span data-ttu-id="72271-103">Erstellt eine Pipeline in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="72271-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="72271-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72271-104">SYNTAX</span></span>

### <span data-ttu-id="72271-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="72271-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72271-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="72271-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72271-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72271-107">DESCRIPTION</span></span>
<span data-ttu-id="72271-108">Das Set-AzDataFactoryV2Pipeline erstellt eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="72271-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="72271-109">Wenn Sie einen Namen für eine Pipeline angeben, die bereits vorhanden ist, werden Sie vom Cmdlet zur Bestätigung aufgefordert, bevor die Pipeline ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="72271-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="72271-110">Wenn Sie den Parameter "Force" angeben, ersetzt das Cmdlet die vorhandene Pipeline ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="72271-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="72271-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus: -- Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="72271-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="72271-112">- Verknüpfte Dienste erstellen.</span><span class="sxs-lookup"><span data-stu-id="72271-112">-- Create linked services.</span></span>
<span data-ttu-id="72271-113">– Erstellen sie Datasets.</span><span class="sxs-lookup"><span data-stu-id="72271-113">-- Create datasets.</span></span>
<span data-ttu-id="72271-114">– Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="72271-114">-- Create a pipeline.</span></span>
<span data-ttu-id="72271-115">Wenn in der Daten factory bereits eine Pipeline mit demselben Namen vorhanden ist, werden Sie von diesem Cmdlet aufgefordert zu bestätigen, ob die vorhandene Pipeline mit der neuen Pipeline überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="72271-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="72271-116">Wenn Sie bestätigen, dass die vorhandene Pipeline überschrieben wird, wird auch die Pipelinedefinition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="72271-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="72271-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72271-117">EXAMPLES</span></span>

### <span data-ttu-id="72271-118">Beispiel 1: Erstellen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="72271-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="72271-119">Mit diesem Befehl wird eine Pipeline mit dem Namen DPWikisample in der Daten factory namens ADF erstellt.</span><span class="sxs-lookup"><span data-stu-id="72271-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="72271-120">Der Befehl basiert auf Der Pipeline basiert auf Informationen in DPWikisample.jsDatei.</span><span class="sxs-lookup"><span data-stu-id="72271-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="72271-121">Diese Datei enthält Informationen zu Aktivitäten wie "Kopieraktivität" und "HDInsight-Aktivität" in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="72271-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="72271-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72271-122">PARAMETERS</span></span>

### <span data-ttu-id="72271-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="72271-123">-DataFactoryName</span></span>
<span data-ttu-id="72271-124">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="72271-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="72271-125">Dieses Cmdlet erstellt eine Pipeline für die Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="72271-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="72271-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72271-126">-DefaultProfile</span></span>
<span data-ttu-id="72271-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72271-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72271-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="72271-128">-DefinitionFile</span></span>
<span data-ttu-id="72271-129">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="72271-129">The JSON file path.</span></span>

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

### <span data-ttu-id="72271-130">-Force</span><span class="sxs-lookup"><span data-stu-id="72271-130">-Force</span></span>
<span data-ttu-id="72271-131">Gibt an, dass dieses Cmdlet eine vorhandene Pipeline ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="72271-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="72271-132">-Name</span><span class="sxs-lookup"><span data-stu-id="72271-132">-Name</span></span>
<span data-ttu-id="72271-133">Gibt den Namen der zu erstellenden Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="72271-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="72271-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72271-134">-ResourceGroupName</span></span>
<span data-ttu-id="72271-135">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="72271-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="72271-136">Dieses Cmdlet erstellt eine Pipeline für die Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="72271-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="72271-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72271-137">-ResourceId</span></span>
<span data-ttu-id="72271-138">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="72271-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="72271-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72271-139">-Confirm</span></span>
<span data-ttu-id="72271-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72271-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72271-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="72271-141">-WhatIf</span></span>
<span data-ttu-id="72271-142">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72271-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="72271-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72271-143">CommonParameters</span></span>
<span data-ttu-id="72271-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72271-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72271-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72271-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72271-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72271-146">INPUTS</span></span>

### <span data-ttu-id="72271-147">System.String</span><span class="sxs-lookup"><span data-stu-id="72271-147">System.String</span></span>

## <span data-ttu-id="72271-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72271-148">OUTPUTS</span></span>

### <span data-ttu-id="72271-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="72271-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="72271-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="72271-150">NOTES</span></span>
<span data-ttu-id="72271-151">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="72271-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="72271-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="72271-152">RELATED LINKS</span></span>

[<span data-ttu-id="72271-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="72271-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="72271-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="72271-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="72271-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="72271-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
