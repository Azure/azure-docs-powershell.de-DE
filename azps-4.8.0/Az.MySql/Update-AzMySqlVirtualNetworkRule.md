---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: f98c24ab0be3b2c35ac43642fb9d4bbf0b421c7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166322"
---
# <span data-ttu-id="88f3e-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="88f3e-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="88f3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="88f3e-103">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="88f3e-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="88f3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88f3e-104">SYNTAX</span></span>

### <span data-ttu-id="88f3e-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="88f3e-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="88f3e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="88f3e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88f3e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88f3e-107">DESCRIPTION</span></span>
<span data-ttu-id="88f3e-108">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="88f3e-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="88f3e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88f3e-109">EXAMPLES</span></span>

### <span data-ttu-id="88f3e-110">Beispiel 1: Aktualisieren der virtuellen MySQL-Netzwerkregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="88f3e-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="88f3e-111">Dieses Cmdlet aktualisiert die virtuelle MySQL-Netzwerkregel nach Namen.</span><span class="sxs-lookup"><span data-stu-id="88f3e-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="88f3e-112">Beispiel 2: Aktualisieren der virtuellen MySQL-Netzwerkregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="88f3e-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="88f3e-113">Diese Cmdlets aktualisieren die virtuelle MySQL-Netzwerkregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="88f3e-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="88f3e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="88f3e-114">PARAMETERS</span></span>

### <span data-ttu-id="88f3e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88f3e-115">-AsJob</span></span>
<span data-ttu-id="88f3e-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="88f3e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="88f3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f3e-117">-DefaultProfile</span></span>
<span data-ttu-id="88f3e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88f3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88f3e-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="88f3e-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="88f3e-120">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="88f3e-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="88f3e-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="88f3e-121">-InputObject</span></span>
<span data-ttu-id="88f3e-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="88f3e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="88f3e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="88f3e-123">-Name</span></span>
<span data-ttu-id="88f3e-124">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="88f3e-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="88f3e-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="88f3e-125">-NoWait</span></span>
<span data-ttu-id="88f3e-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="88f3e-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="88f3e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88f3e-127">-PassThru</span></span>
<span data-ttu-id="88f3e-128">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="88f3e-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="88f3e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88f3e-129">-ResourceGroupName</span></span>
<span data-ttu-id="88f3e-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88f3e-130">The name of the resource group.</span></span>
<span data-ttu-id="88f3e-131">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="88f3e-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="88f3e-132">-Servername</span><span class="sxs-lookup"><span data-stu-id="88f3e-132">-ServerName</span></span>
<span data-ttu-id="88f3e-133">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="88f3e-133">The name of the server.</span></span>

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

### <span data-ttu-id="88f3e-134">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="88f3e-134">-SubnetId</span></span>
<span data-ttu-id="88f3e-135">Die Arm-Ressourcen-ID des virtuellen Netzwerk-Subnets.</span><span class="sxs-lookup"><span data-stu-id="88f3e-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="88f3e-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="88f3e-136">-SubscriptionId</span></span>
<span data-ttu-id="88f3e-137">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="88f3e-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="88f3e-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88f3e-138">-Confirm</span></span>
<span data-ttu-id="88f3e-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88f3e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88f3e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88f3e-140">-WhatIf</span></span>
<span data-ttu-id="88f3e-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88f3e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88f3e-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88f3e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88f3e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f3e-143">CommonParameters</span></span>
<span data-ttu-id="88f3e-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88f3e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f3e-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88f3e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f3e-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88f3e-146">INPUTS</span></span>

### <span data-ttu-id="88f3e-147">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="88f3e-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="88f3e-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88f3e-148">OUTPUTS</span></span>

### <span data-ttu-id="88f3e-149">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="88f3e-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="88f3e-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="88f3e-150">NOTES</span></span>

<span data-ttu-id="88f3e-151">Aliase</span><span class="sxs-lookup"><span data-stu-id="88f3e-151">ALIASES</span></span>

<span data-ttu-id="88f3e-152">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88f3e-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88f3e-153">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="88f3e-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88f3e-154">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="88f3e-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88f3e-155">Inputobject <IMySqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="88f3e-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88f3e-156">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="88f3e-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="88f3e-157">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="88f3e-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="88f3e-158">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="88f3e-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="88f3e-159">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="88f3e-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88f3e-160">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="88f3e-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="88f3e-161">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88f3e-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="88f3e-162">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="88f3e-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="88f3e-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="88f3e-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="88f3e-164">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="88f3e-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="88f3e-165">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="88f3e-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="88f3e-166">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="88f3e-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="88f3e-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88f3e-167">RELATED LINKS</span></span>

