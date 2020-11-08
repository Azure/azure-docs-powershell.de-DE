---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166329"
---
# <span data-ttu-id="9beab-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9beab-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="9beab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9beab-102">SYNOPSIS</span></span>
<span data-ttu-id="9beab-103">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="9beab-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="9beab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9beab-104">SYNTAX</span></span>

### <span data-ttu-id="9beab-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="9beab-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9beab-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9beab-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9beab-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9beab-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9beab-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9beab-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9beab-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9beab-109">DESCRIPTION</span></span>
<span data-ttu-id="9beab-110">Erstellt eine neue Firewall-Regel oder aktualisiert eine vorhandene Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="9beab-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="9beab-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9beab-111">EXAMPLES</span></span>

### <span data-ttu-id="9beab-112">Beispiel 1: Aktualisieren der MariaDB-Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="9beab-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="9beab-113">Mit diesem Befehl wird eine MariaDB-Firewallregel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9beab-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="9beab-114">Beispiel 2: Aktualisieren der MariaDB-Firewall-Regel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="9beab-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="9beab-115">Das Cmdlet aktualisiert die MariaDB-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="9beab-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="9beab-116">Beispiel 3: Aktualisieren der MariaDB-Firewall-Regel by-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9beab-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="9beab-117">Das Cmdlet aktualisiert die MariaDB-Firewall-Regel nach-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="9beab-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="9beab-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="9beab-118">PARAMETERS</span></span>

### <span data-ttu-id="9beab-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9beab-119">-AsJob</span></span>
<span data-ttu-id="9beab-120">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="9beab-120">Run the command as a job</span></span>

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

### <span data-ttu-id="9beab-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9beab-121">-ClientIPAddress</span></span>
<span data-ttu-id="9beab-122">Client hat eine einzelne IP-Adresse der Server Firewall-Regel angegeben.</span><span class="sxs-lookup"><span data-stu-id="9beab-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="9beab-123">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="9beab-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9beab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9beab-124">-DefaultProfile</span></span>
<span data-ttu-id="9beab-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9beab-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9beab-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="9beab-126">-EndIPAddress</span></span>
<span data-ttu-id="9beab-127">Die End-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="9beab-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="9beab-128">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="9beab-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9beab-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9beab-129">-InputObject</span></span>
<span data-ttu-id="9beab-130">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9beab-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9beab-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9beab-131">-Name</span></span>
<span data-ttu-id="9beab-132">Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="9beab-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="9beab-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9beab-133">-NoWait</span></span>
<span data-ttu-id="9beab-134">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="9beab-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9beab-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9beab-135">-ResourceGroupName</span></span>
<span data-ttu-id="9beab-136">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="9beab-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9beab-137">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="9beab-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9beab-138">-Servername</span><span class="sxs-lookup"><span data-stu-id="9beab-138">-ServerName</span></span>
<span data-ttu-id="9beab-139">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="9beab-139">The name of the server.</span></span>

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

### <span data-ttu-id="9beab-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="9beab-140">-StartIPAddress</span></span>
<span data-ttu-id="9beab-141">Die Start-IP-Adresse der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="9beab-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="9beab-142">Muss ein IPv4-Format sein.</span><span class="sxs-lookup"><span data-stu-id="9beab-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9beab-143">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9beab-143">-SubscriptionId</span></span>
<span data-ttu-id="9beab-144">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9beab-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="9beab-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9beab-145">-Confirm</span></span>
<span data-ttu-id="9beab-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9beab-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9beab-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9beab-147">-WhatIf</span></span>
<span data-ttu-id="9beab-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9beab-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9beab-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9beab-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9beab-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9beab-150">CommonParameters</span></span>
<span data-ttu-id="9beab-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9beab-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9beab-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9beab-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9beab-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9beab-153">INPUTS</span></span>

### <span data-ttu-id="9beab-154">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="9beab-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="9beab-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9beab-155">OUTPUTS</span></span>

### <span data-ttu-id="9beab-156">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9beab-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="9beab-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="9beab-157">NOTES</span></span>

<span data-ttu-id="9beab-158">Aliase</span><span class="sxs-lookup"><span data-stu-id="9beab-158">ALIASES</span></span>

<span data-ttu-id="9beab-159">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9beab-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9beab-160">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9beab-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9beab-161">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="9beab-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9beab-162">Inputobject <IMariaDbIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9beab-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9beab-163">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="9beab-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9beab-164">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9beab-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9beab-165">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="9beab-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9beab-166">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="9beab-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9beab-167">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="9beab-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9beab-168">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="9beab-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9beab-169">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="9beab-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9beab-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="9beab-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9beab-171">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="9beab-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9beab-172">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9beab-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="9beab-173">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9beab-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9beab-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9beab-174">RELATED LINKS</span></span>

