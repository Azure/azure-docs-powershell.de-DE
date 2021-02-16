---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146308"
---
# <span data-ttu-id="7a279-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a279-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="7a279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a279-102">SYNOPSIS</span></span>
<span data-ttu-id="7a279-103">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="7a279-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="7a279-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a279-104">SYNTAX</span></span>

### <span data-ttu-id="7a279-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a279-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7a279-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="7a279-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7a279-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7a279-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7a279-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7a279-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7a279-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a279-109">DESCRIPTION</span></span>
<span data-ttu-id="7a279-110">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="7a279-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="7a279-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a279-111">EXAMPLES</span></span>

### <span data-ttu-id="7a279-112">Beispiel 1: Aktualisieren der PostgreSql-Firewallregel nach Name</span><span class="sxs-lookup"><span data-stu-id="7a279-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="7a279-113">Dieses Cmdlet aktualisiert die PostgreSql-Firewallregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="7a279-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="7a279-114">Beispiel 2: Aktualisieren der PostgreSql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="7a279-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="7a279-115">Diese Cmdlets aktualisieren die PostgreSql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="7a279-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="7a279-116">Beispiel 3: Aktualisieren der PostgreSql-Firewallregel von "-ClientIPAddress".</span><span class="sxs-lookup"><span data-stu-id="7a279-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="7a279-117">Diese Cmdlets aktualisieren die PostgreSql-Firewallregel von "-ClientIPAddress".</span><span class="sxs-lookup"><span data-stu-id="7a279-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="7a279-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a279-118">PARAMETERS</span></span>

### <span data-ttu-id="7a279-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a279-119">-AsJob</span></span>
<span data-ttu-id="7a279-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7a279-120">Run the command as a job</span></span>

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

### <span data-ttu-id="7a279-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="7a279-121">-ClientIPAddress</span></span>
<span data-ttu-id="7a279-122">Vom Client angegebene einzelne IP der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="7a279-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="7a279-123">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="7a279-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7a279-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a279-124">-DefaultProfile</span></span>
<span data-ttu-id="7a279-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a279-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a279-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="7a279-126">-EndIPAddress</span></span>
<span data-ttu-id="7a279-127">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="7a279-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="7a279-128">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="7a279-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7a279-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a279-129">-InputObject</span></span>
<span data-ttu-id="7a279-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7a279-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7a279-131">-Name</span><span class="sxs-lookup"><span data-stu-id="7a279-131">-Name</span></span>
<span data-ttu-id="7a279-132">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="7a279-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="7a279-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7a279-133">-NoWait</span></span>
<span data-ttu-id="7a279-134">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7a279-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7a279-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a279-135">-ResourceGroupName</span></span>
<span data-ttu-id="7a279-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7a279-136">The name of the resource group.</span></span>
<span data-ttu-id="7a279-137">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a279-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7a279-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a279-138">-ServerName</span></span>
<span data-ttu-id="7a279-139">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="7a279-139">The name of the server.</span></span>

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

### <span data-ttu-id="7a279-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="7a279-140">-StartIPAddress</span></span>
<span data-ttu-id="7a279-141">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="7a279-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="7a279-142">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="7a279-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="7a279-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a279-143">-SubscriptionId</span></span>
<span data-ttu-id="7a279-144">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7a279-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7a279-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a279-145">-Confirm</span></span>
<span data-ttu-id="7a279-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a279-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a279-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7a279-147">-WhatIf</span></span>
<span data-ttu-id="7a279-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a279-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a279-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a279-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a279-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a279-150">CommonParameters</span></span>
<span data-ttu-id="7a279-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a279-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a279-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a279-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a279-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a279-153">INPUTS</span></span>

### <span data-ttu-id="7a279-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7a279-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="7a279-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a279-155">OUTPUTS</span></span>

### <span data-ttu-id="7a279-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a279-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="7a279-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a279-157">NOTES</span></span>

<span data-ttu-id="7a279-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7a279-158">ALIASES</span></span>

<span data-ttu-id="7a279-159">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7a279-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a279-160">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7a279-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a279-161">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a279-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a279-162">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7a279-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7a279-163">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7a279-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7a279-164">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7a279-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7a279-165">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="7a279-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7a279-166">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7a279-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7a279-167">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="7a279-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7a279-168">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7a279-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7a279-169">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a279-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="7a279-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7a279-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7a279-171">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="7a279-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7a279-172">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7a279-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7a279-173">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7a279-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7a279-174">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a279-174">RELATED LINKS</span></span>

