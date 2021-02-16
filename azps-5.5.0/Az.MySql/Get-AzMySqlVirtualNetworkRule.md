---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 8756626488dcc1f5f2a41a06d30581a67db74bb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152132"
---
# <span data-ttu-id="0fc89-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0fc89-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="0fc89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fc89-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc89-103">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="0fc89-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="0fc89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fc89-104">SYNTAX</span></span>

### <span data-ttu-id="0fc89-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="0fc89-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0fc89-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0fc89-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0fc89-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0fc89-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="0fc89-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fc89-108">DESCRIPTION</span></span>
<span data-ttu-id="0fc89-109">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="0fc89-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="0fc89-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0fc89-110">EXAMPLES</span></span>

### <span data-ttu-id="0fc89-111">Beispiel 1: Listet alle Regeln für virtuelle Netzwerke im angegebenen Server von MySql auf.</span><span class="sxs-lookup"><span data-stu-id="0fc89-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="0fc89-112">Dieses Cmdlet listet alle Regeln für virtuelle Netzwerke im angegebenen Server von MySql auf.</span><span class="sxs-lookup"><span data-stu-id="0fc89-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="0fc89-113">Beispiel 2: Virtuelle Netzwerkregel nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="0fc89-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="0fc89-114">Dieses Cmdlet ruft virtuelle Netzwerkregel nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="0fc89-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="0fc89-115">Beispiel 3: Virtuelle Netzwerkregel nach Identität erhalten</span><span class="sxs-lookup"><span data-stu-id="0fc89-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="0fc89-116">Dieses Cmdlet ruft virtuelle Netzwerkregel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="0fc89-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="0fc89-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fc89-117">PARAMETERS</span></span>

### <span data-ttu-id="0fc89-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc89-118">-DefaultProfile</span></span>
<span data-ttu-id="0fc89-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fc89-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc89-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fc89-120">-InputObject</span></span>
<span data-ttu-id="0fc89-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0fc89-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0fc89-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0fc89-122">-Name</span></span>
<span data-ttu-id="0fc89-123">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0fc89-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc89-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fc89-124">-PassThru</span></span>
<span data-ttu-id="0fc89-125">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0fc89-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0fc89-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc89-126">-ResourceGroupName</span></span>
<span data-ttu-id="0fc89-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0fc89-127">The name of the resource group.</span></span>
<span data-ttu-id="0fc89-128">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0fc89-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0fc89-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0fc89-129">-ServerName</span></span>
<span data-ttu-id="0fc89-130">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0fc89-130">The name of the server.</span></span>

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

### <span data-ttu-id="0fc89-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0fc89-131">-SubscriptionId</span></span>
<span data-ttu-id="0fc89-132">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0fc89-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0fc89-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc89-133">CommonParameters</span></span>
<span data-ttu-id="0fc89-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fc89-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc89-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fc89-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc89-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0fc89-136">INPUTS</span></span>

### <span data-ttu-id="0fc89-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0fc89-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0fc89-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0fc89-138">OUTPUTS</span></span>

### <span data-ttu-id="0fc89-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0fc89-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="0fc89-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0fc89-140">NOTES</span></span>

<span data-ttu-id="0fc89-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0fc89-141">ALIASES</span></span>

<span data-ttu-id="0fc89-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0fc89-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0fc89-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0fc89-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0fc89-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0fc89-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0fc89-145">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0fc89-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0fc89-146">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0fc89-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0fc89-147">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0fc89-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0fc89-148">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="0fc89-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0fc89-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="0fc89-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0fc89-150">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="0fc89-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="0fc89-151">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="0fc89-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0fc89-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0fc89-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0fc89-153">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0fc89-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="0fc89-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="0fc89-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0fc89-155">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0fc89-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0fc89-156">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0fc89-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0fc89-157">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0fc89-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0fc89-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0fc89-158">RELATED LINKS</span></span>

