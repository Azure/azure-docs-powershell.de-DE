---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159468"
---
# <span data-ttu-id="a3dbc-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a3dbc-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="a3dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="a3dbc-103">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="a3dbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3dbc-104">SYNTAX</span></span>

### <span data-ttu-id="a3dbc-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3dbc-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3dbc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a3dbc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a3dbc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="a3dbc-108">Erstellt oder aktualisiert eine vorhandene Regel für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="a3dbc-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3dbc-109">EXAMPLES</span></span>

### <span data-ttu-id="a3dbc-110">Beispiel 1: Aktualisieren der Regel für das virtuelle Netzwerk MariaDB</span><span class="sxs-lookup"><span data-stu-id="a3dbc-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="a3dbc-111">Mit diesem Befehl wird eine Regel für ein virtuelles Netzwerk aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="a3dbc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3dbc-112">PARAMETERS</span></span>

### <span data-ttu-id="a3dbc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3dbc-113">-AsJob</span></span>
<span data-ttu-id="a3dbc-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a3dbc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a3dbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3dbc-115">-DefaultProfile</span></span>
<span data-ttu-id="a3dbc-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3dbc-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3dbc-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="a3dbc-118">Erstellen Sie eine Firewallregel, bevor der vnetdienstendpunkt im virtuellen Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="a3dbc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3dbc-119">-InputObject</span></span>
<span data-ttu-id="a3dbc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3dbc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a3dbc-121">-Name</span></span>
<span data-ttu-id="a3dbc-122">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="a3dbc-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a3dbc-123">-NoWait</span></span>
<span data-ttu-id="a3dbc-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a3dbc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a3dbc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3dbc-125">-PassThru</span></span>
<span data-ttu-id="a3dbc-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a3dbc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3dbc-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3dbc-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a3dbc-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a3dbc-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a3dbc-130">-ServerName</span></span>
<span data-ttu-id="a3dbc-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-131">The name of the server.</span></span>

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

### <span data-ttu-id="a3dbc-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a3dbc-132">-SubnetId</span></span>
<span data-ttu-id="a3dbc-133">Die ARM Ressourcen-ID des virtuellen Netzwerk-Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-133">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3dbc-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3dbc-134">-SubscriptionId</span></span>
<span data-ttu-id="a3dbc-135">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a3dbc-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3dbc-136">-Confirm</span></span>
<span data-ttu-id="a3dbc-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3dbc-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a3dbc-138">-WhatIf</span></span>
<span data-ttu-id="a3dbc-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3dbc-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3dbc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3dbc-141">CommonParameters</span></span>
<span data-ttu-id="a3dbc-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3dbc-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3dbc-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3dbc-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3dbc-144">INPUTS</span></span>

### <span data-ttu-id="a3dbc-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="a3dbc-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="a3dbc-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3dbc-146">OUTPUTS</span></span>

### <span data-ttu-id="a3dbc-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a3dbc-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="a3dbc-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3dbc-148">NOTES</span></span>

<span data-ttu-id="a3dbc-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a3dbc-149">ALIASES</span></span>

<span data-ttu-id="a3dbc-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a3dbc-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3dbc-151">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3dbc-152">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3dbc-153">INPUTOBJECT <IMariaDbIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a3dbc-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3dbc-154">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a3dbc-155">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a3dbc-156">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a3dbc-157">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a3dbc-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3dbc-158">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a3dbc-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a3dbc-160">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a3dbc-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a3dbc-162">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a3dbc-163">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="a3dbc-164">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a3dbc-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a3dbc-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3dbc-165">RELATED LINKS</span></span>

