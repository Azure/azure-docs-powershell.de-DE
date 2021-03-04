---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: e5eb6e239ef49dccf610be866a0f9711245d5ba5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936139"
---
# <span data-ttu-id="4d3ee-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4d3ee-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="4d3ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3ee-103">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="4d3ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d3ee-104">SYNTAX</span></span>

### <span data-ttu-id="4d3ee-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d3ee-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4d3ee-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4d3ee-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4d3ee-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d3ee-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4d3ee-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d3ee-108">DESCRIPTION</span></span>
<span data-ttu-id="4d3ee-109">Ruft eine Regel für ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="4d3ee-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4d3ee-110">EXAMPLES</span></span>

### <span data-ttu-id="4d3ee-111">Beispiel 1: Listet alle Regeln für virtuelles Netzwerk auf dem angegebenen PostgreSql-Server auf.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="4d3ee-112">In diesem Cmdlet werden alle Regeln für virtuelle Netzwerke im angegebenen PostgreSql-Server aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="4d3ee-113">Beispiel 2: Virtuelle Netzwerkregel nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="4d3ee-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="4d3ee-114">Dieses Cmdlet ruft virtuelle Netzwerkregel nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="4d3ee-115">Beispiel 3: Virtuelle Netzwerkregel nach Identität erhalten</span><span class="sxs-lookup"><span data-stu-id="4d3ee-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="4d3ee-116">Dieses Cmdlet ruft virtuelle Netzwerkregel nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="4d3ee-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4d3ee-117">PARAMETERS</span></span>

### <span data-ttu-id="4d3ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3ee-118">-DefaultProfile</span></span>
<span data-ttu-id="4d3ee-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d3ee-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d3ee-120">-InputObject</span></span>
<span data-ttu-id="4d3ee-121">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d3ee-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4d3ee-122">-Name</span></span>
<span data-ttu-id="4d3ee-123">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="4d3ee-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d3ee-124">-PassThru</span></span>
<span data-ttu-id="4d3ee-125">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4d3ee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d3ee-126">-ResourceGroupName</span></span>
<span data-ttu-id="4d3ee-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-127">The name of the resource group.</span></span>
<span data-ttu-id="4d3ee-128">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4d3ee-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="4d3ee-129">-ServerName</span></span>
<span data-ttu-id="4d3ee-130">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-130">The name of the server.</span></span>

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

### <span data-ttu-id="4d3ee-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d3ee-131">-SubscriptionId</span></span>
<span data-ttu-id="4d3ee-132">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4d3ee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3ee-133">CommonParameters</span></span>
<span data-ttu-id="4d3ee-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3ee-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d3ee-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3ee-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4d3ee-136">INPUTS</span></span>

### <span data-ttu-id="4d3ee-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4d3ee-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="4d3ee-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4d3ee-138">OUTPUTS</span></span>

### <span data-ttu-id="4d3ee-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4d3ee-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="4d3ee-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4d3ee-140">NOTES</span></span>

<span data-ttu-id="4d3ee-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4d3ee-141">ALIASES</span></span>

<span data-ttu-id="4d3ee-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="4d3ee-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d3ee-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d3ee-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d3ee-145">INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="4d3ee-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d3ee-146">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4d3ee-147">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4d3ee-148">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4d3ee-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="4d3ee-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d3ee-150">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4d3ee-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4d3ee-152">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="4d3ee-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4d3ee-154">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4d3ee-155">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4d3ee-156">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4d3ee-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4d3ee-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4d3ee-157">RELATED LINKS</span></span>

