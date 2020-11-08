---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 2bae0bd597cbd97a81efeaecb07e052457b88438
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995183"
---
# <span data-ttu-id="714bb-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="714bb-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="714bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="714bb-102">SYNOPSIS</span></span>
<span data-ttu-id="714bb-103">Entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="714bb-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="714bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="714bb-104">SYNTAX</span></span>

### <span data-ttu-id="714bb-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="714bb-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="714bb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="714bb-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="714bb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="714bb-107">DESCRIPTION</span></span>
<span data-ttu-id="714bb-108">Das Cmdlet **Remove-AzDataFactoryPipeline** entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="714bb-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="714bb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="714bb-109">EXAMPLES</span></span>

### <span data-ttu-id="714bb-110">Beispiel 1: Entfernen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="714bb-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="714bb-111">Dieses Cmdlet entfernt die Pipeline mit dem Namen DPWikisample aus der Data Factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="714bb-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="714bb-112">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="714bb-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="714bb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="714bb-113">PARAMETERS</span></span>

### <span data-ttu-id="714bb-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="714bb-114">-DataFactory</span></span>
<span data-ttu-id="714bb-115">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="714bb-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="714bb-116">Dieses Cmdlet entfernt eine Pipeline aus der Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="714bb-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="714bb-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="714bb-117">-DataFactoryName</span></span>
<span data-ttu-id="714bb-118">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="714bb-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="714bb-119">Dieses Cmdlet entfernt eine Pipeline aus der Data Factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="714bb-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="714bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="714bb-120">-DefaultProfile</span></span>
<span data-ttu-id="714bb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="714bb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="714bb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="714bb-122">-Force</span></span>
<span data-ttu-id="714bb-123">Gibt an, dass dieses Cmdlet eine Pipeline entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="714bb-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="714bb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="714bb-124">-Name</span></span>
<span data-ttu-id="714bb-125">Gibt den Namen der zu entfernenden Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="714bb-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="714bb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="714bb-126">-ResourceGroupName</span></span>
<span data-ttu-id="714bb-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="714bb-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="714bb-128">Dieses Cmdlet entfernt eine Pipeline aus der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="714bb-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="714bb-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="714bb-129">-Confirm</span></span>
<span data-ttu-id="714bb-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="714bb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="714bb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="714bb-131">-WhatIf</span></span>
<span data-ttu-id="714bb-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="714bb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="714bb-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="714bb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="714bb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="714bb-134">CommonParameters</span></span>
<span data-ttu-id="714bb-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="714bb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="714bb-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="714bb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="714bb-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="714bb-137">INPUTS</span></span>

### <span data-ttu-id="714bb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="714bb-138">System.String</span></span>

### <span data-ttu-id="714bb-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="714bb-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="714bb-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="714bb-140">OUTPUTS</span></span>

### <span data-ttu-id="714bb-141">System. void</span><span class="sxs-lookup"><span data-stu-id="714bb-141">System.Void</span></span>

## <span data-ttu-id="714bb-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="714bb-142">NOTES</span></span>
* <span data-ttu-id="714bb-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="714bb-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="714bb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="714bb-144">RELATED LINKS</span></span>

[<span data-ttu-id="714bb-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="714bb-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="714bb-146">Neu – AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="714bb-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="714bb-147">Lebenslauf-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="714bb-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="714bb-148">Satz-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="714bb-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="714bb-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="714bb-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


