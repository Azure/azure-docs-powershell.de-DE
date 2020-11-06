---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/resume-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 298a86c05cc318fbe360cddd2341901070601d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477858"
---
# <span data-ttu-id="72a3b-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="72a3b-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="72a3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="72a3b-103">Setzt eine angehaltene Pipeline in Data Factory fort.</span><span class="sxs-lookup"><span data-stu-id="72a3b-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72a3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72a3b-104">SYNTAX</span></span>

### <span data-ttu-id="72a3b-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="72a3b-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72a3b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="72a3b-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72a3b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72a3b-107">DESCRIPTION</span></span>
<span data-ttu-id="72a3b-108">Mit dem Cmdlet **Resume-AzureRmDataFactoryPipeline** wird eine angehaltene Pipeline in Azure Data Factory fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="72a3b-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="72a3b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72a3b-109">EXAMPLES</span></span>

### <span data-ttu-id="72a3b-110">Beispiel 1: Fortsetzen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="72a3b-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="72a3b-111">Mit diesem Befehl wird die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="72a3b-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="72a3b-112">Verwenden Sie das Cmdlet **Suspend-AzureRmDataFactoryPipeline** , um eine Pipeline auszusetzen.</span><span class="sxs-lookup"><span data-stu-id="72a3b-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="72a3b-113">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="72a3b-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="72a3b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="72a3b-114">PARAMETERS</span></span>

### <span data-ttu-id="72a3b-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="72a3b-115">-DataFactory</span></span>
<span data-ttu-id="72a3b-116">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="72a3b-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="72a3b-117">Mit diesem Cmdlet wird eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt, fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="72a3b-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="72a3b-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="72a3b-118">-DataFactoryName</span></span>
<span data-ttu-id="72a3b-119">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="72a3b-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="72a3b-120">Mit diesem Cmdlet wird eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt, fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="72a3b-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="72a3b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a3b-121">-DefaultProfile</span></span>
<span data-ttu-id="72a3b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="72a3b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72a3b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="72a3b-123">-Name</span></span>
<span data-ttu-id="72a3b-124">Gibt den Namen der Pipeline an, die fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="72a3b-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="72a3b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a3b-125">-ResourceGroupName</span></span>
<span data-ttu-id="72a3b-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="72a3b-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="72a3b-127">Mit diesem Cmdlet wird eine Pipeline, die zu der Gruppe gehört, die dieser Parameter angibt, fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="72a3b-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="72a3b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72a3b-128">-Confirm</span></span>
<span data-ttu-id="72a3b-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72a3b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72a3b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72a3b-130">-WhatIf</span></span>
<span data-ttu-id="72a3b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72a3b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72a3b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72a3b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72a3b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a3b-133">CommonParameters</span></span>
<span data-ttu-id="72a3b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72a3b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a3b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a3b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a3b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72a3b-136">INPUTS</span></span>

### <span data-ttu-id="72a3b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="72a3b-137">System.String</span></span>

### <span data-ttu-id="72a3b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="72a3b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="72a3b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72a3b-139">OUTPUTS</span></span>

### <span data-ttu-id="72a3b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72a3b-140">System.Boolean</span></span>

## <span data-ttu-id="72a3b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="72a3b-141">NOTES</span></span>
* <span data-ttu-id="72a3b-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="72a3b-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="72a3b-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72a3b-143">RELATED LINKS</span></span>

[<span data-ttu-id="72a3b-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="72a3b-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="72a3b-145">Neu – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="72a3b-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="72a3b-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="72a3b-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="72a3b-147">Satz-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="72a3b-147">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="72a3b-148">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="72a3b-148">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


