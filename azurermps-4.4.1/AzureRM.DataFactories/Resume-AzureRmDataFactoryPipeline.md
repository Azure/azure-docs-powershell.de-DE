---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 63bb7337e7473d27838b08763ebe2a7de14514a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479318"
---
# <span data-ttu-id="1f20c-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f20c-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="1f20c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f20c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f20c-103">Setzt eine angehaltene Pipeline in Data Factory fort.</span><span class="sxs-lookup"><span data-stu-id="1f20c-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f20c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f20c-104">SYNTAX</span></span>

### <span data-ttu-id="1f20c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f20c-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f20c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1f20c-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f20c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f20c-107">DESCRIPTION</span></span>
<span data-ttu-id="1f20c-108">Mit dem Cmdlet **Resume-AzureRmDataFactoryPipeline** wird eine angehaltene Pipeline in Azure Data Factory fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1f20c-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="1f20c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f20c-109">EXAMPLES</span></span>

### <span data-ttu-id="1f20c-110">Beispiel 1: Fortsetzen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="1f20c-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="1f20c-111">Mit diesem Befehl wird die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1f20c-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="1f20c-112">Verwenden Sie das Cmdlet **Suspend-AzureRmDataFactoryPipeline** , um eine Pipeline auszusetzen.</span><span class="sxs-lookup"><span data-stu-id="1f20c-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="1f20c-113">Der Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="1f20c-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="1f20c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f20c-114">PARAMETERS</span></span>

### <span data-ttu-id="1f20c-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1f20c-115">-DataFactory</span></span>
<span data-ttu-id="1f20c-116">Gibt ein **PSDataFactory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1f20c-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1f20c-117">Mit diesem Cmdlet wird eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt, fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1f20c-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1f20c-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1f20c-118">-DataFactoryName</span></span>
<span data-ttu-id="1f20c-119">Gibt den Namen einer Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="1f20c-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1f20c-120">Mit diesem Cmdlet wird eine Pipeline, die zu der Data Factory gehört, die dieser Parameter angibt, fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1f20c-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1f20c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1f20c-121">-Name</span></span>
<span data-ttu-id="1f20c-122">Gibt den Namen der Pipeline an, die fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f20c-122">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="1f20c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f20c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f20c-124">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1f20c-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1f20c-125">Mit diesem Cmdlet wird eine Pipeline, die zu der Gruppe gehört, die dieser Parameter angibt, fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1f20c-125">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1f20c-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f20c-126">-Confirm</span></span>
<span data-ttu-id="1f20c-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f20c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f20c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f20c-128">-WhatIf</span></span>
<span data-ttu-id="1f20c-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f20c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f20c-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f20c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f20c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f20c-131">-DefaultProfile</span></span>
<span data-ttu-id="1f20c-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f20c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f20c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f20c-133">CommonParameters</span></span>
<span data-ttu-id="1f20c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f20c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f20c-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f20c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f20c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f20c-136">INPUTS</span></span>

## <span data-ttu-id="1f20c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f20c-137">OUTPUTS</span></span>

### <span data-ttu-id="1f20c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f20c-138">System.Boolean</span></span>

## <span data-ttu-id="1f20c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f20c-139">NOTES</span></span>
* <span data-ttu-id="1f20c-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="1f20c-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1f20c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f20c-141">RELATED LINKS</span></span>

[<span data-ttu-id="1f20c-142">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f20c-142">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="1f20c-143">Neu – AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f20c-143">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="1f20c-144">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f20c-144">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="1f20c-145">Satz-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="1f20c-145">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="1f20c-146">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f20c-146">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


