---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dbdefb2e6fa419898447c17053f58631b35a906d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497630"
---
# <span data-ttu-id="248e5-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="248e5-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="248e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="248e5-102">SYNOPSIS</span></span>
<span data-ttu-id="248e5-103">Erstellt eine Pipeline in Data Factory.</span><span class="sxs-lookup"><span data-stu-id="248e5-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="248e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="248e5-104">SYNTAX</span></span>

### <span data-ttu-id="248e5-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="248e5-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="248e5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="248e5-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="248e5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="248e5-107">DESCRIPTION</span></span>
<span data-ttu-id="248e5-108">Das Cmdlet **New-AzureRmDataFactoryPipeline** erstellt eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="248e5-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="248e5-109">Wenn Sie einen Namen für eine Pipeline angeben, die bereits vorhanden ist, werden Sie vom Cmdlet zur Bestätigung aufgefordert, bevor Sie die Pipeline ersetzt.</span><span class="sxs-lookup"><span data-stu-id="248e5-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="248e5-110">Wenn Sie den Parameter *Force* angeben, ersetzt das Cmdlet die vorhandene Pipeline ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="248e5-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="248e5-111">Führen Sie diese Vorgänge in der folgenden Reihenfolge aus:</span><span class="sxs-lookup"><span data-stu-id="248e5-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="248e5-112">Erstellen Sie eine Data Factory.</span><span class="sxs-lookup"><span data-stu-id="248e5-112">Create a data factory.</span></span> 
- <span data-ttu-id="248e5-113">Erstellen Sie verknüpfte Dienste.</span><span class="sxs-lookup"><span data-stu-id="248e5-113">Create linked services.</span></span> 
- <span data-ttu-id="248e5-114">Erstellen von Datasets</span><span class="sxs-lookup"><span data-stu-id="248e5-114">Create datasets.</span></span> 
- <span data-ttu-id="248e5-115">Erstellen Sie eine Pipeline.</span><span class="sxs-lookup"><span data-stu-id="248e5-115">Create a pipeline.</span></span>

<span data-ttu-id="248e5-116">Wenn bereits eine Pipeline mit demselben Namen in der Data Factory vorhanden ist, werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, ob die vorhandene Pipeline mit der neuen Pipeline überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="248e5-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="248e5-117">Wenn Sie bestätigen, dass die vorhandene Pipeline überschrieben werden soll, wird auch die Pipeline Definition ersetzt.</span><span class="sxs-lookup"><span data-stu-id="248e5-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="248e5-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="248e5-118">EXAMPLES</span></span>

### <span data-ttu-id="248e5-119">Beispiel 1: Erstellen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="248e5-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="248e5-120">Dieser Befehl erstellt eine Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen ADF.</span><span class="sxs-lookup"><span data-stu-id="248e5-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="248e5-121">Der Befehl basiert auf Informationen in der DPWikisample.jsfür die Datei.</span><span class="sxs-lookup"><span data-stu-id="248e5-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="248e5-122">Diese Datei enthält Informationen zu Aktivitäten wie Kopier Aktivitäten und HDInsight-Aktivitäten in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="248e5-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="248e5-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="248e5-123">PARAMETERS</span></span>

### <span data-ttu-id="248e5-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="248e5-124">-DataFactory</span></span>
<span data-ttu-id="248e5-125">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="248e5-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="248e5-126">Dieses Cmdlet erstellt eine Pipeline für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="248e5-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="248e5-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="248e5-127">-DataFactoryName</span></span>
<span data-ttu-id="248e5-128">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="248e5-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="248e5-129">Dieses Cmdlet erstellt eine Pipeline für die Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="248e5-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="248e5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="248e5-130">-DefaultProfile</span></span>
<span data-ttu-id="248e5-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="248e5-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="248e5-132">-Datei</span><span class="sxs-lookup"><span data-stu-id="248e5-132">-File</span></span>
<span data-ttu-id="248e5-133">Gibt den vollständigen Pfad der JSON-Datei (JavaScript Object Notation) an, die die Beschreibung der Pipeline enthält.</span><span class="sxs-lookup"><span data-stu-id="248e5-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="248e5-134">-Force</span><span class="sxs-lookup"><span data-stu-id="248e5-134">-Force</span></span>
<span data-ttu-id="248e5-135">Gibt an, dass dieses Cmdlet eine vorhandene Pipeline ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="248e5-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="248e5-136">-Name</span><span class="sxs-lookup"><span data-stu-id="248e5-136">-Name</span></span>
<span data-ttu-id="248e5-137">Gibt den Namen der zu erstellende Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="248e5-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="248e5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="248e5-138">-ResourceGroupName</span></span>
<span data-ttu-id="248e5-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="248e5-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="248e5-140">Dieses Cmdlet erstellt eine Pipeline für die Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="248e5-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="248e5-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="248e5-141">-Confirm</span></span>
<span data-ttu-id="248e5-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="248e5-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="248e5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="248e5-143">-WhatIf</span></span>
<span data-ttu-id="248e5-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="248e5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="248e5-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="248e5-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="248e5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="248e5-146">CommonParameters</span></span>
<span data-ttu-id="248e5-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="248e5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="248e5-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="248e5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="248e5-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="248e5-149">INPUTS</span></span>

### <span data-ttu-id="248e5-150">Keine</span><span class="sxs-lookup"><span data-stu-id="248e5-150">None</span></span>
<span data-ttu-id="248e5-151">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="248e5-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="248e5-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="248e5-152">OUTPUTS</span></span>

### <span data-ttu-id="248e5-153">Microsoft. WindowsAzure. Commands. Utilities. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="248e5-153">Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="248e5-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="248e5-154">NOTES</span></span>
* <span data-ttu-id="248e5-155">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="248e5-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="248e5-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="248e5-156">RELATED LINKS</span></span>

[<span data-ttu-id="248e5-157">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="248e5-157">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="248e5-158">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="248e5-158">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="248e5-159">Lebenslauf-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="248e5-159">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="248e5-160">Satz-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="248e5-160">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="248e5-161">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="248e5-161">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


