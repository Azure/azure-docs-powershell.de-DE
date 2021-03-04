---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: ad731dc612290e572ee74a967788e324f764a930
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928232"
---
# <span data-ttu-id="0834f-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0834f-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="0834f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0834f-102">SYNOPSIS</span></span>
<span data-ttu-id="0834f-103">Erstellt eine Pipeline in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0834f-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="0834f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0834f-104">SYNTAX</span></span>

### <span data-ttu-id="0834f-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0834f-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0834f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0834f-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0834f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0834f-107">DESCRIPTION</span></span>
<span data-ttu-id="0834f-108">Das **Cmdlet New-AzDataFactoryPipeline** erstellt eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0834f-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="0834f-109">Wenn Sie einen Namen für eine bereits vorhandene Pipeline angeben, werden Sie vom Cmdlet zur Bestätigung aufgefordert, bevor die Pipeline ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="0834f-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="0834f-110">Wenn Sie den Parameter *Erzwingen* angeben, ersetzt das Cmdlet die vorhandene Pipeline ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="0834f-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="0834f-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="0834f-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="0834f-112">Erstellen Sie eine Daten factory.</span><span class="sxs-lookup"><span data-stu-id="0834f-112">Create a data factory.</span></span> 
- <span data-ttu-id="0834f-113">Erstellen sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="0834f-113">Create linked services.</span></span> 
- <span data-ttu-id="0834f-114">Erstellen Sie Datasets.</span><span class="sxs-lookup"><span data-stu-id="0834f-114">Create datasets.</span></span> 
- <span data-ttu-id="0834f-115">Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0834f-115">Create a pipeline.</span></span>
<span data-ttu-id="0834f-116">Wenn in der Daten factory bereits eine Pipeline mit demselben Namen vorhanden ist, werden Sie in diesem Cmdlet aufgefordert, zu bestätigen, ob die vorhandene Pipeline mit der neuen Pipeline überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0834f-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="0834f-117">Wenn Sie bestätigen, dass die vorhandene Pipeline überschrieben wird, wird auch die Pipelinedefinition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0834f-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="0834f-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0834f-118">EXAMPLES</span></span>

### <span data-ttu-id="0834f-119">Beispiel 1: Erstellen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="0834f-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="0834f-120">Mit diesem Befehl wird eine Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen ADF erstellt.</span><span class="sxs-lookup"><span data-stu-id="0834f-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="0834f-121">Der Befehl basiert auf Informationen in DPWikisample.jsDatei.</span><span class="sxs-lookup"><span data-stu-id="0834f-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="0834f-122">Diese Datei enthält Informationen zu Aktivitäten wie Aktivität kopieren und HDInsight-Aktivität in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0834f-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="0834f-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0834f-123">PARAMETERS</span></span>

### <span data-ttu-id="0834f-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0834f-124">-DataFactory</span></span>
<span data-ttu-id="0834f-125">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="0834f-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0834f-126">Dieses Cmdlet erstellt eine Pipeline für die Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0834f-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0834f-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0834f-127">-DataFactoryName</span></span>
<span data-ttu-id="0834f-128">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="0834f-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0834f-129">Dieses Cmdlet erstellt eine Pipeline für die Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0834f-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0834f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0834f-130">-DefaultProfile</span></span>
<span data-ttu-id="0834f-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0834f-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0834f-132">-Datei</span><span class="sxs-lookup"><span data-stu-id="0834f-132">-File</span></span>
<span data-ttu-id="0834f-133">Gibt den vollständigen Pfad der JSON(JavaScript Object Notation)-Datei an, die die Beschreibung der Pipeline enthält.</span><span class="sxs-lookup"><span data-stu-id="0834f-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="0834f-134">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="0834f-134">-Force</span></span>
<span data-ttu-id="0834f-135">Gibt an, dass dieses Cmdlet eine vorhandene Pipeline ersetzt, ohne Dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0834f-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0834f-136">-Name</span><span class="sxs-lookup"><span data-stu-id="0834f-136">-Name</span></span>
<span data-ttu-id="0834f-137">Gibt den Namen der zu erstellenden Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="0834f-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0834f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0834f-138">-ResourceGroupName</span></span>
<span data-ttu-id="0834f-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0834f-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0834f-140">Dieses Cmdlet erstellt eine Pipeline für die Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0834f-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0834f-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0834f-141">-Confirm</span></span>
<span data-ttu-id="0834f-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0834f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0834f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0834f-143">-WhatIf</span></span>
<span data-ttu-id="0834f-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0834f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0834f-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0834f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0834f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0834f-146">CommonParameters</span></span>
<span data-ttu-id="0834f-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0834f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0834f-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0834f-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0834f-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0834f-149">INPUTS</span></span>

### <span data-ttu-id="0834f-150">System.String</span><span class="sxs-lookup"><span data-stu-id="0834f-150">System.String</span></span>

### <span data-ttu-id="0834f-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0834f-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="0834f-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0834f-152">OUTPUTS</span></span>

### <span data-ttu-id="0834f-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="0834f-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="0834f-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0834f-154">NOTES</span></span>
* <span data-ttu-id="0834f-155">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="0834f-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0834f-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0834f-156">RELATED LINKS</span></span>

[<span data-ttu-id="0834f-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0834f-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="0834f-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0834f-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="0834f-159">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0834f-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="0834f-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="0834f-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="0834f-161">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="0834f-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


