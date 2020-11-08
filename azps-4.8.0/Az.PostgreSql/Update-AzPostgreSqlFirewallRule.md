---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165040"
---
# <span data-ttu-id="d7685-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d7685-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="d7685-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7685-102">SYNOPSIS</span></span>
<span data-ttu-id="d7685-103">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="d7685-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d7685-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7685-104">SYNTAX</span></span>

### <span data-ttu-id="d7685-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7685-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7685-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d7685-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7685-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d7685-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7685-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d7685-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d7685-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7685-109">DESCRIPTION</span></span>
<span data-ttu-id="d7685-110">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="d7685-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d7685-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7685-111">EXAMPLES</span></span>

### <span data-ttu-id="d7685-112">Beispiel 1: Aktualisieren der PostgreSQL-Firewall-Regel nach Namen</span><span class="sxs-lookup"><span data-stu-id="d7685-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d7685-113">Dieses Cmdlet aktualisiert die Regel der PostgreSQL-Firewall nach Namen.</span><span class="sxs-lookup"><span data-stu-id="d7685-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="d7685-114">Beispiel 2: Aktualisieren der PostgreSQL-Firewall-Regel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="d7685-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="d7685-115">Diese Cmdlets aktualisieren die PostgreSQL-Firewall-Regel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="d7685-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="d7685-116">Beispiel 3: Aktualisieren der PostgreSQL-Firewall-Regel by-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d7685-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="d7685-117">Diese Cmdlets aktualisieren die ClientIPAddress-Regel für die PostgreSQL-Firewall.</span><span class="sxs-lookup"><span data-stu-id="d7685-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="d7685-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7685-118">PARAMETERS</span></span>

### <span data-ttu-id="d7685-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7685-119">-AsJob</span></span>
<span data-ttu-id="d7685-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d7685-120">Run the command as a job</span></span>

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

### <span data-ttu-id="d7685-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d7685-121">-ClientIPAddress</span></span>
<span data-ttu-id="d7685-122">Client hat eine einzelne IP-Adresse der Server Firewall-Regel angegeben.</span><span class="sxs-lookup"><span data-stu-id="d7685-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="d7685-123">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="d7685-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d7685-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7685-124">-DefaultProfile</span></span>
<span data-ttu-id="d7685-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7685-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7685-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="d7685-126">-EndIPAddress</span></span>
<span data-ttu-id="d7685-127">Die End-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="d7685-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="d7685-128">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="d7685-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d7685-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d7685-129">-InputObject</span></span>
<span data-ttu-id="d7685-130">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d7685-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d7685-131">-Name</span><span class="sxs-lookup"><span data-stu-id="d7685-131">-Name</span></span>
<span data-ttu-id="d7685-132">Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="d7685-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="d7685-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d7685-133">-NoWait</span></span>
<span data-ttu-id="d7685-134">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d7685-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d7685-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7685-135">-ResourceGroupName</span></span>
<span data-ttu-id="d7685-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d7685-136">The name of the resource group.</span></span>
<span data-ttu-id="d7685-137">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d7685-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d7685-138">-Servername</span><span class="sxs-lookup"><span data-stu-id="d7685-138">-ServerName</span></span>
<span data-ttu-id="d7685-139">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="d7685-139">The name of the server.</span></span>

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

### <span data-ttu-id="d7685-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="d7685-140">-StartIPAddress</span></span>
<span data-ttu-id="d7685-141">Die Start-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="d7685-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="d7685-142">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="d7685-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d7685-143">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d7685-143">-SubscriptionId</span></span>
<span data-ttu-id="d7685-144">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d7685-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d7685-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7685-145">-Confirm</span></span>
<span data-ttu-id="d7685-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7685-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7685-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7685-147">-WhatIf</span></span>
<span data-ttu-id="d7685-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7685-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7685-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7685-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7685-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7685-150">CommonParameters</span></span>
<span data-ttu-id="d7685-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7685-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7685-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7685-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7685-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7685-153">INPUTS</span></span>

### <span data-ttu-id="d7685-154">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d7685-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d7685-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7685-155">OUTPUTS</span></span>

### <span data-ttu-id="d7685-156">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d7685-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="d7685-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7685-157">NOTES</span></span>

<span data-ttu-id="d7685-158">Aliase</span><span class="sxs-lookup"><span data-stu-id="d7685-158">ALIASES</span></span>

<span data-ttu-id="d7685-159">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7685-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7685-160">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d7685-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7685-161">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d7685-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7685-162">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="d7685-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7685-163">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d7685-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d7685-164">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d7685-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d7685-165">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="d7685-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d7685-166">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="d7685-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7685-167">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="d7685-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d7685-168">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d7685-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d7685-169">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d7685-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="d7685-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d7685-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d7685-171">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="d7685-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d7685-172">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d7685-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d7685-173">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d7685-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d7685-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7685-174">RELATED LINKS</span></span>

