---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 5df722564e899d46a1f68bf8e88ecdaa2b792121
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467511"
---
# <span data-ttu-id="132ff-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="132ff-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="132ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="132ff-102">SYNOPSIS</span></span>
<span data-ttu-id="132ff-103">Aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="132ff-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="132ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="132ff-104">SYNTAX</span></span>

### <span data-ttu-id="132ff-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="132ff-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="132ff-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="132ff-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="132ff-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="132ff-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="132ff-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="132ff-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="132ff-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="132ff-109">DESCRIPTION</span></span>
<span data-ttu-id="132ff-110">Aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="132ff-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="132ff-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="132ff-111">EXAMPLES</span></span>

### <span data-ttu-id="132ff-112">Beispiel 1: Aktualisieren der MySql-Firewallregel nach Name</span><span class="sxs-lookup"><span data-stu-id="132ff-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="132ff-113">Dieses Cmdlet aktualisiert die MySql-Firewallregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="132ff-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="132ff-114">Beispiel 2: Aktualisieren der MySql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="132ff-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="132ff-115">Diese Cmdlets aktualisieren die MySql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="132ff-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="132ff-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="132ff-116">PARAMETERS</span></span>

### <span data-ttu-id="132ff-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="132ff-117">-AsJob</span></span>
<span data-ttu-id="132ff-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="132ff-118">Run the command as a job</span></span>

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

### <span data-ttu-id="132ff-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="132ff-119">-ClientIPAddress</span></span>
<span data-ttu-id="132ff-120">Vom Client angegebene einzelne IP der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="132ff-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="132ff-121">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="132ff-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="132ff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="132ff-122">-DefaultProfile</span></span>
<span data-ttu-id="132ff-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="132ff-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="132ff-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="132ff-124">-EndIPAddress</span></span>
<span data-ttu-id="132ff-125">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="132ff-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="132ff-126">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="132ff-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="132ff-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="132ff-127">-InputObject</span></span>
<span data-ttu-id="132ff-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="132ff-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="132ff-129">-Name</span><span class="sxs-lookup"><span data-stu-id="132ff-129">-Name</span></span>
<span data-ttu-id="132ff-130">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="132ff-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="132ff-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="132ff-131">-NoWait</span></span>
<span data-ttu-id="132ff-132">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="132ff-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="132ff-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="132ff-133">-ResourceGroupName</span></span>
<span data-ttu-id="132ff-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="132ff-134">The name of the resource group.</span></span>
<span data-ttu-id="132ff-135">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="132ff-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="132ff-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="132ff-136">-ServerName</span></span>
<span data-ttu-id="132ff-137">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="132ff-137">The name of the server.</span></span>

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

### <span data-ttu-id="132ff-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="132ff-138">-StartIPAddress</span></span>
<span data-ttu-id="132ff-139">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="132ff-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="132ff-140">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="132ff-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="132ff-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="132ff-141">-SubscriptionId</span></span>
<span data-ttu-id="132ff-142">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="132ff-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="132ff-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="132ff-143">-Confirm</span></span>
<span data-ttu-id="132ff-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="132ff-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="132ff-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="132ff-145">-WhatIf</span></span>
<span data-ttu-id="132ff-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="132ff-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="132ff-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="132ff-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="132ff-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="132ff-148">CommonParameters</span></span>
<span data-ttu-id="132ff-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="132ff-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="132ff-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="132ff-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="132ff-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="132ff-151">INPUTS</span></span>

### <span data-ttu-id="132ff-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="132ff-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="132ff-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="132ff-153">OUTPUTS</span></span>

### <span data-ttu-id="132ff-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="132ff-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="132ff-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="132ff-155">NOTES</span></span>

<span data-ttu-id="132ff-156">ALIASE</span><span class="sxs-lookup"><span data-stu-id="132ff-156">ALIASES</span></span>

<span data-ttu-id="132ff-157">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="132ff-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="132ff-158">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="132ff-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="132ff-159">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="132ff-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="132ff-160">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="132ff-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="132ff-161">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="132ff-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="132ff-162">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="132ff-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="132ff-163">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="132ff-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="132ff-164">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="132ff-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="132ff-165">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="132ff-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="132ff-166">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="132ff-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="132ff-167">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="132ff-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="132ff-168">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="132ff-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="132ff-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="132ff-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="132ff-170">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="132ff-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="132ff-171">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="132ff-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="132ff-172">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="132ff-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="132ff-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="132ff-173">RELATED LINKS</span></span>

