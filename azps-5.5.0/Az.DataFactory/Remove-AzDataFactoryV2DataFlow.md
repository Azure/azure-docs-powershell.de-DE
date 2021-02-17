---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b441c354214775f3f6aad425513a953fbefe7810
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404512"
---
# <span data-ttu-id="c7b7e-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="c7b7e-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="c7b7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b7e-103">Entfernt einen Datenfluss aus Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="c7b7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7b7e-104">SYNTAX</span></span>

### <span data-ttu-id="c7b7e-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7b7e-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7b7e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c7b7e-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b7e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b7e-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7b7e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7b7e-108">DESCRIPTION</span></span>
<span data-ttu-id="c7b7e-109">Das Remove-AzDataFactoryV2DataFlow cmdlet entfernt einen Datenfluss aus Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="c7b7e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7b7e-110">EXAMPLES</span></span>

### <span data-ttu-id="c7b7e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c7b7e-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="c7b7e-112">Mit diesem Befehl wird der Datenfluss mit dem Namen "dataflow5" aus der Daten factory namens WikiADF entfernt.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="c7b7e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7b7e-113">PARAMETERS</span></span>

### <span data-ttu-id="c7b7e-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c7b7e-114">-DataFactoryName</span></span>
<span data-ttu-id="c7b7e-115">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-115">The data factory name.</span></span>

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

### <span data-ttu-id="c7b7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b7e-116">-DefaultProfile</span></span>
<span data-ttu-id="c7b7e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7b7e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c7b7e-118">-Force</span></span>
<span data-ttu-id="c7b7e-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c7b7e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7b7e-120">-InputObject</span></span>
<span data-ttu-id="c7b7e-121">Das Datenflussobjekt.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b7e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c7b7e-122">-Name</span></span>
<span data-ttu-id="c7b7e-123">Der Datenflussname.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b7e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7b7e-124">-ResourceGroupName</span></span>
<span data-ttu-id="c7b7e-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-125">The resource group name.</span></span>

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

### <span data-ttu-id="c7b7e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b7e-126">-ResourceId</span></span>
<span data-ttu-id="c7b7e-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b7e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7b7e-128">-PassThru</span></span>
<span data-ttu-id="c7b7e-129">Wenn angegeben, wird "true" für den Fall geschrieben, dass der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="c7b7e-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7b7e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7b7e-131">-Confirm</span></span>
<span data-ttu-id="c7b7e-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b7e-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c7b7e-133">-WhatIf</span></span>
<span data-ttu-id="c7b7e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7b7e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b7e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b7e-136">CommonParameters</span></span>
<span data-ttu-id="c7b7e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b7e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b7e-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7b7e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b7e-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7b7e-139">INPUTS</span></span>

### <span data-ttu-id="c7b7e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="c7b7e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="c7b7e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c7b7e-141">System.String</span></span>

## <span data-ttu-id="c7b7e-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7b7e-142">OUTPUTS</span></span>

### <span data-ttu-id="c7b7e-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="c7b7e-143">System.Void</span></span>

### <span data-ttu-id="c7b7e-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c7b7e-144">System.Boolean</span></span>

## <span data-ttu-id="c7b7e-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c7b7e-145">NOTES</span></span>
<span data-ttu-id="c7b7e-146">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="c7b7e-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c7b7e-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c7b7e-147">RELATED LINKS</span></span>



