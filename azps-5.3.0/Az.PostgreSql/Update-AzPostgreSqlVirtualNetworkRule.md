---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468708"
---
# <span data-ttu-id="67287-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="67287-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="67287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67287-102">SYNOPSIS</span></span>
<span data-ttu-id="67287-103">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="67287-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="67287-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67287-104">SYNTAX</span></span>

### <span data-ttu-id="67287-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="67287-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="67287-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="67287-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="67287-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67287-107">DESCRIPTION</span></span>
<span data-ttu-id="67287-108">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="67287-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="67287-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67287-109">EXAMPLES</span></span>

### <span data-ttu-id="67287-110">Beispiel 1: Aktualisieren der virtuellen PostgreSql-Netzwerkregel nach Name</span><span class="sxs-lookup"><span data-stu-id="67287-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="67287-111">Dieses Cmdlet aktualisiert die virtuelle PostgreSql-Netzwerkregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="67287-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="67287-112">Beispiel 2: Aktualisieren der virtuellen PostgreSql-Netzwerkregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="67287-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="67287-113">Diese Cmdlets aktualisieren die Regeln für das virtuelle PostgreSql-Netzwerk nach Identität.</span><span class="sxs-lookup"><span data-stu-id="67287-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="67287-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67287-114">PARAMETERS</span></span>

### <span data-ttu-id="67287-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67287-115">-AsJob</span></span>
<span data-ttu-id="67287-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="67287-116">Run the command as a job</span></span>

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

### <span data-ttu-id="67287-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67287-117">-DefaultProfile</span></span>
<span data-ttu-id="67287-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67287-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67287-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="67287-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="67287-120">Erstellen Sie eine Firewallregel, bevor der vnetdienstendpunkt im virtuellen Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="67287-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="67287-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67287-121">-InputObject</span></span>
<span data-ttu-id="67287-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="67287-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67287-123">-Name</span><span class="sxs-lookup"><span data-stu-id="67287-123">-Name</span></span>
<span data-ttu-id="67287-124">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="67287-124">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67287-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="67287-125">-NoWait</span></span>
<span data-ttu-id="67287-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="67287-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="67287-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67287-127">-PassThru</span></span>
<span data-ttu-id="67287-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="67287-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="67287-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67287-129">-ResourceGroupName</span></span>
<span data-ttu-id="67287-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67287-130">The name of the resource group.</span></span>
<span data-ttu-id="67287-131">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="67287-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67287-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67287-132">-ServerName</span></span>
<span data-ttu-id="67287-133">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="67287-133">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67287-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="67287-134">-SubnetId</span></span>
<span data-ttu-id="67287-135">Die ARM Ressourcen-ID des virtuellen Netzwerk-Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="67287-135">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67287-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67287-136">-SubscriptionId</span></span>
<span data-ttu-id="67287-137">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="67287-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67287-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67287-138">-Confirm</span></span>
<span data-ttu-id="67287-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67287-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67287-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="67287-140">-WhatIf</span></span>
<span data-ttu-id="67287-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67287-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67287-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67287-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67287-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67287-143">CommonParameters</span></span>
<span data-ttu-id="67287-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67287-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67287-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67287-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67287-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67287-146">INPUTS</span></span>

### <span data-ttu-id="67287-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="67287-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="67287-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67287-148">OUTPUTS</span></span>

### <span data-ttu-id="67287-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="67287-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="67287-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="67287-150">NOTES</span></span>

<span data-ttu-id="67287-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="67287-151">ALIASES</span></span>

<span data-ttu-id="67287-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="67287-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67287-153">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="67287-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67287-154">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67287-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67287-155">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="67287-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67287-156">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="67287-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="67287-157">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="67287-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="67287-158">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="67287-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="67287-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="67287-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67287-160">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="67287-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="67287-161">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67287-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="67287-162">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="67287-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="67287-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="67287-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="67287-164">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="67287-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="67287-165">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="67287-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="67287-166">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="67287-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="67287-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="67287-167">RELATED LINKS</span></span>

