---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 7f2a3e567da4df9a004c5dac642f480a4cd7388a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358964"
---
# <span data-ttu-id="47386-101">Get-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="47386-101">Get-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="47386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47386-102">SYNOPSIS</span></span>
<span data-ttu-id="47386-103">Ruft Informationen zu einer Serverfirewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="47386-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="47386-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47386-104">SYNTAX</span></span>

### <span data-ttu-id="47386-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="47386-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47386-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="47386-106">Get</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47386-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47386-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="47386-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47386-108">DESCRIPTION</span></span>
<span data-ttu-id="47386-109">Ruft Informationen zu einer Serverfirewallregel ab.</span><span class="sxs-lookup"><span data-stu-id="47386-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="47386-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47386-110">EXAMPLES</span></span>

### <span data-ttu-id="47386-111">Beispiel 1: Erhalten von Firewallregeln nach Name</span><span class="sxs-lookup"><span data-stu-id="47386-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="47386-112">Dieses Cmdlet ruft Firewallregeln nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="47386-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="47386-113">Beispiel 2: Erhalten von Firewallregeln nach Identität</span><span class="sxs-lookup"><span data-stu-id="47386-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="47386-114">Dieses Cmdlet ruft Firewallregeln nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="47386-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="47386-115">Beispiel 3: Listet alle Firewallregeln im angegebenen Server von MySql auf.</span><span class="sxs-lookup"><span data-stu-id="47386-115">Example 3: Lists all the firewall rules in the specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="47386-116">Dieses Cmdlet listet alle Firewallregeln auf dem angegebenen Server "MySql" auf.</span><span class="sxs-lookup"><span data-stu-id="47386-116">This cmdlet lists all the firewall rule in specified MySql server.</span></span>

## <span data-ttu-id="47386-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47386-117">PARAMETERS</span></span>

### <span data-ttu-id="47386-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47386-118">-DefaultProfile</span></span>
<span data-ttu-id="47386-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47386-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47386-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47386-120">-InputObject</span></span>
<span data-ttu-id="47386-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="47386-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="47386-122">-Name</span><span class="sxs-lookup"><span data-stu-id="47386-122">-Name</span></span>
<span data-ttu-id="47386-123">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="47386-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="47386-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47386-124">-ResourceGroupName</span></span>
<span data-ttu-id="47386-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="47386-125">The name of the resource group.</span></span>
<span data-ttu-id="47386-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="47386-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="47386-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47386-127">-ServerName</span></span>
<span data-ttu-id="47386-128">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="47386-128">The name of the server.</span></span>

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

### <span data-ttu-id="47386-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47386-129">-SubscriptionId</span></span>
<span data-ttu-id="47386-130">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="47386-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="47386-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47386-131">CommonParameters</span></span>
<span data-ttu-id="47386-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47386-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47386-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47386-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47386-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47386-134">INPUTS</span></span>

### <span data-ttu-id="47386-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="47386-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="47386-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47386-136">OUTPUTS</span></span>

### <span data-ttu-id="47386-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="47386-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="47386-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="47386-138">NOTES</span></span>

<span data-ttu-id="47386-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="47386-139">ALIASES</span></span>

<span data-ttu-id="47386-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="47386-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47386-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="47386-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47386-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47386-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47386-143">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="47386-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47386-144">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="47386-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="47386-145">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="47386-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="47386-146">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="47386-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="47386-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="47386-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47386-148">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="47386-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="47386-149">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="47386-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="47386-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="47386-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="47386-151">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="47386-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="47386-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="47386-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="47386-153">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="47386-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="47386-154">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="47386-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="47386-155">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="47386-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="47386-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="47386-156">RELATED LINKS</span></span>

