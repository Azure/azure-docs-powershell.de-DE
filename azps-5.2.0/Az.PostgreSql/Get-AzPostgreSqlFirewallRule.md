---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298171"
---
# <span data-ttu-id="733bb-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="733bb-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="733bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="733bb-102">SYNOPSIS</span></span>
<span data-ttu-id="733bb-103">Ruft Informationen zu einer Serverfirewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="733bb-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="733bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="733bb-104">SYNTAX</span></span>

### <span data-ttu-id="733bb-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="733bb-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="733bb-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="733bb-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="733bb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="733bb-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="733bb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="733bb-108">DESCRIPTION</span></span>
<span data-ttu-id="733bb-109">Ruft Informationen zu einer Serverfirewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="733bb-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="733bb-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="733bb-110">EXAMPLES</span></span>

### <span data-ttu-id="733bb-111">Beispiel 1: Listet alle Firewallregeln im angegebenen Server von PostgreSql auf.</span><span class="sxs-lookup"><span data-stu-id="733bb-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="733bb-112">Dieses Cmdlet listet alle Firewallregeln im angegebenen Server von PostgreSql auf.</span><span class="sxs-lookup"><span data-stu-id="733bb-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="733bb-113">Beispiel 2: Firewallregel nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="733bb-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="733bb-114">Dieses Cmdlet ruft die Firewallregel nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="733bb-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="733bb-115">Beispiel 3: Firewallregel nach Identität erhalten</span><span class="sxs-lookup"><span data-stu-id="733bb-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="733bb-116">Dieses Cmdlet ruft die Firewallregel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="733bb-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="733bb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="733bb-117">PARAMETERS</span></span>

### <span data-ttu-id="733bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="733bb-118">-DefaultProfile</span></span>
<span data-ttu-id="733bb-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="733bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="733bb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="733bb-120">-InputObject</span></span>
<span data-ttu-id="733bb-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="733bb-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="733bb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="733bb-122">-Name</span></span>
<span data-ttu-id="733bb-123">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="733bb-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="733bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="733bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="733bb-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="733bb-125">The name of the resource group.</span></span>
<span data-ttu-id="733bb-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="733bb-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="733bb-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="733bb-127">-ServerName</span></span>
<span data-ttu-id="733bb-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="733bb-128">The name of the server.</span></span>

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

### <span data-ttu-id="733bb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="733bb-129">-SubscriptionId</span></span>
<span data-ttu-id="733bb-130">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="733bb-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="733bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="733bb-131">CommonParameters</span></span>
<span data-ttu-id="733bb-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="733bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="733bb-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="733bb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="733bb-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="733bb-134">INPUTS</span></span>

### <span data-ttu-id="733bb-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="733bb-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="733bb-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="733bb-136">OUTPUTS</span></span>

### <span data-ttu-id="733bb-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="733bb-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="733bb-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="733bb-138">NOTES</span></span>

<span data-ttu-id="733bb-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="733bb-139">ALIASES</span></span>

<span data-ttu-id="733bb-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="733bb-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="733bb-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="733bb-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="733bb-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="733bb-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="733bb-143">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="733bb-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="733bb-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="733bb-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="733bb-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="733bb-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="733bb-146">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="733bb-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="733bb-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="733bb-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="733bb-148">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="733bb-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="733bb-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="733bb-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="733bb-150">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="733bb-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="733bb-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="733bb-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="733bb-152">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="733bb-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="733bb-153">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="733bb-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="733bb-154">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="733bb-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="733bb-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="733bb-155">RELATED LINKS</span></span>

