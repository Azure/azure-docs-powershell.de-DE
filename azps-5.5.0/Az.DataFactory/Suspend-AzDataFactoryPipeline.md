---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174617"
---
# <span data-ttu-id="af5c0-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="af5c0-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="af5c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af5c0-102">SYNOPSIS</span></span>
<span data-ttu-id="af5c0-103">Eine Pipeline in Azure Data Factory wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="af5c0-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="af5c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af5c0-104">SYNTAX</span></span>

### <span data-ttu-id="af5c0-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="af5c0-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af5c0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="af5c0-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af5c0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af5c0-107">DESCRIPTION</span></span>
<span data-ttu-id="af5c0-108">Das **Cmdlet "Suspend-AzDataFactoryPipeline"** setzt eine Pipeline in Azure Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="af5c0-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="af5c0-109">Sie können die Pipeline mithilfe des Resume-AzDataFactoryPipeline fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="af5c0-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="af5c0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af5c0-110">EXAMPLES</span></span>

### <span data-ttu-id="af5c0-111">Beispiel 1: Anhalten einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="af5c0-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="af5c0-112">Mit diesem Befehl wird die Pipeline mit dem Namen "DPWikiSample" in der Daten factory namens WikiADF angehalten.</span><span class="sxs-lookup"><span data-stu-id="af5c0-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="af5c0-113">Der Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="af5c0-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="af5c0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af5c0-114">PARAMETERS</span></span>

### <span data-ttu-id="af5c0-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="af5c0-115">-DataFactory</span></span>
<span data-ttu-id="af5c0-116">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="af5c0-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="af5c0-117">Mit diesem Cmdlet wird eine Pipeline angehalten, die zu der von diesem Parameter angegebenen Daten factory gehört.</span><span class="sxs-lookup"><span data-stu-id="af5c0-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="af5c0-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="af5c0-118">-DataFactoryName</span></span>
<span data-ttu-id="af5c0-119">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="af5c0-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="af5c0-120">Mit diesem Cmdlet wird eine Pipeline angehalten, die zu der von diesem Parameter angegebenen Daten factory gehört.</span><span class="sxs-lookup"><span data-stu-id="af5c0-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="af5c0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af5c0-121">-DefaultProfile</span></span>
<span data-ttu-id="af5c0-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="af5c0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af5c0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="af5c0-123">-Name</span></span>
<span data-ttu-id="af5c0-124">Gibt den Namen der Pipeline an, die angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="af5c0-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="af5c0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af5c0-125">-ResourceGroupName</span></span>
<span data-ttu-id="af5c0-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="af5c0-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="af5c0-127">Dieses Cmdlet setzt eine Pipeline an, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="af5c0-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="af5c0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af5c0-128">-Confirm</span></span>
<span data-ttu-id="af5c0-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="af5c0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af5c0-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="af5c0-130">-WhatIf</span></span>
<span data-ttu-id="af5c0-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af5c0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af5c0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="af5c0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af5c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af5c0-133">CommonParameters</span></span>
<span data-ttu-id="af5c0-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af5c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af5c0-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af5c0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af5c0-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af5c0-136">INPUTS</span></span>

### <span data-ttu-id="af5c0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="af5c0-137">System.String</span></span>

### <span data-ttu-id="af5c0-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="af5c0-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="af5c0-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af5c0-139">OUTPUTS</span></span>

### <span data-ttu-id="af5c0-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af5c0-140">System.Boolean</span></span>

## <span data-ttu-id="af5c0-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="af5c0-141">NOTES</span></span>
* <span data-ttu-id="af5c0-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="af5c0-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="af5c0-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="af5c0-143">RELATED LINKS</span></span>

[<span data-ttu-id="af5c0-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="af5c0-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="af5c0-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="af5c0-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="af5c0-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="af5c0-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="af5c0-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="af5c0-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="af5c0-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="af5c0-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


