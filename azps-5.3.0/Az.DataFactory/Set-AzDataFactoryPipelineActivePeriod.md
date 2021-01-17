---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 903e375c1272023d2d9b606325cae62103fbbc75
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472640"
---
# <span data-ttu-id="76c6c-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="76c6c-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="76c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="76c6c-103">Konfiguriert den aktiven Zeitraum für Datenschnitte.</span><span class="sxs-lookup"><span data-stu-id="76c6c-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="76c6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76c6c-104">SYNTAX</span></span>

### <span data-ttu-id="76c6c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="76c6c-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76c6c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="76c6c-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76c6c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76c6c-107">DESCRIPTION</span></span>
<span data-ttu-id="76c6c-108">Das **Cmdlet Set-AzDataFactoryPipelineActivePeriod** konfiguriert den aktiven Zeitraum für die Datenschnitte, die von einer Pipeline in Azure Data Factory verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="76c6c-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="76c6c-109">Wenn Sie das Cmdlet Set-AzDataFactorySliceStatus verwenden, um den Status von Segmenten für ein Dataset zu ändern, stellen Sie sicher, dass sich Start- und Endzeit für ein Segment im aktiven Zeitraum der Pipeline befinden.</span><span class="sxs-lookup"><span data-stu-id="76c6c-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="76c6c-110">Nachdem Sie eine Pipeline erstellt haben, können Sie den Zeitraum angeben, in dem die Daten verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="76c6c-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="76c6c-111">Durch Angeben des aktiven Zeitraums für eine Pipeline wird die Dauer definiert,  für die die Datenschnitte verarbeitet werden, basierend auf den Verfügbarkeitseigenschaften, die für jedes Data Factory-Dataset definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="76c6c-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="76c6c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76c6c-112">EXAMPLES</span></span>

### <span data-ttu-id="76c6c-113">Beispiel 1: Konfigurieren des aktiven Zeitraums</span><span class="sxs-lookup"><span data-stu-id="76c6c-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="76c6c-114">Mit diesem Befehl wird der aktive Zeitraum für die Datenschnitte konfiguriert, die von der Pipeline mit dem Namen "DPWikisample" verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="76c6c-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="76c6c-115">Der Befehl stellt Anfangs- und Endpunkte für die Datenschnitte als Werte dar.</span><span class="sxs-lookup"><span data-stu-id="76c6c-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="76c6c-116">Der Befehl gibt den Wert "$True" zurück.</span><span class="sxs-lookup"><span data-stu-id="76c6c-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="76c6c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76c6c-117">PARAMETERS</span></span>

### <span data-ttu-id="76c6c-118">-AutoResolve</span><span class="sxs-lookup"><span data-stu-id="76c6c-118">-AutoResolve</span></span>
<span data-ttu-id="76c6c-119">Gibt an, dass für dieses Cmdlet die automatische Aufräumung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76c6c-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="76c6c-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="76c6c-120">-DataFactory</span></span>
<span data-ttu-id="76c6c-121">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="76c6c-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="76c6c-122">Dieses Cmdlet ändert den aktiven Zeitraum für eine Pipeline, die zu der von diesem Parameter angegebenen Daten factory gehört.</span><span class="sxs-lookup"><span data-stu-id="76c6c-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="76c6c-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="76c6c-123">-DataFactoryName</span></span>
<span data-ttu-id="76c6c-124">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="76c6c-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="76c6c-125">Dieses Cmdlet ändert den aktiven Zeitraum für eine Pipeline, die zu der von diesem Parameter angegebenen Daten factory gehört.</span><span class="sxs-lookup"><span data-stu-id="76c6c-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="76c6c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c6c-126">-DefaultProfile</span></span>
<span data-ttu-id="76c6c-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="76c6c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76c6c-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="76c6c-128">-EndDateTime</span></span>
<span data-ttu-id="76c6c-129">Gibt das Ende eines Zeitraums als **"DateTime"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="76c6c-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="76c6c-130">Die Datenverarbeitung erfolgt, oder Datenschnitte werden innerhalb dieses Zeitraums verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="76c6c-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="76c6c-131">Weitere Informationen zu **"DateTime"-Objekten** erhalten Sie, wenn Sie `Get-Help Get-Date` ".</span><span class="sxs-lookup"><span data-stu-id="76c6c-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="76c6c-132">*EndDateTime* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) Der Standard-Zeitzonen-Designator ist UTC.</span><span class="sxs-lookup"><span data-stu-id="76c6c-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c6c-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="76c6c-133">-ForceRecalculate</span></span>
<span data-ttu-id="76c6c-134">Gibt an, dass für dieses Cmdlet eine Neuberechnung erzwingen wird.</span><span class="sxs-lookup"><span data-stu-id="76c6c-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="76c6c-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="76c6c-135">-PipelineName</span></span>
<span data-ttu-id="76c6c-136">Gibt den Namen der Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="76c6c-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="76c6c-137">Dieses Cmdlet legt den aktiven Zeitraum für die Pipeline fest, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="76c6c-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c6c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c6c-138">-ResourceGroupName</span></span>
<span data-ttu-id="76c6c-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="76c6c-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="76c6c-140">Dieses Cmdlet ändert den aktiven Zeitraum für eine Pipeline, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="76c6c-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="76c6c-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="76c6c-141">-StartDateTime</span></span>
<span data-ttu-id="76c6c-142">Gibt den Anfang eines Zeitraums als **"DateTime"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="76c6c-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="76c6c-143">Die Datenverarbeitung erfolgt, oder Datenschnitte werden innerhalb dieses Zeitraums verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="76c6c-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="76c6c-144">*StartDateTime* muss im ISO8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76c6c-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c6c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76c6c-145">-Confirm</span></span>
<span data-ttu-id="76c6c-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76c6c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c6c-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76c6c-147">-WhatIf</span></span>
<span data-ttu-id="76c6c-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76c6c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c6c-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76c6c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c6c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c6c-150">CommonParameters</span></span>
<span data-ttu-id="76c6c-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c6c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c6c-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c6c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c6c-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76c6c-153">INPUTS</span></span>

### <span data-ttu-id="76c6c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="76c6c-154">System.String</span></span>

### <span data-ttu-id="76c6c-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="76c6c-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="76c6c-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76c6c-156">OUTPUTS</span></span>

### <span data-ttu-id="76c6c-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76c6c-157">System.Boolean</span></span>

## <span data-ttu-id="76c6c-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76c6c-158">NOTES</span></span>
* <span data-ttu-id="76c6c-159">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="76c6c-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="76c6c-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76c6c-160">RELATED LINKS</span></span>

[<span data-ttu-id="76c6c-161">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="76c6c-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="76c6c-162">Set-AzDataFactorySstatus</span><span class="sxs-lookup"><span data-stu-id="76c6c-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


