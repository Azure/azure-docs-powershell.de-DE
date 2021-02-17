---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: f750718c4bd380b579dff0897b53a68ae4f45b95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159380"
---
# <span data-ttu-id="986ec-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="986ec-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="986ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="986ec-102">SYNOPSIS</span></span>
<span data-ttu-id="986ec-103">Ruft Informationen zu einer Serverfirewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="986ec-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="986ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="986ec-104">SYNTAX</span></span>

### <span data-ttu-id="986ec-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="986ec-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="986ec-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="986ec-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="986ec-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="986ec-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="986ec-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="986ec-108">DESCRIPTION</span></span>
<span data-ttu-id="986ec-109">Ruft Informationen zu einer Serverfirewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="986ec-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="986ec-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="986ec-110">EXAMPLES</span></span>

### <span data-ttu-id="986ec-111">Beispiel 1: Listet alle Firewallregeln im angegebenen Server von MySql auf.</span><span class="sxs-lookup"><span data-stu-id="986ec-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="986ec-112">Dieses Cmdlet listet alle Firewallregeln im angegebenen Server von MySql auf.</span><span class="sxs-lookup"><span data-stu-id="986ec-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="986ec-113">Beispiel 2: Firewallregel nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="986ec-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="986ec-114">Dieses Cmdlet ruft die Firewallregel nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="986ec-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="986ec-115">Beispiel 3: Firewallregel nach Identität erhalten</span><span class="sxs-lookup"><span data-stu-id="986ec-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="986ec-116">Dieses Cmdlet ruft die Firewallregel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="986ec-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="986ec-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="986ec-117">PARAMETERS</span></span>

### <span data-ttu-id="986ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="986ec-118">-DefaultProfile</span></span>
<span data-ttu-id="986ec-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="986ec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="986ec-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="986ec-120">-InputObject</span></span>
<span data-ttu-id="986ec-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="986ec-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="986ec-122">-Name</span><span class="sxs-lookup"><span data-stu-id="986ec-122">-Name</span></span>
<span data-ttu-id="986ec-123">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="986ec-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="986ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="986ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="986ec-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="986ec-125">The name of the resource group.</span></span>
<span data-ttu-id="986ec-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="986ec-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="986ec-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="986ec-127">-ServerName</span></span>
<span data-ttu-id="986ec-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="986ec-128">The name of the server.</span></span>

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

### <span data-ttu-id="986ec-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="986ec-129">-SubscriptionId</span></span>
<span data-ttu-id="986ec-130">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="986ec-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="986ec-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986ec-131">CommonParameters</span></span>
<span data-ttu-id="986ec-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="986ec-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986ec-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="986ec-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986ec-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="986ec-134">INPUTS</span></span>

### <span data-ttu-id="986ec-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="986ec-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="986ec-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="986ec-136">OUTPUTS</span></span>

### <span data-ttu-id="986ec-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="986ec-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="986ec-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="986ec-138">NOTES</span></span>

<span data-ttu-id="986ec-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="986ec-139">ALIASES</span></span>

<span data-ttu-id="986ec-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="986ec-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="986ec-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="986ec-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="986ec-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="986ec-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="986ec-143">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="986ec-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="986ec-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="986ec-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="986ec-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="986ec-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="986ec-146">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="986ec-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="986ec-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="986ec-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="986ec-148">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="986ec-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="986ec-149">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="986ec-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="986ec-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="986ec-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="986ec-151">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="986ec-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="986ec-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="986ec-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="986ec-153">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="986ec-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="986ec-154">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="986ec-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="986ec-155">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="986ec-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="986ec-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="986ec-156">RELATED LINKS</span></span>

