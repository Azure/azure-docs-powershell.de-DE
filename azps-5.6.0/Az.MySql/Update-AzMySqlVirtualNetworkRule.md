---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 572943ea0f694b5a3a68ff4c1c030a1a3a1fc0f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926984"
---
# <span data-ttu-id="34b9f-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="34b9f-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="34b9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="34b9f-103">Erstellt oder aktualisiert eine vorhandene Regel für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="34b9f-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="34b9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34b9f-104">SYNTAX</span></span>

### <span data-ttu-id="34b9f-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="34b9f-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="34b9f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="34b9f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34b9f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34b9f-107">DESCRIPTION</span></span>
<span data-ttu-id="34b9f-108">Erstellt oder aktualisiert eine vorhandene Regel für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="34b9f-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="34b9f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="34b9f-109">EXAMPLES</span></span>

### <span data-ttu-id="34b9f-110">Beispiel 1: Aktualisieren der virtuellen MySql-Netzwerkregel nach Name</span><span class="sxs-lookup"><span data-stu-id="34b9f-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="34b9f-111">Dieses Cmdlet aktualisiert die MySql Virtual Network Rule nach Name.</span><span class="sxs-lookup"><span data-stu-id="34b9f-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="34b9f-112">Beispiel 2: Aktualisieren der virtuellen MySql-Netzwerkregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="34b9f-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="34b9f-113">Diese Cmdlets aktualisieren mySql Virtual Network Rule nach Identität.</span><span class="sxs-lookup"><span data-stu-id="34b9f-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="34b9f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="34b9f-114">PARAMETERS</span></span>

### <span data-ttu-id="34b9f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34b9f-115">-AsJob</span></span>
<span data-ttu-id="34b9f-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="34b9f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="34b9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b9f-117">-DefaultProfile</span></span>
<span data-ttu-id="34b9f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34b9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34b9f-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="34b9f-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="34b9f-120">Erstellen Sie eine Firewallregel, bevor für das virtuelle Netzwerk der vnet-Dienstendpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="34b9f-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="34b9f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34b9f-121">-InputObject</span></span>
<span data-ttu-id="34b9f-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="34b9f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34b9f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="34b9f-123">-Name</span></span>
<span data-ttu-id="34b9f-124">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="34b9f-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="34b9f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="34b9f-125">-NoWait</span></span>
<span data-ttu-id="34b9f-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="34b9f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="34b9f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34b9f-127">-PassThru</span></span>
<span data-ttu-id="34b9f-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34b9f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="34b9f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34b9f-129">-ResourceGroupName</span></span>
<span data-ttu-id="34b9f-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="34b9f-130">The name of the resource group.</span></span>
<span data-ttu-id="34b9f-131">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="34b9f-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="34b9f-132">-Servername</span><span class="sxs-lookup"><span data-stu-id="34b9f-132">-ServerName</span></span>
<span data-ttu-id="34b9f-133">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="34b9f-133">The name of the server.</span></span>

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

### <span data-ttu-id="34b9f-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="34b9f-134">-SubnetId</span></span>
<span data-ttu-id="34b9f-135">Die ARM Ressourcen-ID des Subnetzes des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="34b9f-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="34b9f-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34b9f-136">-SubscriptionId</span></span>
<span data-ttu-id="34b9f-137">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="34b9f-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="34b9f-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34b9f-138">-Confirm</span></span>
<span data-ttu-id="34b9f-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34b9f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34b9f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34b9f-140">-WhatIf</span></span>
<span data-ttu-id="34b9f-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34b9f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34b9f-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34b9f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34b9f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b9f-143">CommonParameters</span></span>
<span data-ttu-id="34b9f-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34b9f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b9f-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34b9f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b9f-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="34b9f-146">INPUTS</span></span>

### <span data-ttu-id="34b9f-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="34b9f-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="34b9f-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="34b9f-148">OUTPUTS</span></span>

### <span data-ttu-id="34b9f-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="34b9f-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="34b9f-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="34b9f-150">NOTES</span></span>

<span data-ttu-id="34b9f-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="34b9f-151">ALIASES</span></span>

<span data-ttu-id="34b9f-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="34b9f-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34b9f-153">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="34b9f-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34b9f-154">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34b9f-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34b9f-155">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="34b9f-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34b9f-156">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="34b9f-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="34b9f-157">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="34b9f-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="34b9f-158">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="34b9f-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="34b9f-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="34b9f-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34b9f-160">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="34b9f-160">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="34b9f-161">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="34b9f-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="34b9f-162">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="34b9f-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="34b9f-163">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="34b9f-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="34b9f-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="34b9f-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="34b9f-165">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="34b9f-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="34b9f-166">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="34b9f-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="34b9f-167">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="34b9f-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="34b9f-168">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="34b9f-168">RELATED LINKS</span></span>

