---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298179"
---
# <span data-ttu-id="d7a83-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7a83-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="d7a83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7a83-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a83-103">Unterbricht eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d7a83-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="d7a83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7a83-104">SYNTAX</span></span>

### <span data-ttu-id="d7a83-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7a83-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7a83-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d7a83-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7a83-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7a83-107">DESCRIPTION</span></span>
<span data-ttu-id="d7a83-108">Das Cmdlet **Suspend-AzDataFactoryPipeline** unterbricht eine Pipeline in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d7a83-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="d7a83-109">Sie können die Pipeline mithilfe des Resume-AzDataFactoryPipeline-Cmdlets fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="d7a83-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="d7a83-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7a83-110">EXAMPLES</span></span>

### <span data-ttu-id="d7a83-111">Beispiel 1: Anhalten einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="d7a83-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="d7a83-112">Dieser Befehl unterbricht die Pipeline mit dem Namen DPWikiSample in der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d7a83-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="d7a83-113">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="d7a83-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="d7a83-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7a83-114">PARAMETERS</span></span>

### <span data-ttu-id="d7a83-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d7a83-115">-DataFactory</span></span>
<span data-ttu-id="d7a83-116">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d7a83-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d7a83-117">Dieses Cmdlet unterbricht eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7a83-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7a83-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d7a83-118">-DataFactoryName</span></span>
<span data-ttu-id="d7a83-119">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="d7a83-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d7a83-120">Dieses Cmdlet unterbricht eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7a83-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7a83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a83-121">-DefaultProfile</span></span>
<span data-ttu-id="d7a83-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d7a83-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7a83-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d7a83-123">-Name</span></span>
<span data-ttu-id="d7a83-124">Gibt den Namen der Pipeline an, die angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7a83-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="d7a83-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7a83-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7a83-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d7a83-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d7a83-127">Dieses Cmdlet unterbricht eine Pipeline, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7a83-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7a83-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7a83-128">-Confirm</span></span>
<span data-ttu-id="d7a83-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7a83-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7a83-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7a83-130">-WhatIf</span></span>
<span data-ttu-id="d7a83-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7a83-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7a83-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7a83-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7a83-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a83-133">CommonParameters</span></span>
<span data-ttu-id="d7a83-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a83-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a83-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a83-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a83-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7a83-136">INPUTS</span></span>

### <span data-ttu-id="d7a83-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d7a83-137">System.String</span></span>

### <span data-ttu-id="d7a83-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d7a83-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d7a83-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7a83-139">OUTPUTS</span></span>

### <span data-ttu-id="d7a83-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7a83-140">System.Boolean</span></span>

## <span data-ttu-id="d7a83-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7a83-141">NOTES</span></span>
* <span data-ttu-id="d7a83-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="d7a83-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d7a83-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7a83-143">RELATED LINKS</span></span>

[<span data-ttu-id="d7a83-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7a83-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="d7a83-145">Neu – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7a83-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="d7a83-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7a83-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="d7a83-147">Lebenslauf-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7a83-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="d7a83-148">Satz-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d7a83-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


