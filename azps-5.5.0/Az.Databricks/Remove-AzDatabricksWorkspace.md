---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148044"
---
# <span data-ttu-id="138d7-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="138d7-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="138d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="138d7-102">SYNOPSIS</span></span>
<span data-ttu-id="138d7-103">Löscht den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="138d7-103">Deletes the workspace.</span></span>

## <span data-ttu-id="138d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="138d7-104">SYNTAX</span></span>

### <span data-ttu-id="138d7-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="138d7-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="138d7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="138d7-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="138d7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="138d7-107">DESCRIPTION</span></span>
<span data-ttu-id="138d7-108">Löscht den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="138d7-108">Deletes the workspace.</span></span>

## <span data-ttu-id="138d7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="138d7-109">EXAMPLES</span></span>

### <span data-ttu-id="138d7-110">Beispiel 1: Entfernen eines Arbeitsbereichs "Databsdatum"</span><span class="sxs-lookup"><span data-stu-id="138d7-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="138d7-111">Mit diesem Befehl wird ein Arbeitsbereich "Databungs" aus einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="138d7-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="138d7-112">Beispiel 2: Entfernen eines Arbeitsbereichs "Databinnen" nach Objekt</span><span class="sxs-lookup"><span data-stu-id="138d7-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="138d7-113">Mit diesem Befehl wird ein Arbeitsbereich "Databungs" aus einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="138d7-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="138d7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="138d7-114">PARAMETERS</span></span>

### <span data-ttu-id="138d7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="138d7-115">-AsJob</span></span>
<span data-ttu-id="138d7-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="138d7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="138d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="138d7-117">-DefaultProfile</span></span>
<span data-ttu-id="138d7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="138d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="138d7-119">-InputObject</span></span>
<span data-ttu-id="138d7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="138d7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="138d7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="138d7-121">-Name</span></span>
<span data-ttu-id="138d7-122">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="138d7-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138d7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="138d7-123">-NoWait</span></span>
<span data-ttu-id="138d7-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="138d7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="138d7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="138d7-125">-PassThru</span></span>
<span data-ttu-id="138d7-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="138d7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="138d7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="138d7-127">-ResourceGroupName</span></span>
<span data-ttu-id="138d7-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="138d7-128">The name of the resource group.</span></span>
<span data-ttu-id="138d7-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="138d7-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138d7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="138d7-130">-SubscriptionId</span></span>
<span data-ttu-id="138d7-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="138d7-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="138d7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="138d7-132">-Confirm</span></span>
<span data-ttu-id="138d7-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="138d7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="138d7-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="138d7-134">-WhatIf</span></span>
<span data-ttu-id="138d7-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="138d7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="138d7-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="138d7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="138d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="138d7-137">CommonParameters</span></span>
<span data-ttu-id="138d7-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="138d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="138d7-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="138d7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="138d7-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="138d7-140">INPUTS</span></span>

### <span data-ttu-id="138d7-141">Microsoft.Azure.PowerShell.Cmdlets.Databpersonenbezogenes.Models.IDatabseriesIdentity</span><span class="sxs-lookup"><span data-stu-id="138d7-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="138d7-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="138d7-142">OUTPUTS</span></span>

### <span data-ttu-id="138d7-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="138d7-143">System.Boolean</span></span>

## <span data-ttu-id="138d7-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="138d7-144">NOTES</span></span>

<span data-ttu-id="138d7-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="138d7-145">ALIASES</span></span>

<span data-ttu-id="138d7-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="138d7-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="138d7-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="138d7-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="138d7-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="138d7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="138d7-149">INPUTOBJECT <IDatabricksIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="138d7-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="138d7-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="138d7-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="138d7-151">`[PeeringName <String>]`: Der Name des vNet-Arbeitsbereichs-Peerings.</span><span class="sxs-lookup"><span data-stu-id="138d7-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="138d7-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="138d7-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="138d7-153">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="138d7-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="138d7-154">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="138d7-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="138d7-155">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="138d7-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="138d7-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="138d7-156">RELATED LINKS</span></span>

