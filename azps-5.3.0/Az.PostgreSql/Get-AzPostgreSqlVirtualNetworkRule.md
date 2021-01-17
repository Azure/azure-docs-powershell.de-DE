---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378438"
---
# <span data-ttu-id="cbc1d-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cbc1d-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="cbc1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc1d-103">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="cbc1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbc1d-104">SYNTAX</span></span>

### <span data-ttu-id="cbc1d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="cbc1d-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cbc1d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="cbc1d-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cbc1d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cbc1d-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="cbc1d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cbc1d-108">DESCRIPTION</span></span>
<span data-ttu-id="cbc1d-109">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="cbc1d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cbc1d-110">EXAMPLES</span></span>

### <span data-ttu-id="cbc1d-111">Beispiel 1: Listet alle Regeln für virtuelle Netzwerke im angegebenen Server von PostgreSql auf.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="cbc1d-112">Dieses Cmdlet listet alle Regeln für virtuelle Netzwerke im angegebenen Server von PostgreSql auf.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="cbc1d-113">Beispiel 2: Virtuelle Netzwerkregel nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="cbc1d-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="cbc1d-114">Dieses Cmdlet ruft virtuelle Netzwerkregel nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="cbc1d-115">Beispiel 3: Virtuelle Netzwerkregel nach Identität erhalten</span><span class="sxs-lookup"><span data-stu-id="cbc1d-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="cbc1d-116">Dieses Cmdlet ruft virtuelle Netzwerkregel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="cbc1d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbc1d-117">PARAMETERS</span></span>

### <span data-ttu-id="cbc1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc1d-118">-DefaultProfile</span></span>
<span data-ttu-id="cbc1d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbc1d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbc1d-120">-InputObject</span></span>
<span data-ttu-id="cbc1d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbc1d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cbc1d-122">-Name</span></span>
<span data-ttu-id="cbc1d-123">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="cbc1d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbc1d-124">-PassThru</span></span>
<span data-ttu-id="cbc1d-125">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cbc1d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbc1d-126">-ResourceGroupName</span></span>
<span data-ttu-id="cbc1d-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-127">The name of the resource group.</span></span>
<span data-ttu-id="cbc1d-128">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cbc1d-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cbc1d-129">-ServerName</span></span>
<span data-ttu-id="cbc1d-130">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-130">The name of the server.</span></span>

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

### <span data-ttu-id="cbc1d-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbc1d-131">-SubscriptionId</span></span>
<span data-ttu-id="cbc1d-132">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cbc1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc1d-133">CommonParameters</span></span>
<span data-ttu-id="cbc1d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc1d-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbc1d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc1d-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cbc1d-136">INPUTS</span></span>

### <span data-ttu-id="cbc1d-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cbc1d-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="cbc1d-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cbc1d-138">OUTPUTS</span></span>

### <span data-ttu-id="cbc1d-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cbc1d-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="cbc1d-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cbc1d-140">NOTES</span></span>

<span data-ttu-id="cbc1d-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cbc1d-141">ALIASES</span></span>

<span data-ttu-id="cbc1d-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cbc1d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cbc1d-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbc1d-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cbc1d-145">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="cbc1d-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cbc1d-146">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cbc1d-147">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cbc1d-148">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cbc1d-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="cbc1d-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cbc1d-150">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cbc1d-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cbc1d-152">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="cbc1d-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cbc1d-154">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cbc1d-155">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cbc1d-156">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cbc1d-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cbc1d-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cbc1d-157">RELATED LINKS</span></span>

