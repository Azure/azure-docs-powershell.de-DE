---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356403"
---
# <span data-ttu-id="6310f-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6310f-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="6310f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6310f-102">SYNOPSIS</span></span>
<span data-ttu-id="6310f-103">Eine Pipeline in Azure Data Factory wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="6310f-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="6310f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6310f-104">SYNTAX</span></span>

### <span data-ttu-id="6310f-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6310f-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6310f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6310f-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6310f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6310f-107">DESCRIPTION</span></span>
<span data-ttu-id="6310f-108">Das **Cmdlet "Suspend-AzDataFactoryPipeline"** setzt eine Pipeline in Azure Data Factory an.</span><span class="sxs-lookup"><span data-stu-id="6310f-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="6310f-109">Sie können die Pipeline mithilfe des Resume-AzDataFactoryPipeline fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="6310f-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="6310f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6310f-110">EXAMPLES</span></span>

### <span data-ttu-id="6310f-111">Beispiel 1: Anhalten einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="6310f-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="6310f-112">Mit diesem Befehl wird die Pipeline mit dem Namen DPWikiSample in der Daten factory namens WikiADF angehalten.</span><span class="sxs-lookup"><span data-stu-id="6310f-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="6310f-113">Der Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="6310f-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="6310f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6310f-114">PARAMETERS</span></span>

### <span data-ttu-id="6310f-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6310f-115">-DataFactory</span></span>
<span data-ttu-id="6310f-116">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="6310f-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6310f-117">Mit diesem Cmdlet wird eine Pipeline angehalten, die zu der von diesem Parameter angegebenen Daten factory gehört.</span><span class="sxs-lookup"><span data-stu-id="6310f-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6310f-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6310f-118">-DataFactoryName</span></span>
<span data-ttu-id="6310f-119">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="6310f-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6310f-120">Mit diesem Cmdlet wird eine Pipeline angehalten, die zu der von diesem Parameter angegebenen Daten factory gehört.</span><span class="sxs-lookup"><span data-stu-id="6310f-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6310f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6310f-121">-DefaultProfile</span></span>
<span data-ttu-id="6310f-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6310f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6310f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6310f-123">-Name</span></span>
<span data-ttu-id="6310f-124">Gibt den Namen der Pipeline an, die angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="6310f-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="6310f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6310f-125">-ResourceGroupName</span></span>
<span data-ttu-id="6310f-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6310f-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6310f-127">Mit diesem Cmdlet wird eine Pipeline angehalten, die zu der Gruppe gehört, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6310f-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6310f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6310f-128">-Confirm</span></span>
<span data-ttu-id="6310f-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6310f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6310f-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6310f-130">-WhatIf</span></span>
<span data-ttu-id="6310f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6310f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6310f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6310f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6310f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6310f-133">CommonParameters</span></span>
<span data-ttu-id="6310f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6310f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6310f-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6310f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6310f-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6310f-136">INPUTS</span></span>

### <span data-ttu-id="6310f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6310f-137">System.String</span></span>

### <span data-ttu-id="6310f-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6310f-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="6310f-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6310f-139">OUTPUTS</span></span>

### <span data-ttu-id="6310f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6310f-140">System.Boolean</span></span>

## <span data-ttu-id="6310f-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6310f-141">NOTES</span></span>
* <span data-ttu-id="6310f-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="6310f-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6310f-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6310f-143">RELATED LINKS</span></span>

[<span data-ttu-id="6310f-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6310f-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="6310f-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6310f-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="6310f-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6310f-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="6310f-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6310f-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="6310f-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="6310f-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


