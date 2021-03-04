---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 25653cb7423803f2722a87e218c4ee4b3d73be86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929043"
---
# <span data-ttu-id="ee5b8-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ee5b8-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="ee5b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee5b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5b8-103">Entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="ee5b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee5b8-104">SYNTAX</span></span>

### <span data-ttu-id="ee5b8-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee5b8-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee5b8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ee5b8-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee5b8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee5b8-107">DESCRIPTION</span></span>
<span data-ttu-id="ee5b8-108">Das **Cmdlet Remove-AzDataFactoryPipeline** entfernt eine Pipeline aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="ee5b8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ee5b8-109">EXAMPLES</span></span>

### <span data-ttu-id="ee5b8-110">Beispiel 1: Entfernen einer Pipeline</span><span class="sxs-lookup"><span data-stu-id="ee5b8-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="ee5b8-111">Dieses Cmdlet entfernt die Pipeline mit dem Namen DPWikisample aus der Daten factory mit dem Namen WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="ee5b8-112">Der Befehl gibt einen Wert von $True.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="ee5b8-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ee5b8-113">PARAMETERS</span></span>

### <span data-ttu-id="ee5b8-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ee5b8-114">-DataFactory</span></span>
<span data-ttu-id="ee5b8-115">Gibt ein **PSDataFactory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ee5b8-116">Dieses Cmdlet entfernt eine Pipeline aus der Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee5b8-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ee5b8-117">-DataFactoryName</span></span>
<span data-ttu-id="ee5b8-118">Gibt den Namen einer Daten factory an.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ee5b8-119">Dieses Cmdlet entfernt eine Pipeline aus der Daten factory, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee5b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee5b8-120">-DefaultProfile</span></span>
<span data-ttu-id="ee5b8-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ee5b8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee5b8-122">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ee5b8-122">-Force</span></span>
<span data-ttu-id="ee5b8-123">Gibt an, dass mit diesem Cmdlet eine Pipeline entfernt wird, ohne sie zur Bestätigung auffordern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ee5b8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ee5b8-124">-Name</span></span>
<span data-ttu-id="ee5b8-125">Gibt den Namen der zu entfernenden Pipeline an.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="ee5b8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5b8-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee5b8-127">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ee5b8-128">Dieses Cmdlet entfernt eine Pipeline aus der Gruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee5b8-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ee5b8-129">-Confirm</span></span>
<span data-ttu-id="ee5b8-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee5b8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee5b8-131">-WhatIf</span></span>
<span data-ttu-id="ee5b8-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee5b8-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee5b8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5b8-134">CommonParameters</span></span>
<span data-ttu-id="ee5b8-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee5b8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5b8-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee5b8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5b8-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ee5b8-137">INPUTS</span></span>

### <span data-ttu-id="ee5b8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ee5b8-138">System.String</span></span>

### <span data-ttu-id="ee5b8-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ee5b8-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ee5b8-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ee5b8-140">OUTPUTS</span></span>

### <span data-ttu-id="ee5b8-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="ee5b8-141">System.Void</span></span>

## <span data-ttu-id="ee5b8-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ee5b8-142">NOTES</span></span>
* <span data-ttu-id="ee5b8-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="ee5b8-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ee5b8-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ee5b8-144">RELATED LINKS</span></span>

[<span data-ttu-id="ee5b8-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ee5b8-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="ee5b8-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ee5b8-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="ee5b8-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ee5b8-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="ee5b8-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="ee5b8-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="ee5b8-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ee5b8-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


