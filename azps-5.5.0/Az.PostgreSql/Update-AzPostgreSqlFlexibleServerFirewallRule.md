---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: fe6ef1a5193119c4778d18c39a7ecff98354cf89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172247"
---
# <span data-ttu-id="68dea-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="68dea-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="68dea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68dea-102">SYNOPSIS</span></span>
<span data-ttu-id="68dea-103">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="68dea-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="68dea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68dea-104">SYNTAX</span></span>

### <span data-ttu-id="68dea-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="68dea-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68dea-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="68dea-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68dea-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="68dea-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68dea-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="68dea-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="68dea-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68dea-109">DESCRIPTION</span></span>
<span data-ttu-id="68dea-110">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="68dea-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="68dea-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="68dea-111">EXAMPLES</span></span>

### <span data-ttu-id="68dea-112">Beispiel 1: Aktualisieren der PostgreSql-Firewallregel nach Name</span><span class="sxs-lookup"><span data-stu-id="68dea-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="68dea-113">Dieses Cmdlet aktualisiert die PostgreSql-Firewallregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="68dea-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="68dea-114">Beispiel 2: Aktualisieren der PostgreSql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="68dea-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="68dea-115">Diese Cmdlets aktualisieren die PostgreSql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="68dea-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="68dea-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68dea-116">PARAMETERS</span></span>

### <span data-ttu-id="68dea-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68dea-117">-AsJob</span></span>
<span data-ttu-id="68dea-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="68dea-118">Run the command as a job</span></span>

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

### <span data-ttu-id="68dea-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="68dea-119">-ClientIPAddress</span></span>
<span data-ttu-id="68dea-120">Vom Client angegebene einzelne IP der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="68dea-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="68dea-121">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="68dea-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="68dea-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68dea-122">-DefaultProfile</span></span>
<span data-ttu-id="68dea-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68dea-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68dea-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="68dea-124">-EndIPAddress</span></span>
<span data-ttu-id="68dea-125">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="68dea-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="68dea-126">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="68dea-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="68dea-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68dea-127">-InputObject</span></span>
<span data-ttu-id="68dea-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="68dea-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68dea-129">-Name</span><span class="sxs-lookup"><span data-stu-id="68dea-129">-Name</span></span>
<span data-ttu-id="68dea-130">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="68dea-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="68dea-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="68dea-131">-NoWait</span></span>
<span data-ttu-id="68dea-132">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="68dea-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="68dea-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68dea-133">-ResourceGroupName</span></span>
<span data-ttu-id="68dea-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="68dea-134">The name of the resource group.</span></span>
<span data-ttu-id="68dea-135">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="68dea-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="68dea-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="68dea-136">-ServerName</span></span>
<span data-ttu-id="68dea-137">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="68dea-137">The name of the server.</span></span>

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

### <span data-ttu-id="68dea-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="68dea-138">-StartIPAddress</span></span>
<span data-ttu-id="68dea-139">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="68dea-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="68dea-140">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="68dea-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="68dea-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68dea-141">-SubscriptionId</span></span>
<span data-ttu-id="68dea-142">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="68dea-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="68dea-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68dea-143">-Confirm</span></span>
<span data-ttu-id="68dea-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68dea-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68dea-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="68dea-145">-WhatIf</span></span>
<span data-ttu-id="68dea-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68dea-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68dea-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68dea-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68dea-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68dea-148">CommonParameters</span></span>
<span data-ttu-id="68dea-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68dea-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68dea-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68dea-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68dea-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="68dea-151">INPUTS</span></span>

### <span data-ttu-id="68dea-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="68dea-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="68dea-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="68dea-153">OUTPUTS</span></span>

### <span data-ttu-id="68dea-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="68dea-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="68dea-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="68dea-155">NOTES</span></span>

<span data-ttu-id="68dea-156">ALIASE</span><span class="sxs-lookup"><span data-stu-id="68dea-156">ALIASES</span></span>

<span data-ttu-id="68dea-157">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="68dea-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68dea-158">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="68dea-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68dea-159">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68dea-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68dea-160">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="68dea-160">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="68dea-161">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="68dea-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="68dea-162">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="68dea-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="68dea-163">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="68dea-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="68dea-164">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="68dea-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="68dea-165">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="68dea-165">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="68dea-166">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="68dea-166">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="68dea-167">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="68dea-167">The name is case insensitive.</span></span>
  - <span data-ttu-id="68dea-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="68dea-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="68dea-169">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="68dea-169">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="68dea-170">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="68dea-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="68dea-171">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="68dea-171">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="68dea-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="68dea-172">RELATED LINKS</span></span>

