---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: 89c11be18fbb603f2b05fa9768a3ce05d51ddd86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929931"
---
# <span data-ttu-id="1ca13-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1ca13-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="1ca13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ca13-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca13-103">Erstellt oder aktualisiert eine vorhandene Regel für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="1ca13-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="1ca13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ca13-104">SYNTAX</span></span>

### <span data-ttu-id="1ca13-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ca13-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1ca13-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1ca13-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ca13-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ca13-107">DESCRIPTION</span></span>
<span data-ttu-id="1ca13-108">Erstellt oder aktualisiert eine vorhandene Regel für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="1ca13-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="1ca13-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ca13-109">EXAMPLES</span></span>

### <span data-ttu-id="1ca13-110">Beispiel 1: Aktualisieren der virtuellen PostgreSql-Netzwerkregel nach Name</span><span class="sxs-lookup"><span data-stu-id="1ca13-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="1ca13-111">Dieses Cmdlet aktualisiert die virtuelle PostgreSql-Netzwerkregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="1ca13-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="1ca13-112">Beispiel 2: Aktualisieren der virtuellen PostgreSql-Netzwerkregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="1ca13-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="1ca13-113">Diese Cmdlets aktualisieren die virtuelle PostgreSql-Netzwerkregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="1ca13-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="1ca13-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1ca13-114">PARAMETERS</span></span>

### <span data-ttu-id="1ca13-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ca13-115">-AsJob</span></span>
<span data-ttu-id="1ca13-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1ca13-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1ca13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca13-117">-DefaultProfile</span></span>
<span data-ttu-id="1ca13-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ca13-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ca13-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ca13-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="1ca13-120">Erstellen Sie eine Firewallregel, bevor für das virtuelle Netzwerk der vnet-Dienstendpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1ca13-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="1ca13-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ca13-121">-InputObject</span></span>
<span data-ttu-id="1ca13-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1ca13-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ca13-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1ca13-123">-Name</span></span>
<span data-ttu-id="1ca13-124">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1ca13-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="1ca13-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1ca13-125">-NoWait</span></span>
<span data-ttu-id="1ca13-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1ca13-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1ca13-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ca13-127">-PassThru</span></span>
<span data-ttu-id="1ca13-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ca13-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1ca13-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ca13-129">-ResourceGroupName</span></span>
<span data-ttu-id="1ca13-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1ca13-130">The name of the resource group.</span></span>
<span data-ttu-id="1ca13-131">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="1ca13-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1ca13-132">-Servername</span><span class="sxs-lookup"><span data-stu-id="1ca13-132">-ServerName</span></span>
<span data-ttu-id="1ca13-133">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="1ca13-133">The name of the server.</span></span>

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

### <span data-ttu-id="1ca13-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1ca13-134">-SubnetId</span></span>
<span data-ttu-id="1ca13-135">Die ARM Ressourcen-ID des Subnetzes des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="1ca13-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="1ca13-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ca13-136">-SubscriptionId</span></span>
<span data-ttu-id="1ca13-137">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1ca13-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1ca13-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ca13-138">-Confirm</span></span>
<span data-ttu-id="1ca13-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ca13-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ca13-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ca13-140">-WhatIf</span></span>
<span data-ttu-id="1ca13-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ca13-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ca13-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ca13-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ca13-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca13-143">CommonParameters</span></span>
<span data-ttu-id="1ca13-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ca13-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca13-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ca13-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca13-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ca13-146">INPUTS</span></span>

### <span data-ttu-id="1ca13-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1ca13-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="1ca13-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ca13-148">OUTPUTS</span></span>

### <span data-ttu-id="1ca13-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1ca13-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="1ca13-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1ca13-150">NOTES</span></span>

<span data-ttu-id="1ca13-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1ca13-151">ALIASES</span></span>

<span data-ttu-id="1ca13-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1ca13-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ca13-153">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="1ca13-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ca13-154">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1ca13-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ca13-155">INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="1ca13-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ca13-156">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ca13-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1ca13-157">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1ca13-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1ca13-158">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="1ca13-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1ca13-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="1ca13-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ca13-160">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="1ca13-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1ca13-161">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1ca13-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1ca13-162">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="1ca13-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="1ca13-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="1ca13-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1ca13-164">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="1ca13-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1ca13-165">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="1ca13-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1ca13-166">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1ca13-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1ca13-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1ca13-167">RELATED LINKS</span></span>

