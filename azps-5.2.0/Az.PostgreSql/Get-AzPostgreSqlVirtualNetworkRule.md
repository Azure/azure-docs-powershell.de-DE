---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358852"
---
# <span data-ttu-id="56157-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="56157-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="56157-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56157-102">SYNOPSIS</span></span>
<span data-ttu-id="56157-103">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="56157-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="56157-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56157-104">SYNTAX</span></span>

### <span data-ttu-id="56157-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="56157-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="56157-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="56157-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="56157-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56157-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="56157-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56157-108">DESCRIPTION</span></span>
<span data-ttu-id="56157-109">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="56157-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="56157-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56157-110">EXAMPLES</span></span>

### <span data-ttu-id="56157-111">Beispiel 1: Listet alle Regeln für das virtuelle Netzwerk im angegebenen Server von PostgreSql auf.</span><span class="sxs-lookup"><span data-stu-id="56157-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="56157-112">Dieses Cmdlet listet alle Regeln für virtuelle Netzwerke im angegebenen Server von PostgreSql auf.</span><span class="sxs-lookup"><span data-stu-id="56157-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="56157-113">Beispiel 2: Virtuelle Netzwerkregel nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="56157-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="56157-114">Dieses Cmdlet ruft virtuelle Netzwerkregel nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="56157-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="56157-115">Beispiel 3: Virtuelle Netzwerkregel nach Identität erhalten</span><span class="sxs-lookup"><span data-stu-id="56157-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="56157-116">Dieses Cmdlet ruft virtuelle Netzwerkregel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="56157-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="56157-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56157-117">PARAMETERS</span></span>

### <span data-ttu-id="56157-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56157-118">-DefaultProfile</span></span>
<span data-ttu-id="56157-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56157-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56157-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56157-120">-InputObject</span></span>
<span data-ttu-id="56157-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="56157-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56157-122">-Name</span><span class="sxs-lookup"><span data-stu-id="56157-122">-Name</span></span>
<span data-ttu-id="56157-123">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="56157-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="56157-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56157-124">-PassThru</span></span>
<span data-ttu-id="56157-125">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="56157-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="56157-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56157-126">-ResourceGroupName</span></span>
<span data-ttu-id="56157-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="56157-127">The name of the resource group.</span></span>
<span data-ttu-id="56157-128">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="56157-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="56157-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56157-129">-ServerName</span></span>
<span data-ttu-id="56157-130">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="56157-130">The name of the server.</span></span>

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

### <span data-ttu-id="56157-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56157-131">-SubscriptionId</span></span>
<span data-ttu-id="56157-132">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="56157-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="56157-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56157-133">CommonParameters</span></span>
<span data-ttu-id="56157-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56157-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56157-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56157-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56157-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56157-136">INPUTS</span></span>

### <span data-ttu-id="56157-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="56157-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="56157-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56157-138">OUTPUTS</span></span>

### <span data-ttu-id="56157-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="56157-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="56157-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="56157-140">NOTES</span></span>

<span data-ttu-id="56157-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="56157-141">ALIASES</span></span>

<span data-ttu-id="56157-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="56157-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56157-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="56157-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56157-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56157-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56157-145">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="56157-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56157-146">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="56157-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="56157-147">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="56157-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="56157-148">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="56157-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="56157-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="56157-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56157-150">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="56157-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="56157-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="56157-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="56157-152">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="56157-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="56157-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="56157-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="56157-154">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="56157-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="56157-155">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="56157-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="56157-156">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="56157-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="56157-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="56157-157">RELATED LINKS</span></span>

