---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166180"
---
# <span data-ttu-id="e8f08-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e8f08-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="e8f08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8f08-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f08-103">Ruft Informationen zu einer Server Firewall-Regel ab.</span><span class="sxs-lookup"><span data-stu-id="e8f08-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="e8f08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8f08-104">SYNTAX</span></span>

### <span data-ttu-id="e8f08-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8f08-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e8f08-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e8f08-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e8f08-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e8f08-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8f08-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8f08-108">DESCRIPTION</span></span>
<span data-ttu-id="e8f08-109">Ruft Informationen zu einer Server Firewall-Regel ab.</span><span class="sxs-lookup"><span data-stu-id="e8f08-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="e8f08-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8f08-110">EXAMPLES</span></span>

### <span data-ttu-id="e8f08-111">Beispiel 1: Listet alle Firewallregeln auf dem angegebenen PostgreSQL-Server auf</span><span class="sxs-lookup"><span data-stu-id="e8f08-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="e8f08-112">Dieses Cmdlet listet alle Firewallregel auf, die sich auf dem angegebenen PostgreSQL-Server befinden.</span><span class="sxs-lookup"><span data-stu-id="e8f08-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="e8f08-113">Beispiel 2: Abrufen der Firewallregel nach Name</span><span class="sxs-lookup"><span data-stu-id="e8f08-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="e8f08-114">Dieses Cmdlet ruft die Firewall-Regel nach Namen ab.</span><span class="sxs-lookup"><span data-stu-id="e8f08-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="e8f08-115">Beispiel 3: Abrufen der Firewall-Regel nach Identität</span><span class="sxs-lookup"><span data-stu-id="e8f08-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="e8f08-116">Dieses Cmdlet ruft die Firewall-Regel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="e8f08-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="e8f08-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8f08-117">PARAMETERS</span></span>

### <span data-ttu-id="e8f08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f08-118">-DefaultProfile</span></span>
<span data-ttu-id="e8f08-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8f08-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f08-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8f08-120">-InputObject</span></span>
<span data-ttu-id="e8f08-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e8f08-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e8f08-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e8f08-122">-Name</span></span>
<span data-ttu-id="e8f08-123">Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="e8f08-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="e8f08-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f08-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8f08-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e8f08-125">The name of the resource group.</span></span>
<span data-ttu-id="e8f08-126">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e8f08-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e8f08-127">-Servername</span><span class="sxs-lookup"><span data-stu-id="e8f08-127">-ServerName</span></span>
<span data-ttu-id="e8f08-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e8f08-128">The name of the server.</span></span>

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

### <span data-ttu-id="e8f08-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e8f08-129">-SubscriptionId</span></span>
<span data-ttu-id="e8f08-130">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e8f08-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e8f08-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f08-131">CommonParameters</span></span>
<span data-ttu-id="e8f08-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8f08-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f08-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8f08-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f08-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8f08-134">INPUTS</span></span>

### <span data-ttu-id="e8f08-135">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e8f08-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e8f08-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8f08-136">OUTPUTS</span></span>

### <span data-ttu-id="e8f08-137">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e8f08-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="e8f08-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8f08-138">NOTES</span></span>

<span data-ttu-id="e8f08-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="e8f08-139">ALIASES</span></span>

<span data-ttu-id="e8f08-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e8f08-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e8f08-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e8f08-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e8f08-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="e8f08-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e8f08-143">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="e8f08-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e8f08-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e8f08-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e8f08-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e8f08-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e8f08-146">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="e8f08-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e8f08-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="e8f08-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e8f08-148">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="e8f08-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e8f08-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e8f08-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e8f08-150">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e8f08-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="e8f08-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="e8f08-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e8f08-152">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e8f08-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e8f08-153">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e8f08-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e8f08-154">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e8f08-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e8f08-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8f08-155">RELATED LINKS</span></span>

