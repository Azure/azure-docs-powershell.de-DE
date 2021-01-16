---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293302"
---
# <span data-ttu-id="f03da-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f03da-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="f03da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f03da-102">SYNOPSIS</span></span>
<span data-ttu-id="f03da-103">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f03da-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f03da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f03da-104">SYNTAX</span></span>

### <span data-ttu-id="f03da-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f03da-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f03da-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f03da-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f03da-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f03da-107">DESCRIPTION</span></span>
<span data-ttu-id="f03da-108">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f03da-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f03da-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f03da-109">EXAMPLES</span></span>

### <span data-ttu-id="f03da-110">Beispiel 1: Aktualisieren der virtuellen PostgreSql-Netzwerkregel nach Name</span><span class="sxs-lookup"><span data-stu-id="f03da-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="f03da-111">Dieses Cmdlet aktualisiert die virtuelle PostgreSql-Netzwerkregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="f03da-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="f03da-112">Beispiel 2: Aktualisieren der virtuellen PostgreSql-Netzwerkregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="f03da-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="f03da-113">Diese Cmdlets aktualisieren die Regeln für das virtuelle PostgreSql-Netzwerk nach Identität.</span><span class="sxs-lookup"><span data-stu-id="f03da-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="f03da-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f03da-114">PARAMETERS</span></span>

### <span data-ttu-id="f03da-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f03da-115">-AsJob</span></span>
<span data-ttu-id="f03da-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f03da-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f03da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03da-117">-DefaultProfile</span></span>
<span data-ttu-id="f03da-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f03da-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f03da-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f03da-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="f03da-120">Erstellen Sie eine Firewallregel, bevor der vnetdienstendpunkt im virtuellen Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f03da-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="f03da-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f03da-121">-InputObject</span></span>
<span data-ttu-id="f03da-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f03da-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f03da-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f03da-123">-Name</span></span>
<span data-ttu-id="f03da-124">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f03da-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="f03da-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f03da-125">-NoWait</span></span>
<span data-ttu-id="f03da-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f03da-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f03da-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f03da-127">-PassThru</span></span>
<span data-ttu-id="f03da-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f03da-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f03da-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03da-129">-ResourceGroupName</span></span>
<span data-ttu-id="f03da-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f03da-130">The name of the resource group.</span></span>
<span data-ttu-id="f03da-131">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="f03da-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f03da-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f03da-132">-ServerName</span></span>
<span data-ttu-id="f03da-133">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f03da-133">The name of the server.</span></span>

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

### <span data-ttu-id="f03da-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f03da-134">-SubnetId</span></span>
<span data-ttu-id="f03da-135">Die ARM Ressourcen-ID des virtuellen Netzwerk-Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="f03da-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="f03da-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f03da-136">-SubscriptionId</span></span>
<span data-ttu-id="f03da-137">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f03da-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f03da-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f03da-138">-Confirm</span></span>
<span data-ttu-id="f03da-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f03da-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f03da-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f03da-140">-WhatIf</span></span>
<span data-ttu-id="f03da-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f03da-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f03da-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f03da-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f03da-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03da-143">CommonParameters</span></span>
<span data-ttu-id="f03da-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f03da-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03da-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f03da-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03da-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f03da-146">INPUTS</span></span>

### <span data-ttu-id="f03da-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f03da-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="f03da-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f03da-148">OUTPUTS</span></span>

### <span data-ttu-id="f03da-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f03da-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="f03da-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f03da-150">NOTES</span></span>

<span data-ttu-id="f03da-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f03da-151">ALIASES</span></span>

<span data-ttu-id="f03da-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f03da-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f03da-153">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f03da-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f03da-154">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f03da-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f03da-155">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f03da-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f03da-156">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f03da-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f03da-157">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f03da-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f03da-158">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="f03da-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f03da-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f03da-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f03da-160">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="f03da-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f03da-161">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f03da-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f03da-162">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="f03da-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="f03da-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f03da-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f03da-164">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f03da-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f03da-165">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f03da-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f03da-166">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f03da-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f03da-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f03da-167">RELATED LINKS</span></span>

