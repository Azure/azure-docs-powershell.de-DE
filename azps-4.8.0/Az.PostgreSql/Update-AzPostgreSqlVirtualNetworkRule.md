---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007917"
---
# <span data-ttu-id="f3624-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f3624-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="f3624-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3624-102">SYNOPSIS</span></span>
<span data-ttu-id="f3624-103">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="f3624-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f3624-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3624-104">SYNTAX</span></span>

### <span data-ttu-id="f3624-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3624-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f3624-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f3624-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3624-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3624-107">DESCRIPTION</span></span>
<span data-ttu-id="f3624-108">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="f3624-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="f3624-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3624-109">EXAMPLES</span></span>

### <span data-ttu-id="f3624-110">Beispiel 1: Aktualisieren der virtuellen PostgreSQL-Netzwerkregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="f3624-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="f3624-111">Dieses Cmdlet aktualisiert die virtuelle PostgreSQL-Netzwerkregel nach Namen.</span><span class="sxs-lookup"><span data-stu-id="f3624-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="f3624-112">Beispiel 2: Aktualisieren der virtuellen PostgreSQL-Netzwerkregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="f3624-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="f3624-113">Diese Cmdlets aktualisieren die virtuelle PostgreSQL-Netzwerkregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="f3624-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="f3624-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3624-114">PARAMETERS</span></span>

### <span data-ttu-id="f3624-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3624-115">-AsJob</span></span>
<span data-ttu-id="f3624-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f3624-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f3624-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3624-117">-DefaultProfile</span></span>
<span data-ttu-id="f3624-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3624-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3624-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f3624-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="f3624-120">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="f3624-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="f3624-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3624-121">-InputObject</span></span>
<span data-ttu-id="f3624-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f3624-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3624-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f3624-123">-Name</span></span>
<span data-ttu-id="f3624-124">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f3624-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="f3624-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f3624-125">-NoWait</span></span>
<span data-ttu-id="f3624-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f3624-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f3624-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3624-127">-PassThru</span></span>
<span data-ttu-id="f3624-128">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="f3624-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f3624-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3624-129">-ResourceGroupName</span></span>
<span data-ttu-id="f3624-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f3624-130">The name of the resource group.</span></span>
<span data-ttu-id="f3624-131">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f3624-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f3624-132">-Servername</span><span class="sxs-lookup"><span data-stu-id="f3624-132">-ServerName</span></span>
<span data-ttu-id="f3624-133">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f3624-133">The name of the server.</span></span>

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

### <span data-ttu-id="f3624-134">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="f3624-134">-SubnetId</span></span>
<span data-ttu-id="f3624-135">Die Arm-Ressourcen-ID des virtuellen Netzwerk-Subnets.</span><span class="sxs-lookup"><span data-stu-id="f3624-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="f3624-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f3624-136">-SubscriptionId</span></span>
<span data-ttu-id="f3624-137">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f3624-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f3624-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3624-138">-Confirm</span></span>
<span data-ttu-id="f3624-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3624-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3624-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3624-140">-WhatIf</span></span>
<span data-ttu-id="f3624-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3624-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3624-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3624-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3624-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3624-143">CommonParameters</span></span>
<span data-ttu-id="f3624-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3624-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3624-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3624-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3624-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3624-146">INPUTS</span></span>

### <span data-ttu-id="f3624-147">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f3624-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="f3624-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3624-148">OUTPUTS</span></span>

### <span data-ttu-id="f3624-149">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f3624-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="f3624-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3624-150">NOTES</span></span>

<span data-ttu-id="f3624-151">Aliase</span><span class="sxs-lookup"><span data-stu-id="f3624-151">ALIASES</span></span>

<span data-ttu-id="f3624-152">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3624-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f3624-153">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f3624-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3624-154">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f3624-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f3624-155">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f3624-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f3624-156">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f3624-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f3624-157">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f3624-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f3624-158">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="f3624-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f3624-159">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f3624-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f3624-160">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="f3624-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f3624-161">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f3624-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f3624-162">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f3624-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="f3624-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="f3624-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f3624-164">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f3624-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f3624-165">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f3624-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f3624-166">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f3624-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f3624-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3624-167">RELATED LINKS</span></span>

