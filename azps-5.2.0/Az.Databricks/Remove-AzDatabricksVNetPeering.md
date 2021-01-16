---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297094"
---
# <span data-ttu-id="1d4b1-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="1d4b1-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="1d4b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d4b1-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4b1-103">Löscht den Arbeitsbereich vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="1d4b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d4b1-104">SYNTAX</span></span>

### <span data-ttu-id="1d4b1-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d4b1-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1d4b1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1d4b1-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1d4b1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d4b1-107">DESCRIPTION</span></span>
<span data-ttu-id="1d4b1-108">Löscht den Arbeitsbereich vNetPeering.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="1d4b1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d4b1-109">EXAMPLES</span></span>

### <span data-ttu-id="1d4b1-110">Beispiel 1: Entfernen eines vnet-Peerings von Databinnen nach Name</span><span class="sxs-lookup"><span data-stu-id="1d4b1-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="1d4b1-111">Mit diesem Befehl wird ein vnet-Peering von Databinnen nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="1d4b1-112">Beispiel 2: Entfernen eines vnet-Peerings von Databinnen und Daten nach Objekt</span><span class="sxs-lookup"><span data-stu-id="1d4b1-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="1d4b1-113">Mit diesem Befehl wird ein vnet-Peering von Databinnen nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="1d4b1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d4b1-114">PARAMETERS</span></span>

### <span data-ttu-id="1d4b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d4b1-115">-AsJob</span></span>
<span data-ttu-id="1d4b1-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1d4b1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1d4b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4b1-117">-DefaultProfile</span></span>
<span data-ttu-id="1d4b1-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d4b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d4b1-119">-InputObject</span></span>
<span data-ttu-id="1d4b1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1d4b1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1d4b1-121">-Name</span></span>
<span data-ttu-id="1d4b1-122">Der Name des vNet-Arbeitsbereichs-Peerings.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="1d4b1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1d4b1-123">-NoWait</span></span>
<span data-ttu-id="1d4b1-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1d4b1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1d4b1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d4b1-125">-PassThru</span></span>
<span data-ttu-id="1d4b1-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1d4b1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d4b1-127">-ResourceGroupName</span></span>
<span data-ttu-id="1d4b1-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-128">The name of the resource group.</span></span>
<span data-ttu-id="1d4b1-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1d4b1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1d4b1-130">-SubscriptionId</span></span>
<span data-ttu-id="1d4b1-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1d4b1-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1d4b1-132">-WorkspaceName</span></span>
<span data-ttu-id="1d4b1-133">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="1d4b1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d4b1-134">-Confirm</span></span>
<span data-ttu-id="1d4b1-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d4b1-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1d4b1-136">-WhatIf</span></span>
<span data-ttu-id="1d4b1-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d4b1-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d4b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4b1-139">CommonParameters</span></span>
<span data-ttu-id="1d4b1-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4b1-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d4b1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4b1-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d4b1-142">INPUTS</span></span>

### <span data-ttu-id="1d4b1-143">Microsoft.Azure.PowerShell.Cmdlets.Databpersonenbezogenes.Models.IDatabseriesIdentity</span><span class="sxs-lookup"><span data-stu-id="1d4b1-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="1d4b1-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d4b1-144">OUTPUTS</span></span>

### <span data-ttu-id="1d4b1-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d4b1-145">System.Boolean</span></span>

## <span data-ttu-id="1d4b1-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d4b1-146">NOTES</span></span>

<span data-ttu-id="1d4b1-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1d4b1-147">ALIASES</span></span>

<span data-ttu-id="1d4b1-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1d4b1-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1d4b1-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1d4b1-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1d4b1-151">INPUTOBJECT <IDatabricksIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="1d4b1-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1d4b1-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="1d4b1-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1d4b1-153">`[PeeringName <String>]`: Der Name des vNet-Arbeitsbereichs-Peerings.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="1d4b1-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1d4b1-155">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="1d4b1-156">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1d4b1-157">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="1d4b1-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="1d4b1-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d4b1-158">RELATED LINKS</span></span>

