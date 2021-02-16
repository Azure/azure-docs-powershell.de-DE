---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: a4b2f96644a2ec354b38dd13b159bb0f65f008c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146388"
---
# <span data-ttu-id="186f2-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="186f2-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="186f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="186f2-102">SYNOPSIS</span></span>
<span data-ttu-id="186f2-103">Listet alle Firewallregeln auf einem bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="186f2-103">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="186f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="186f2-104">SYNTAX</span></span>

### <span data-ttu-id="186f2-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="186f2-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="186f2-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="186f2-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="186f2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="186f2-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="186f2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="186f2-108">DESCRIPTION</span></span>
<span data-ttu-id="186f2-109">Listet alle Firewallregeln auf einem bestimmten Server auf.</span><span class="sxs-lookup"><span data-stu-id="186f2-109">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="186f2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="186f2-110">EXAMPLES</span></span>

### <span data-ttu-id="186f2-111">Beispiel 1: Erhalten von Firewallregeln nach Name</span><span class="sxs-lookup"><span data-stu-id="186f2-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="186f2-112">Dieses Cmdlet ruft Firewallregeln nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="186f2-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="186f2-113">Beispiel 2: Erhalten von Firewallregeln nach Identität</span><span class="sxs-lookup"><span data-stu-id="186f2-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/servers/postgresql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="186f2-114">Dieses Cmdlet ruft Firewallregeln nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="186f2-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="186f2-115">Beispiel 3: Listet alle Firewallregeln im angegebenen Server von PostgreSql auf.</span><span class="sxs-lookup"><span data-stu-id="186f2-115">Example 3: Lists all the firewall rules in the specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="186f2-116">Dieses Cmdlet listet alle Firewallregeln im angegebenen Server von PostgreSql auf.</span><span class="sxs-lookup"><span data-stu-id="186f2-116">This cmdlet lists all the firewall rule in specified PostgreSql server.</span></span>

## <span data-ttu-id="186f2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="186f2-117">PARAMETERS</span></span>

### <span data-ttu-id="186f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186f2-118">-DefaultProfile</span></span>
<span data-ttu-id="186f2-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="186f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="186f2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="186f2-120">-InputObject</span></span>
<span data-ttu-id="186f2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="186f2-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="186f2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="186f2-122">-Name</span></span>
<span data-ttu-id="186f2-123">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="186f2-123">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="186f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="186f2-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="186f2-125">The name of the resource group.</span></span>
<span data-ttu-id="186f2-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="186f2-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186f2-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="186f2-127">-ServerName</span></span>
<span data-ttu-id="186f2-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="186f2-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186f2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="186f2-129">-SubscriptionId</span></span>
<span data-ttu-id="186f2-130">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="186f2-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186f2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186f2-131">CommonParameters</span></span>
<span data-ttu-id="186f2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="186f2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186f2-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="186f2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186f2-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="186f2-134">INPUTS</span></span>

### <span data-ttu-id="186f2-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="186f2-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="186f2-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="186f2-136">OUTPUTS</span></span>

### <span data-ttu-id="186f2-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="186f2-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="186f2-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="186f2-138">NOTES</span></span>

<span data-ttu-id="186f2-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="186f2-139">ALIASES</span></span>

<span data-ttu-id="186f2-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="186f2-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="186f2-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="186f2-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="186f2-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="186f2-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="186f2-143">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="186f2-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="186f2-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="186f2-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="186f2-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="186f2-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="186f2-146">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="186f2-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="186f2-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="186f2-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="186f2-148">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="186f2-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="186f2-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="186f2-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="186f2-150">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="186f2-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="186f2-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="186f2-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="186f2-152">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="186f2-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="186f2-153">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="186f2-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="186f2-154">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="186f2-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="186f2-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="186f2-155">RELATED LINKS</span></span>

