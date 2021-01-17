---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469400"
---
# <span data-ttu-id="3a97d-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3a97d-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="3a97d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a97d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a97d-103">Löscht die Regel für das virtuelle Netzwerk mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="3a97d-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="3a97d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a97d-104">SYNTAX</span></span>

### <span data-ttu-id="3a97d-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a97d-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3a97d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a97d-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3a97d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a97d-107">DESCRIPTION</span></span>
<span data-ttu-id="3a97d-108">Löscht die Regel für das virtuelle Netzwerk mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="3a97d-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="3a97d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a97d-109">EXAMPLES</span></span>

### <span data-ttu-id="3a97d-110">Beispiel 1: Entfernen einer Regel für ein virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="3a97d-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="3a97d-111">Mit diesem Befehl wird eine Regel für ein virtuelles Netzwerk entfernt.</span><span class="sxs-lookup"><span data-stu-id="3a97d-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="3a97d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a97d-112">PARAMETERS</span></span>

### <span data-ttu-id="3a97d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a97d-113">-AsJob</span></span>
<span data-ttu-id="3a97d-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="3a97d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3a97d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a97d-115">-DefaultProfile</span></span>
<span data-ttu-id="3a97d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a97d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a97d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a97d-117">-InputObject</span></span>
<span data-ttu-id="3a97d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3a97d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a97d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3a97d-119">-Name</span></span>
<span data-ttu-id="3a97d-120">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3a97d-120">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a97d-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3a97d-121">-NoWait</span></span>
<span data-ttu-id="3a97d-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="3a97d-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a97d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a97d-123">-PassThru</span></span>
<span data-ttu-id="3a97d-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="3a97d-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3a97d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a97d-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a97d-126">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="3a97d-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3a97d-127">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="3a97d-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3a97d-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3a97d-128">-ServerName</span></span>
<span data-ttu-id="3a97d-129">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3a97d-129">The name of the server.</span></span>

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

### <span data-ttu-id="3a97d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a97d-130">-SubscriptionId</span></span>
<span data-ttu-id="3a97d-131">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3a97d-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3a97d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a97d-132">-Confirm</span></span>
<span data-ttu-id="3a97d-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a97d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a97d-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3a97d-134">-WhatIf</span></span>
<span data-ttu-id="3a97d-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a97d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a97d-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a97d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a97d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a97d-137">CommonParameters</span></span>
<span data-ttu-id="3a97d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a97d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a97d-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a97d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a97d-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a97d-140">INPUTS</span></span>

### <span data-ttu-id="3a97d-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="3a97d-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="3a97d-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a97d-142">OUTPUTS</span></span>

### <span data-ttu-id="3a97d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a97d-143">System.Boolean</span></span>

## <span data-ttu-id="3a97d-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a97d-144">NOTES</span></span>

<span data-ttu-id="3a97d-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3a97d-145">ALIASES</span></span>

<span data-ttu-id="3a97d-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="3a97d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a97d-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a97d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a97d-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a97d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a97d-149">INPUTOBJECT <IMariaDbIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="3a97d-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a97d-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="3a97d-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3a97d-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3a97d-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3a97d-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="3a97d-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3a97d-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="3a97d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a97d-154">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="3a97d-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3a97d-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="3a97d-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3a97d-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="3a97d-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3a97d-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="3a97d-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3a97d-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3a97d-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3a97d-159">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3a97d-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="3a97d-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3a97d-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3a97d-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a97d-161">RELATED LINKS</span></span>

