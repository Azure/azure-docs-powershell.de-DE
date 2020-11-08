---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 979fc45bb7bdfe36133404a88a646a871cb33301
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009182"
---
# <span data-ttu-id="9cd60-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9cd60-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="9cd60-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9cd60-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd60-103">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="9cd60-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="9cd60-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cd60-104">SYNTAX</span></span>

### <span data-ttu-id="9cd60-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="9cd60-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9cd60-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9cd60-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9cd60-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9cd60-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9cd60-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9cd60-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9cd60-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cd60-109">DESCRIPTION</span></span>
<span data-ttu-id="9cd60-110">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="9cd60-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="9cd60-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cd60-111">EXAMPLES</span></span>

### <span data-ttu-id="9cd60-112">Beispiel 1: Aktualisieren der MySQL-Firewall-Regel nach Namen</span><span class="sxs-lookup"><span data-stu-id="9cd60-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="9cd60-113">Dieses Cmdlet aktualisiert die MySQL-Firewall-Regel nach Namen.</span><span class="sxs-lookup"><span data-stu-id="9cd60-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="9cd60-114">Beispiel 2: Aktualisieren der MySQL-Firewall-Regel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="9cd60-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="9cd60-115">Diese Cmdlets aktualisieren die MySQL-Firewall-Regel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="9cd60-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="9cd60-116">Beispiel 3: Aktualisieren der MySQL-Firewall-Regel by-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9cd60-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="9cd60-117">Diese Cmdlets aktualisieren die MySQL-Firewall-Regel ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="9cd60-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="9cd60-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cd60-118">PARAMETERS</span></span>

### <span data-ttu-id="9cd60-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cd60-119">-AsJob</span></span>
<span data-ttu-id="9cd60-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="9cd60-120">Run the command as a job</span></span>

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

### <span data-ttu-id="9cd60-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9cd60-121">-ClientIPAddress</span></span>
<span data-ttu-id="9cd60-122">Client hat eine einzelne IP-Adresse der Server Firewall-Regel angegeben.</span><span class="sxs-lookup"><span data-stu-id="9cd60-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="9cd60-123">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="9cd60-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9cd60-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd60-124">-DefaultProfile</span></span>
<span data-ttu-id="9cd60-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9cd60-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cd60-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="9cd60-126">-EndIPAddress</span></span>
<span data-ttu-id="9cd60-127">Die End-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="9cd60-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="9cd60-128">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="9cd60-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9cd60-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9cd60-129">-InputObject</span></span>
<span data-ttu-id="9cd60-130">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9cd60-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9cd60-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9cd60-131">-Name</span></span>
<span data-ttu-id="9cd60-132">Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="9cd60-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="9cd60-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9cd60-133">-NoWait</span></span>
<span data-ttu-id="9cd60-134">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="9cd60-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9cd60-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd60-135">-ResourceGroupName</span></span>
<span data-ttu-id="9cd60-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9cd60-136">The name of the resource group.</span></span>
<span data-ttu-id="9cd60-137">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="9cd60-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9cd60-138">-Servername</span><span class="sxs-lookup"><span data-stu-id="9cd60-138">-ServerName</span></span>
<span data-ttu-id="9cd60-139">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="9cd60-139">The name of the server.</span></span>

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

### <span data-ttu-id="9cd60-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="9cd60-140">-StartIPAddress</span></span>
<span data-ttu-id="9cd60-141">Die Start-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="9cd60-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="9cd60-142">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="9cd60-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9cd60-143">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9cd60-143">-SubscriptionId</span></span>
<span data-ttu-id="9cd60-144">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="9cd60-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9cd60-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9cd60-145">-Confirm</span></span>
<span data-ttu-id="9cd60-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9cd60-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cd60-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd60-147">-WhatIf</span></span>
<span data-ttu-id="9cd60-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9cd60-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cd60-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9cd60-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cd60-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd60-150">CommonParameters</span></span>
<span data-ttu-id="9cd60-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd60-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd60-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cd60-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd60-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9cd60-153">INPUTS</span></span>

### <span data-ttu-id="9cd60-154">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9cd60-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9cd60-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9cd60-155">OUTPUTS</span></span>

### <span data-ttu-id="9cd60-156">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9cd60-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="9cd60-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="9cd60-157">NOTES</span></span>

<span data-ttu-id="9cd60-158">Aliase</span><span class="sxs-lookup"><span data-stu-id="9cd60-158">ALIASES</span></span>

<span data-ttu-id="9cd60-159">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9cd60-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9cd60-160">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9cd60-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9cd60-161">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="9cd60-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9cd60-162">Inputobject <IMySqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9cd60-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9cd60-163">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="9cd60-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9cd60-164">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9cd60-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9cd60-165">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="9cd60-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9cd60-166">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="9cd60-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9cd60-167">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="9cd60-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9cd60-168">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9cd60-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9cd60-169">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="9cd60-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="9cd60-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9cd60-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9cd60-171">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="9cd60-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9cd60-172">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="9cd60-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9cd60-173">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9cd60-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9cd60-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9cd60-174">RELATED LINKS</span></span>

