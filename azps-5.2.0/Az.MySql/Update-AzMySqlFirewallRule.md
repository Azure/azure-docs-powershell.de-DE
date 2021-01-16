---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: eb74b9530c9ce196b308a310d5a20642328719e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360252"
---
# <span data-ttu-id="e94e9-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e94e9-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="e94e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e94e9-102">SYNOPSIS</span></span>
<span data-ttu-id="e94e9-103">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="e94e9-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="e94e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e94e9-104">SYNTAX</span></span>

### <span data-ttu-id="e94e9-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="e94e9-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e94e9-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="e94e9-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e94e9-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e94e9-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e94e9-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e94e9-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e94e9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e94e9-109">DESCRIPTION</span></span>
<span data-ttu-id="e94e9-110">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="e94e9-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="e94e9-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e94e9-111">EXAMPLES</span></span>

### <span data-ttu-id="e94e9-112">Beispiel 1: Aktualisieren der MySql-Firewallregel nach Name</span><span class="sxs-lookup"><span data-stu-id="e94e9-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="e94e9-113">Dieses Cmdlet aktualisiert die MySql-Firewallregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="e94e9-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="e94e9-114">Beispiel 2: Aktualisieren der MySql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="e94e9-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="e94e9-115">Diese Cmdlets aktualisieren die MySql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="e94e9-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="e94e9-116">Beispiel 3: Aktualisieren der MySql-Firewallregel durch "-ClientIPAddress".</span><span class="sxs-lookup"><span data-stu-id="e94e9-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="e94e9-117">Diese Cmdlets aktualisieren "MySql-Firewallregel" nach "-ClientIPAddress".</span><span class="sxs-lookup"><span data-stu-id="e94e9-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="e94e9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e94e9-118">PARAMETERS</span></span>

### <span data-ttu-id="e94e9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e94e9-119">-AsJob</span></span>
<span data-ttu-id="e94e9-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e94e9-120">Run the command as a job</span></span>

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

### <span data-ttu-id="e94e9-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="e94e9-121">-ClientIPAddress</span></span>
<span data-ttu-id="e94e9-122">Vom Client angegebene einzelne IP der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="e94e9-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="e94e9-123">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="e94e9-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e94e9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94e9-124">-DefaultProfile</span></span>
<span data-ttu-id="e94e9-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e94e9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e94e9-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="e94e9-126">-EndIPAddress</span></span>
<span data-ttu-id="e94e9-127">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="e94e9-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="e94e9-128">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="e94e9-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e94e9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e94e9-129">-InputObject</span></span>
<span data-ttu-id="e94e9-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e94e9-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e94e9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e94e9-131">-Name</span></span>
<span data-ttu-id="e94e9-132">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="e94e9-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="e94e9-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e94e9-133">-NoWait</span></span>
<span data-ttu-id="e94e9-134">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e94e9-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e94e9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e94e9-135">-ResourceGroupName</span></span>
<span data-ttu-id="e94e9-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e94e9-136">The name of the resource group.</span></span>
<span data-ttu-id="e94e9-137">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="e94e9-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e94e9-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e94e9-138">-ServerName</span></span>
<span data-ttu-id="e94e9-139">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e94e9-139">The name of the server.</span></span>

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

### <span data-ttu-id="e94e9-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="e94e9-140">-StartIPAddress</span></span>
<span data-ttu-id="e94e9-141">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="e94e9-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="e94e9-142">muss im IPv4-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="e94e9-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e94e9-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e94e9-143">-SubscriptionId</span></span>
<span data-ttu-id="e94e9-144">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e94e9-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e94e9-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e94e9-145">-Confirm</span></span>
<span data-ttu-id="e94e9-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e94e9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e94e9-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e94e9-147">-WhatIf</span></span>
<span data-ttu-id="e94e9-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e94e9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94e9-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e94e9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e94e9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94e9-150">CommonParameters</span></span>
<span data-ttu-id="e94e9-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e94e9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94e9-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e94e9-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94e9-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e94e9-153">INPUTS</span></span>

### <span data-ttu-id="e94e9-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e94e9-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="e94e9-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e94e9-155">OUTPUTS</span></span>

### <span data-ttu-id="e94e9-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e94e9-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="e94e9-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e94e9-157">NOTES</span></span>

<span data-ttu-id="e94e9-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e94e9-158">ALIASES</span></span>

<span data-ttu-id="e94e9-159">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e94e9-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e94e9-160">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e94e9-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e94e9-161">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e94e9-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e94e9-162">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e94e9-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e94e9-163">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e94e9-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e94e9-164">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e94e9-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e94e9-165">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="e94e9-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e94e9-166">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e94e9-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e94e9-167">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="e94e9-167">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="e94e9-168">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="e94e9-168">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e94e9-169">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e94e9-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e94e9-170">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="e94e9-170">The name is case insensitive.</span></span>
  - <span data-ttu-id="e94e9-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e94e9-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e94e9-172">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e94e9-172">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e94e9-173">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e94e9-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e94e9-174">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e94e9-174">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e94e9-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e94e9-175">RELATED LINKS</span></span>

