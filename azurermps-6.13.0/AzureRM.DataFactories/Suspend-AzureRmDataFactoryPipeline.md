---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/suspend-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: ecbf1a97ebaa7f4d008b63f9b7d4c49c49a09956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502970"
---
# <span data-ttu-id="a04ab-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a04ab-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="a04ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a04ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a04ab-103">Unterbricht eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a04ab-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a04ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a04ab-104">SYNTAX</span></span>

### <span data-ttu-id="a04ab-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a04ab-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a04ab-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a04ab-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a04ab-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a04ab-107">DESCRIPTION</span></span>
<span data-ttu-id="a04ab-108">Das Cmdlet **Suspend-AzureRmDataFactoryPipeline** unterbricht eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a04ab-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="a04ab-109">Sie können die Pipeline mithilfe des Resume-AzureRmDataFactoryPipeline-Cmdlets fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="a04ab-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="a04ab-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a04ab-110">EXAMPLES</span></span>

### <span data-ttu-id="a04ab-111">Beispiel 1: Anhalten einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="a04ab-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="a04ab-112">Dieser Befehl unterbricht die Pipeline mit dem Namen DPWikiSample in der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a04ab-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="a04ab-113">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="a04ab-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="a04ab-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a04ab-114">PARAMETERS</span></span>

### <span data-ttu-id="a04ab-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a04ab-115">-DataFactory</span></span>
<span data-ttu-id="a04ab-116">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a04ab-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a04ab-117">Dieses Cmdlet unterbricht eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a04ab-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a04ab-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a04ab-118">-DataFactoryName</span></span>
<span data-ttu-id="a04ab-119">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="a04ab-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a04ab-120">Dieses Cmdlet unterbricht eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a04ab-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a04ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04ab-121">-DefaultProfile</span></span>
<span data-ttu-id="a04ab-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a04ab-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a04ab-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a04ab-123">-Name</span></span>
<span data-ttu-id="a04ab-124">Gibt den Namen der Pipeline an, die angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="a04ab-124">Specifies the name of the pipeline to suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a04ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a04ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="a04ab-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a04ab-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a04ab-127">Dieses Cmdlet unterbricht eine Pipeline, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a04ab-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a04ab-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a04ab-128">-Confirm</span></span>
<span data-ttu-id="a04ab-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a04ab-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a04ab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a04ab-130">-WhatIf</span></span>
<span data-ttu-id="a04ab-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a04ab-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a04ab-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a04ab-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a04ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04ab-133">CommonParameters</span></span>
<span data-ttu-id="a04ab-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a04ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04ab-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a04ab-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04ab-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a04ab-136">INPUTS</span></span>

### <span data-ttu-id="a04ab-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a04ab-137">System.String</span></span>

### <span data-ttu-id="a04ab-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a04ab-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a04ab-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a04ab-139">OUTPUTS</span></span>

### <span data-ttu-id="a04ab-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a04ab-140">System.Boolean</span></span>

## <span data-ttu-id="a04ab-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a04ab-141">NOTES</span></span>
* <span data-ttu-id="a04ab-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="a04ab-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a04ab-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a04ab-143">RELATED LINKS</span></span>

[<span data-ttu-id="a04ab-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a04ab-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a04ab-145">Neu – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a04ab-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a04ab-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a04ab-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a04ab-147">Lebenslauf-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a04ab-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a04ab-148">Satz-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a04ab-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


