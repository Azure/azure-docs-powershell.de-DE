---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: edb2e94900d383675bd183c09df16e295828aae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820343"
---
# <span data-ttu-id="560f2-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="560f2-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="560f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="560f2-102">SYNOPSIS</span></span>
<span data-ttu-id="560f2-103">Konfiguriert den aktiven Zeitraum für Datenslices.</span><span class="sxs-lookup"><span data-stu-id="560f2-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="560f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="560f2-104">SYNTAX</span></span>

### <span data-ttu-id="560f2-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="560f2-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="560f2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="560f2-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="560f2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="560f2-107">DESCRIPTION</span></span>
<span data-ttu-id="560f2-108">Das Cmdlet " **festlegen-AzDataFactoryPipelineActivePeriod** " konfiguriert den aktiven Zeitraum für die Datensegmente, die von einer Pipeline in Azure Data Factory verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="560f2-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="560f2-109">Wenn Sie das Set-AzDataFactorySliceStatus-Cmdlet verwenden, um den Status von Segmenten für ein DataSet zu ändern, stellen Sie sicher, dass sich die Startzeit und die Endzeit für ein Segment im aktiven Zeitraum der Pipeline befinden.</span><span class="sxs-lookup"><span data-stu-id="560f2-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="560f2-110">Nachdem Sie eine Pipeline erstellt haben, können Sie den Zeitraum angeben, in dem die Datenverarbeitung erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="560f2-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="560f2-111">Wenn Sie den aktiven Zeitraum für eine Pipeline angeben, wird die Zeitdauer definiert, in der die Datensegmente basierend auf den **Verfügbarkeits** Eigenschaften verarbeitet werden, die für die einzelnen Daten Factory-Datasets definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="560f2-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="560f2-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="560f2-112">EXAMPLES</span></span>

### <span data-ttu-id="560f2-113">Beispiel 1: Konfigurieren des aktiven Zeitraums</span><span class="sxs-lookup"><span data-stu-id="560f2-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="560f2-114">Dieser Befehl konfiguriert den aktiven Zeitraum für die Datensegmente, die von der Pipeline mit dem Namen DPWikisample verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="560f2-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="560f2-115">Der Befehl bietet Anfangs-und Endpunkte für die Datensegmente als Werte.</span><span class="sxs-lookup"><span data-stu-id="560f2-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="560f2-116">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="560f2-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="560f2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="560f2-117">PARAMETERS</span></span>

### <span data-ttu-id="560f2-118">– Autoresolve</span><span class="sxs-lookup"><span data-stu-id="560f2-118">-AutoResolve</span></span>
<span data-ttu-id="560f2-119">Gibt an, dass dieses Cmdlet die automatische Aufhebung verwendet.</span><span class="sxs-lookup"><span data-stu-id="560f2-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="560f2-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="560f2-120">-DataFactory</span></span>
<span data-ttu-id="560f2-121">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="560f2-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="560f2-122">Dieses Cmdlet ändert den aktiven Zeitraum für eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="560f2-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="560f2-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="560f2-123">-DataFactoryName</span></span>
<span data-ttu-id="560f2-124">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="560f2-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="560f2-125">Dieses Cmdlet ändert den aktiven Zeitraum für eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="560f2-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="560f2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560f2-126">-DefaultProfile</span></span>
<span data-ttu-id="560f2-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="560f2-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="560f2-128">-Enddatum</span><span class="sxs-lookup"><span data-stu-id="560f2-128">-EndDateTime</span></span>
<span data-ttu-id="560f2-129">Gibt das Ende eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="560f2-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="560f2-130">Die Datenverarbeitung erfolgt, oder Datenscheiben werden innerhalb dieses Zeitraums verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="560f2-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="560f2-131">Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="560f2-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="560f2-132">*Enddatum* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pazifik-Standardzeit) der standardmäßige Zeitzonenbezeichner ist UTC.</span><span class="sxs-lookup"><span data-stu-id="560f2-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="560f2-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="560f2-133">-ForceRecalculate</span></span>
<span data-ttu-id="560f2-134">Gibt an, dass dieses Cmdlet Force-Neuberechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="560f2-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="560f2-135">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="560f2-135">-PipelineName</span></span>
<span data-ttu-id="560f2-136">Gibt den Namen der Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="560f2-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="560f2-137">Mit diesem Cmdlet wird der aktive Zeitraum für die Pipeline festgelegt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="560f2-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="560f2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="560f2-138">-ResourceGroupName</span></span>
<span data-ttu-id="560f2-139">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="560f2-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="560f2-140">Dieses Cmdlet ändert den aktiven Zeitraum für eine Pipeline, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="560f2-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="560f2-141">-Startdatum</span><span class="sxs-lookup"><span data-stu-id="560f2-141">-StartDateTime</span></span>
<span data-ttu-id="560f2-142">Gibt den Anfang eines Zeitraums als **DateTime** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="560f2-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="560f2-143">Die Datenverarbeitung erfolgt, oder Datenscheiben werden innerhalb dieses Zeitraums verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="560f2-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="560f2-144">Start *Datum* muss im ISO8601-Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="560f2-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="560f2-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="560f2-145">-Confirm</span></span>
<span data-ttu-id="560f2-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="560f2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="560f2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="560f2-147">-WhatIf</span></span>
<span data-ttu-id="560f2-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="560f2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="560f2-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="560f2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="560f2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560f2-150">CommonParameters</span></span>
<span data-ttu-id="560f2-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="560f2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560f2-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="560f2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560f2-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="560f2-153">INPUTS</span></span>

### <span data-ttu-id="560f2-154">System. String</span><span class="sxs-lookup"><span data-stu-id="560f2-154">System.String</span></span>

### <span data-ttu-id="560f2-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="560f2-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="560f2-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="560f2-156">OUTPUTS</span></span>

### <span data-ttu-id="560f2-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="560f2-157">System.Boolean</span></span>

## <span data-ttu-id="560f2-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="560f2-158">NOTES</span></span>
* <span data-ttu-id="560f2-159">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="560f2-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="560f2-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="560f2-160">RELATED LINKS</span></span>

[<span data-ttu-id="560f2-161">Neu – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="560f2-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="560f2-162">Satz-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="560f2-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


