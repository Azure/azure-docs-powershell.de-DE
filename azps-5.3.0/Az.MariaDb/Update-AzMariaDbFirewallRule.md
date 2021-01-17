---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469396"
---
# <span data-ttu-id="66813-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="66813-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="66813-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66813-102">SYNOPSIS</span></span>
<span data-ttu-id="66813-103">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="66813-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="66813-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66813-104">SYNTAX</span></span>

### <span data-ttu-id="66813-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="66813-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="66813-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="66813-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="66813-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="66813-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="66813-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="66813-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="66813-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66813-109">DESCRIPTION</span></span>
<span data-ttu-id="66813-110">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="66813-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="66813-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66813-111">EXAMPLES</span></span>

### <span data-ttu-id="66813-112">Beispiel 1: Aktualisieren der Firewallregel "MariaDB"</span><span class="sxs-lookup"><span data-stu-id="66813-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="66813-113">Mit diesem Befehl wird eine Firewallregel für MariaDB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="66813-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="66813-114">Beispiel 2: Aktualisieren der MariaDB-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="66813-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="66813-115">Das Cmdlet aktualisiert die MariaDB-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="66813-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="66813-116">Beispiel 3: Aktualisieren der MariaDB-Firewallregel nach "-ClientIPAddress".</span><span class="sxs-lookup"><span data-stu-id="66813-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="66813-117">Das Cmdlet aktualisiert die MariaDB-Firewallregel von "-ClientIPAddress".</span><span class="sxs-lookup"><span data-stu-id="66813-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="66813-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66813-118">PARAMETERS</span></span>

### <span data-ttu-id="66813-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66813-119">-AsJob</span></span>
<span data-ttu-id="66813-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="66813-120">Run the command as a job</span></span>

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

### <span data-ttu-id="66813-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="66813-121">-ClientIPAddress</span></span>
<span data-ttu-id="66813-122">Vom Client angegebene einzelne IP der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="66813-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="66813-123">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="66813-123">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66813-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66813-124">-DefaultProfile</span></span>
<span data-ttu-id="66813-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66813-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66813-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="66813-126">-EndIPAddress</span></span>
<span data-ttu-id="66813-127">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="66813-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="66813-128">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="66813-128">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66813-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66813-129">-InputObject</span></span>
<span data-ttu-id="66813-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="66813-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66813-131">-Name</span><span class="sxs-lookup"><span data-stu-id="66813-131">-Name</span></span>
<span data-ttu-id="66813-132">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="66813-132">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66813-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="66813-133">-NoWait</span></span>
<span data-ttu-id="66813-134">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="66813-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="66813-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66813-135">-ResourceGroupName</span></span>
<span data-ttu-id="66813-136">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="66813-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="66813-137">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="66813-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66813-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66813-138">-ServerName</span></span>
<span data-ttu-id="66813-139">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="66813-139">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66813-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="66813-140">-StartIPAddress</span></span>
<span data-ttu-id="66813-141">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="66813-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="66813-142">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="66813-142">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66813-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66813-143">-SubscriptionId</span></span>
<span data-ttu-id="66813-144">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="66813-144">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66813-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66813-145">-Confirm</span></span>
<span data-ttu-id="66813-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66813-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66813-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="66813-147">-WhatIf</span></span>
<span data-ttu-id="66813-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66813-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66813-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66813-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66813-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66813-150">CommonParameters</span></span>
<span data-ttu-id="66813-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66813-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66813-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66813-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66813-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66813-153">INPUTS</span></span>

### <span data-ttu-id="66813-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="66813-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="66813-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66813-155">OUTPUTS</span></span>

### <span data-ttu-id="66813-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="66813-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="66813-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="66813-157">NOTES</span></span>

<span data-ttu-id="66813-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="66813-158">ALIASES</span></span>

<span data-ttu-id="66813-159">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="66813-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="66813-160">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="66813-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66813-161">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66813-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="66813-162">INPUTOBJECT <IMariaDbIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="66813-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66813-163">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="66813-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="66813-164">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="66813-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="66813-165">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="66813-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="66813-166">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="66813-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66813-167">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="66813-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="66813-168">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="66813-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="66813-169">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="66813-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="66813-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="66813-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="66813-171">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="66813-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="66813-172">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="66813-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="66813-173">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="66813-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="66813-174">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="66813-174">RELATED LINKS</span></span>

