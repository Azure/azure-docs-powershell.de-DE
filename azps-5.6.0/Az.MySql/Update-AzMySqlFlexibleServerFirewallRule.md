---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 2147921826c6f50882345bc68603b0dae8cb26ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926995"
---
# <span data-ttu-id="dd5b3-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dd5b3-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="dd5b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd5b3-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5b3-103">Aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="dd5b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd5b3-104">SYNTAX</span></span>

### <span data-ttu-id="dd5b3-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd5b3-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd5b3-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="dd5b3-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd5b3-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dd5b3-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd5b3-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dd5b3-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dd5b3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd5b3-109">DESCRIPTION</span></span>
<span data-ttu-id="dd5b3-110">Aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="dd5b3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd5b3-111">EXAMPLES</span></span>

### <span data-ttu-id="dd5b3-112">Beispiel 1: Aktualisieren der MySql-Firewallregel nach Name</span><span class="sxs-lookup"><span data-stu-id="dd5b3-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="dd5b3-113">Dieses Cmdlet aktualisiert die MySql-Firewallregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="dd5b3-114">Beispiel 2: Aktualisieren der MySql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="dd5b3-115">Diese Cmdlets aktualisieren die MySql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="dd5b3-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dd5b3-116">PARAMETERS</span></span>

### <span data-ttu-id="dd5b3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd5b3-117">-AsJob</span></span>
<span data-ttu-id="dd5b3-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="dd5b3-118">Run the command as a job</span></span>

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

### <span data-ttu-id="dd5b3-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="dd5b3-119">-ClientIPAddress</span></span>
<span data-ttu-id="dd5b3-120">Client hat einzelne IP der Serverfirewallregel angegeben.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="dd5b3-121">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="dd5b3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5b3-122">-DefaultProfile</span></span>
<span data-ttu-id="dd5b3-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd5b3-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="dd5b3-124">-EndIPAddress</span></span>
<span data-ttu-id="dd5b3-125">Die End-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="dd5b3-126">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="dd5b3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd5b3-127">-InputObject</span></span>
<span data-ttu-id="dd5b3-128">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dd5b3-129">-Name</span><span class="sxs-lookup"><span data-stu-id="dd5b3-129">-Name</span></span>
<span data-ttu-id="dd5b3-130">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="dd5b3-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dd5b3-131">-NoWait</span></span>
<span data-ttu-id="dd5b3-132">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="dd5b3-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dd5b3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd5b3-133">-ResourceGroupName</span></span>
<span data-ttu-id="dd5b3-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-134">The name of the resource group.</span></span>
<span data-ttu-id="dd5b3-135">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dd5b3-136">-Servername</span><span class="sxs-lookup"><span data-stu-id="dd5b3-136">-ServerName</span></span>
<span data-ttu-id="dd5b3-137">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-137">The name of the server.</span></span>

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

### <span data-ttu-id="dd5b3-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="dd5b3-138">-StartIPAddress</span></span>
<span data-ttu-id="dd5b3-139">Die Start-IP-Adresse der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="dd5b3-140">Muss das IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="dd5b3-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd5b3-141">-SubscriptionId</span></span>
<span data-ttu-id="dd5b3-142">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dd5b3-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd5b3-143">-Confirm</span></span>
<span data-ttu-id="dd5b3-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd5b3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd5b3-145">-WhatIf</span></span>
<span data-ttu-id="dd5b3-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd5b3-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd5b3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5b3-148">CommonParameters</span></span>
<span data-ttu-id="dd5b3-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5b3-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd5b3-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5b3-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd5b3-151">INPUTS</span></span>

### <span data-ttu-id="dd5b3-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="dd5b3-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="dd5b3-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd5b3-153">OUTPUTS</span></span>

### <span data-ttu-id="dd5b3-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dd5b3-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="dd5b3-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dd5b3-155">NOTES</span></span>

<span data-ttu-id="dd5b3-156">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dd5b3-156">ALIASES</span></span>

<span data-ttu-id="dd5b3-157">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="dd5b3-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd5b3-158">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd5b3-159">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd5b3-160">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="dd5b3-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd5b3-161">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dd5b3-162">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dd5b3-163">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dd5b3-164">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="dd5b3-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd5b3-165">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="dd5b3-166">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dd5b3-167">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dd5b3-168">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="dd5b3-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dd5b3-170">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dd5b3-171">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dd5b3-172">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dd5b3-173">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dd5b3-173">RELATED LINKS</span></span>

