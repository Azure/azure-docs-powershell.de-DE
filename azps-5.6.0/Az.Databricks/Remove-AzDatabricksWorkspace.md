---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: c8e63bd0a6496b1c0ce0899f0e183fb10db32a7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923731"
---
# <span data-ttu-id="d3a97-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="d3a97-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="d3a97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a97-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a97-103">Löscht den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="d3a97-103">Deletes the workspace.</span></span>

## <span data-ttu-id="d3a97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3a97-104">SYNTAX</span></span>

### <span data-ttu-id="d3a97-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3a97-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d3a97-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d3a97-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d3a97-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3a97-107">DESCRIPTION</span></span>
<span data-ttu-id="d3a97-108">Löscht den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="d3a97-108">Deletes the workspace.</span></span>

## <span data-ttu-id="d3a97-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3a97-109">EXAMPLES</span></span>

### <span data-ttu-id="d3a97-110">Beispiel 1: Entfernen eines Databricks-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="d3a97-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="d3a97-111">Mit diesem Befehl wird ein Databricks-Arbeitsbereich aus einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="d3a97-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="d3a97-112">Beispiel 2: Entfernen eines Databricks-Arbeitsbereichs nach Objekt</span><span class="sxs-lookup"><span data-stu-id="d3a97-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="d3a97-113">Mit diesem Befehl wird ein Databricks-Arbeitsbereich aus einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="d3a97-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="d3a97-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d3a97-114">PARAMETERS</span></span>

### <span data-ttu-id="d3a97-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3a97-115">-AsJob</span></span>
<span data-ttu-id="d3a97-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d3a97-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d3a97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a97-117">-DefaultProfile</span></span>
<span data-ttu-id="d3a97-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3a97-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a97-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3a97-119">-InputObject</span></span>
<span data-ttu-id="d3a97-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d3a97-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d3a97-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d3a97-121">-Name</span></span>
<span data-ttu-id="d3a97-122">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d3a97-122">The name of the workspace.</span></span>

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

### <span data-ttu-id="d3a97-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d3a97-123">-NoWait</span></span>
<span data-ttu-id="d3a97-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d3a97-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d3a97-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3a97-125">-PassThru</span></span>
<span data-ttu-id="d3a97-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3a97-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d3a97-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a97-127">-ResourceGroupName</span></span>
<span data-ttu-id="d3a97-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d3a97-128">The name of the resource group.</span></span>
<span data-ttu-id="d3a97-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="d3a97-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d3a97-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3a97-130">-SubscriptionId</span></span>
<span data-ttu-id="d3a97-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d3a97-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d3a97-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3a97-132">-Confirm</span></span>
<span data-ttu-id="d3a97-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3a97-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a97-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a97-134">-WhatIf</span></span>
<span data-ttu-id="d3a97-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3a97-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3a97-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3a97-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a97-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a97-137">CommonParameters</span></span>
<span data-ttu-id="d3a97-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a97-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a97-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3a97-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a97-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3a97-140">INPUTS</span></span>

### <span data-ttu-id="d3a97-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="d3a97-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="d3a97-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3a97-142">OUTPUTS</span></span>

### <span data-ttu-id="d3a97-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d3a97-143">System.Boolean</span></span>

## <span data-ttu-id="d3a97-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d3a97-144">NOTES</span></span>

<span data-ttu-id="d3a97-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d3a97-145">ALIASES</span></span>

<span data-ttu-id="d3a97-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d3a97-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d3a97-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="d3a97-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3a97-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d3a97-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d3a97-149">INPUTOBJECT <IDatabricksIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="d3a97-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d3a97-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d3a97-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d3a97-151">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet-Peering.</span><span class="sxs-lookup"><span data-stu-id="d3a97-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="d3a97-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d3a97-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d3a97-153">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="d3a97-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="d3a97-154">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d3a97-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d3a97-155">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d3a97-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="d3a97-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d3a97-156">RELATED LINKS</span></span>

