---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/remove-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Remove-AzDataBoxJob.md
ms.openlocfilehash: 5a9415b5590b6f78c5ca703dba8293c153de819d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942651"
---
# <span data-ttu-id="d6e1b-101">Remove-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="d6e1b-101">Remove-AzDataBoxJob</span></span>

## <span data-ttu-id="d6e1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e1b-103">Löscht den Databoxauftrag</span><span class="sxs-lookup"><span data-stu-id="d6e1b-103">Deletes the databox job</span></span>

## <span data-ttu-id="d6e1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6e1b-104">SYNTAX</span></span>

### <span data-ttu-id="d6e1b-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6e1b-105">GetByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e1b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6e1b-106">GetByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6e1b-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6e1b-107">GetByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxJob -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6e1b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6e1b-108">DESCRIPTION</span></span>
<span data-ttu-id="d6e1b-109">Das **Cmdlet Remove-AzDataBoxJob** wird verwendet, um einen abgeschlossenen Datenboxauftrag aus der Liste der Databoxaufträge zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d6e1b-109">The **Remove-AzDataBoxJob** cmdlet is used to delete a finished databox job from the list of databox jobs.</span></span>

## <span data-ttu-id="d6e1b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d6e1b-110">EXAMPLES</span></span>

### <span data-ttu-id="d6e1b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6e1b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test 
Confirm
"Cancelling Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="d6e1b-112">Löscht den angegebenen Databoxauftrag</span><span class="sxs-lookup"><span data-stu-id="d6e1b-112">Deletes the specified databox job</span></span>

### <span data-ttu-id="d6e1b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d6e1b-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceGroupName TestRg -name test -Force

```

<span data-ttu-id="d6e1b-114">Löscht den angegebenen Databox-Auftrag ohne Bestätigung mit Gewalt</span><span class="sxs-lookup"><span data-stu-id="d6e1b-114">Deletes the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="d6e1b-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d6e1b-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="d6e1b-116">Löscht den angegebenen Databoxauftrag</span><span class="sxs-lookup"><span data-stu-id="d6e1b-116">Deletes the specified databox job</span></span>

## <span data-ttu-id="d6e1b-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d6e1b-117">PARAMETERS</span></span>

### <span data-ttu-id="d6e1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e1b-118">-DefaultProfile</span></span>
<span data-ttu-id="d6e1b-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6e1b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6e1b-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d6e1b-120">-Force</span></span>
<span data-ttu-id="d6e1b-121">Erzwingen des Entfernens ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="d6e1b-121">Force remove without confirmation</span></span>

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

### <span data-ttu-id="d6e1b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6e1b-122">-InputObject</span></span>
<span data-ttu-id="d6e1b-123">InputObject vom Typ PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="d6e1b-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e1b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d6e1b-124">-Name</span></span>
<span data-ttu-id="d6e1b-125">Name des Databox-Auftrags</span><span class="sxs-lookup"><span data-stu-id="d6e1b-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e1b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6e1b-126">-PassThru</span></span>
<span data-ttu-id="d6e1b-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="d6e1b-127">PassThru</span></span>

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

### <span data-ttu-id="d6e1b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e1b-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6e1b-129">Name der Databox-Jobressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d6e1b-129">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6e1b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6e1b-130">-ResourceId</span></span>
<span data-ttu-id="d6e1b-131">Databox Job Resource Id</span><span class="sxs-lookup"><span data-stu-id="d6e1b-131">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6e1b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6e1b-132">-Confirm</span></span>
<span data-ttu-id="d6e1b-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6e1b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6e1b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6e1b-134">-WhatIf</span></span>
<span data-ttu-id="d6e1b-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6e1b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6e1b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6e1b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6e1b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e1b-137">CommonParameters</span></span>
<span data-ttu-id="d6e1b-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6e1b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e1b-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6e1b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e1b-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d6e1b-140">INPUTS</span></span>

### <span data-ttu-id="d6e1b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d6e1b-141">System.String</span></span>

## <span data-ttu-id="d6e1b-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d6e1b-142">OUTPUTS</span></span>

### <span data-ttu-id="d6e1b-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="d6e1b-143">System.Void</span></span>

## <span data-ttu-id="d6e1b-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d6e1b-144">NOTES</span></span>

## <span data-ttu-id="d6e1b-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d6e1b-145">RELATED LINKS</span></span>
