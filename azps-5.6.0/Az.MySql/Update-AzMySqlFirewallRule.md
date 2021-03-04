---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 314d8016f96d76546e0f2afee163bb5cb911ff0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927024"
---
# <span data-ttu-id="b653a-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b653a-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="b653a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b653a-102">SYNOPSIS</span></span>
<span data-ttu-id="b653a-103">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="b653a-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b653a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b653a-104">SYNTAX</span></span>

### <span data-ttu-id="b653a-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="b653a-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b653a-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b653a-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b653a-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b653a-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b653a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b653a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b653a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b653a-109">DESCRIPTION</span></span>
<span data-ttu-id="b653a-110">Erstellt eine neue Firewallregel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="b653a-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b653a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b653a-111">EXAMPLES</span></span>

### <span data-ttu-id="b653a-112">Beispiel 1: Aktualisieren der MySql-Firewallregel nach Name</span><span class="sxs-lookup"><span data-stu-id="b653a-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b653a-113">Dieses Cmdlet aktualisiert die MySql-Firewallregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="b653a-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="b653a-114">Beispiel 2: Aktualisieren der MySql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="b653a-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b653a-115">Diese Cmdlets aktualisieren die MySql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="b653a-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="b653a-116">Beispiel 3: Aktualisieren der MySql-Firewallregel durch -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="b653a-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="b653a-117">Diese Cmdlets aktualisieren die MySql-Firewallregel durch -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="b653a-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="b653a-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b653a-118">PARAMETERS</span></span>

### <span data-ttu-id="b653a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b653a-119">-AsJob</span></span>
<span data-ttu-id="b653a-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b653a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b653a-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b653a-121">-ClientIPAddress</span></span>
<span data-ttu-id="b653a-122">Client hat einzelne IP der Serverfirewallregel angegeben.</span><span class="sxs-lookup"><span data-stu-id="b653a-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b653a-123">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="b653a-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b653a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b653a-124">-DefaultProfile</span></span>
<span data-ttu-id="b653a-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b653a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b653a-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b653a-126">-EndIPAddress</span></span>
<span data-ttu-id="b653a-127">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="b653a-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b653a-128">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="b653a-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b653a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b653a-129">-InputObject</span></span>
<span data-ttu-id="b653a-130">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b653a-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b653a-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b653a-131">-Name</span></span>
<span data-ttu-id="b653a-132">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="b653a-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b653a-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b653a-133">-NoWait</span></span>
<span data-ttu-id="b653a-134">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b653a-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b653a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b653a-135">-ResourceGroupName</span></span>
<span data-ttu-id="b653a-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b653a-136">The name of the resource group.</span></span>
<span data-ttu-id="b653a-137">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="b653a-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b653a-138">-Servername</span><span class="sxs-lookup"><span data-stu-id="b653a-138">-ServerName</span></span>
<span data-ttu-id="b653a-139">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="b653a-139">The name of the server.</span></span>

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

### <span data-ttu-id="b653a-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b653a-140">-StartIPAddress</span></span>
<span data-ttu-id="b653a-141">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="b653a-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b653a-142">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="b653a-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b653a-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b653a-143">-SubscriptionId</span></span>
<span data-ttu-id="b653a-144">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="b653a-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b653a-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b653a-145">-Confirm</span></span>
<span data-ttu-id="b653a-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b653a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b653a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b653a-147">-WhatIf</span></span>
<span data-ttu-id="b653a-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b653a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b653a-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b653a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b653a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b653a-150">CommonParameters</span></span>
<span data-ttu-id="b653a-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b653a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b653a-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b653a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b653a-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b653a-153">INPUTS</span></span>

### <span data-ttu-id="b653a-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b653a-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b653a-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b653a-155">OUTPUTS</span></span>

### <span data-ttu-id="b653a-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b653a-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="b653a-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b653a-157">NOTES</span></span>

<span data-ttu-id="b653a-158">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b653a-158">ALIASES</span></span>

<span data-ttu-id="b653a-159">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b653a-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b653a-160">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b653a-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b653a-161">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b653a-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b653a-162">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="b653a-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b653a-163">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b653a-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b653a-164">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b653a-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b653a-165">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="b653a-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b653a-166">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b653a-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b653a-167">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="b653a-167">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b653a-168">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="b653a-168">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b653a-169">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b653a-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b653a-170">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="b653a-170">The name is case insensitive.</span></span>
  - <span data-ttu-id="b653a-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b653a-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b653a-172">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="b653a-172">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b653a-173">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="b653a-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b653a-174">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="b653a-174">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b653a-175">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b653a-175">RELATED LINKS</span></span>

