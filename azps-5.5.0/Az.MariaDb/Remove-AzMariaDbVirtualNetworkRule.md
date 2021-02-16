---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170352"
---
# <span data-ttu-id="15601-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="15601-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="15601-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15601-102">SYNOPSIS</span></span>
<span data-ttu-id="15601-103">Löscht die Regel für das virtuelle Netzwerk mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="15601-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="15601-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15601-104">SYNTAX</span></span>

### <span data-ttu-id="15601-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="15601-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="15601-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15601-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15601-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15601-107">DESCRIPTION</span></span>
<span data-ttu-id="15601-108">Löscht die Regel für das virtuelle Netzwerk mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="15601-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="15601-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15601-109">EXAMPLES</span></span>

### <span data-ttu-id="15601-110">Beispiel 1: Entfernen einer Regel für ein virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="15601-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="15601-111">Mit diesem Befehl wird eine Regel für ein virtuelles Netzwerk entfernt.</span><span class="sxs-lookup"><span data-stu-id="15601-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="15601-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15601-112">PARAMETERS</span></span>

### <span data-ttu-id="15601-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15601-113">-AsJob</span></span>
<span data-ttu-id="15601-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="15601-114">Run the command as a job</span></span>

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

### <span data-ttu-id="15601-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15601-115">-DefaultProfile</span></span>
<span data-ttu-id="15601-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15601-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15601-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15601-117">-InputObject</span></span>
<span data-ttu-id="15601-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="15601-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15601-119">-Name</span><span class="sxs-lookup"><span data-stu-id="15601-119">-Name</span></span>
<span data-ttu-id="15601-120">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="15601-120">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="15601-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="15601-121">-NoWait</span></span>
<span data-ttu-id="15601-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="15601-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="15601-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15601-123">-PassThru</span></span>
<span data-ttu-id="15601-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="15601-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="15601-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15601-125">-ResourceGroupName</span></span>
<span data-ttu-id="15601-126">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="15601-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="15601-127">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="15601-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="15601-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="15601-128">-ServerName</span></span>
<span data-ttu-id="15601-129">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="15601-129">The name of the server.</span></span>

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

### <span data-ttu-id="15601-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15601-130">-SubscriptionId</span></span>
<span data-ttu-id="15601-131">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="15601-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="15601-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15601-132">-Confirm</span></span>
<span data-ttu-id="15601-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15601-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15601-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="15601-134">-WhatIf</span></span>
<span data-ttu-id="15601-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15601-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15601-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15601-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15601-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15601-137">CommonParameters</span></span>
<span data-ttu-id="15601-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15601-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15601-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15601-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15601-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15601-140">INPUTS</span></span>

### <span data-ttu-id="15601-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="15601-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="15601-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15601-142">OUTPUTS</span></span>

### <span data-ttu-id="15601-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="15601-143">System.Boolean</span></span>

## <span data-ttu-id="15601-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="15601-144">NOTES</span></span>

<span data-ttu-id="15601-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="15601-145">ALIASES</span></span>

<span data-ttu-id="15601-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="15601-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15601-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="15601-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15601-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="15601-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15601-149">INPUTOBJECT <IMariaDbIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="15601-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15601-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="15601-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="15601-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="15601-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="15601-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="15601-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="15601-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="15601-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15601-154">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="15601-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="15601-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="15601-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="15601-156">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="15601-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="15601-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="15601-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="15601-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="15601-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="15601-159">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="15601-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="15601-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="15601-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="15601-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="15601-161">RELATED LINKS</span></span>

