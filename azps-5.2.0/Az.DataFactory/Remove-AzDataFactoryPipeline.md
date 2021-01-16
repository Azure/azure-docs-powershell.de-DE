---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 2bae0bd597cbd97a81efeaecb07e052457b88438
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372349"
---
# <span data-ttu-id="bf62c-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bf62c-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="bf62c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf62c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf62c-103">Entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="bf62c-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="bf62c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf62c-104">SYNTAX</span></span>

### <span data-ttu-id="bf62c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf62c-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf62c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bf62c-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf62c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf62c-107">DESCRIPTION</span></span>
<span data-ttu-id="bf62c-108">Das **Cmdlet "Remove-AzDataFactoryPipeline"** entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="bf62c-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="bf62c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf62c-109">EXAMPLES</span></span>

### <span data-ttu-id="bf62c-110">Beispiel 1: Entfernen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="bf62c-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="bf62c-111">Dieses Cmdlet entfernt die Pipeline mit dem Namen DPWikisample aus der Daten factory namens WikiADF.</span><span class="sxs-lookup"><span data-stu-id="bf62c-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="bf62c-112">Der Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="bf62c-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="bf62c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf62c-113">PARAMETERS</span></span>

### <span data-ttu-id="bf62c-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf62c-114">-DataFactory</span></span>
<span data-ttu-id="bf62c-115">Gibt ein **"PSDataFactory"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="bf62c-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bf62c-116">Dieses Cmdlet entfernt eine Pipeline aus der Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bf62c-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf62c-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bf62c-117">-DataFactoryName</span></span>
<span data-ttu-id="bf62c-118">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="bf62c-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bf62c-119">Dieses Cmdlet entfernt eine Pipeline aus der Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bf62c-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf62c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf62c-120">-DefaultProfile</span></span>
<span data-ttu-id="bf62c-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bf62c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf62c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bf62c-122">-Force</span></span>
<span data-ttu-id="bf62c-123">Zeigt an, dass mit diesem Cmdlet eine Pipeline entfernt wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="bf62c-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="bf62c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bf62c-124">-Name</span></span>
<span data-ttu-id="bf62c-125">Gibt den Namen der zu entfernenden Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="bf62c-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="bf62c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf62c-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf62c-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="bf62c-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bf62c-128">Mit diesem Cmdlet wird eine Pipeline aus der Gruppe entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bf62c-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf62c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf62c-129">-Confirm</span></span>
<span data-ttu-id="bf62c-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf62c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf62c-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bf62c-131">-WhatIf</span></span>
<span data-ttu-id="bf62c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf62c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf62c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf62c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf62c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf62c-134">CommonParameters</span></span>
<span data-ttu-id="bf62c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf62c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf62c-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf62c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf62c-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf62c-137">INPUTS</span></span>

### <span data-ttu-id="bf62c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bf62c-138">System.String</span></span>

### <span data-ttu-id="bf62c-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bf62c-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="bf62c-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf62c-140">OUTPUTS</span></span>

### <span data-ttu-id="bf62c-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="bf62c-141">System.Void</span></span>

## <span data-ttu-id="bf62c-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bf62c-142">NOTES</span></span>
* <span data-ttu-id="bf62c-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="bf62c-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bf62c-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bf62c-144">RELATED LINKS</span></span>

[<span data-ttu-id="bf62c-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bf62c-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="bf62c-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bf62c-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="bf62c-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bf62c-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="bf62c-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="bf62c-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="bf62c-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="bf62c-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


