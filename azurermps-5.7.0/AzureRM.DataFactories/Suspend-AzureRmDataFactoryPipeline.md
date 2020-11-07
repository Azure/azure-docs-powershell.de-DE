---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/suspend-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 98c8d5778e827b251c5d0c9b919bde9f86e2c41e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662361"
---
# <span data-ttu-id="fa844-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fa844-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="fa844-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa844-102">SYNOPSIS</span></span>
<span data-ttu-id="fa844-103">Unterbricht eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fa844-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa844-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa844-104">SYNTAX</span></span>

### <span data-ttu-id="fa844-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa844-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa844-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fa844-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa844-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa844-107">DESCRIPTION</span></span>
<span data-ttu-id="fa844-108">Das Cmdlet **Suspend-AzureRmDataFactoryPipeline** unterbricht eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="fa844-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="fa844-109">Sie können die Pipeline mithilfe des Resume-AzureRmDataFactoryPipeline-Cmdlets fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="fa844-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="fa844-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa844-110">EXAMPLES</span></span>

### <span data-ttu-id="fa844-111">Beispiel 1: Anhalten einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="fa844-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="fa844-112">Dieser Befehl unterbricht die Pipeline mit dem Namen DPWikiSample in der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="fa844-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="fa844-113">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="fa844-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="fa844-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa844-114">PARAMETERS</span></span>

### <span data-ttu-id="fa844-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fa844-115">-DataFactory</span></span>
<span data-ttu-id="fa844-116">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fa844-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fa844-117">Dieses Cmdlet unterbricht eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fa844-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa844-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fa844-118">-DataFactoryName</span></span>
<span data-ttu-id="fa844-119">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="fa844-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fa844-120">Dieses Cmdlet unterbricht eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fa844-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa844-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa844-121">-DefaultProfile</span></span>
<span data-ttu-id="fa844-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fa844-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa844-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fa844-123">-Name</span></span>
<span data-ttu-id="fa844-124">Gibt den Namen der Pipeline an, die angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa844-124">Specifies the name of the pipeline to suspend.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa844-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa844-125">-ResourceGroupName</span></span>
<span data-ttu-id="fa844-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fa844-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fa844-127">Dieses Cmdlet unterbricht eine Pipeline, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fa844-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa844-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa844-128">-Confirm</span></span>
<span data-ttu-id="fa844-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa844-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa844-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa844-130">-WhatIf</span></span>
<span data-ttu-id="fa844-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa844-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa844-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa844-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa844-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa844-133">CommonParameters</span></span>
<span data-ttu-id="fa844-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa844-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa844-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa844-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa844-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa844-136">INPUTS</span></span>

### <span data-ttu-id="fa844-137">Keine</span><span class="sxs-lookup"><span data-stu-id="fa844-137">None</span></span>
<span data-ttu-id="fa844-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fa844-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa844-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa844-139">OUTPUTS</span></span>

### <span data-ttu-id="fa844-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa844-140">System.Boolean</span></span>

## <span data-ttu-id="fa844-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa844-141">NOTES</span></span>
* <span data-ttu-id="fa844-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="fa844-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fa844-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa844-143">RELATED LINKS</span></span>

[<span data-ttu-id="fa844-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fa844-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="fa844-145">Neu – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fa844-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="fa844-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fa844-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="fa844-147">Lebenslauf-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="fa844-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="fa844-148">Satz-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="fa844-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


