---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cbb774e0a4bedb66a32839c069c305317c8e9f43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945034"
---
# <span data-ttu-id="cd311-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cd311-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="cd311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd311-102">SYNOPSIS</span></span>
<span data-ttu-id="cd311-103">Erstellt oder aktualisiert eine vorhandene Regel für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="cd311-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="cd311-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd311-104">SYNTAX</span></span>

### <span data-ttu-id="cd311-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd311-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd311-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cd311-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cd311-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd311-107">DESCRIPTION</span></span>
<span data-ttu-id="cd311-108">Erstellt oder aktualisiert eine vorhandene Regel für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="cd311-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="cd311-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cd311-109">EXAMPLES</span></span>

### <span data-ttu-id="cd311-110">Beispiel 1: Aktualisieren der virtuellen MariaDB-Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="cd311-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="cd311-111">Mit diesem Befehl wird eine Regel für ein virtuelles Netzwerk aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd311-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="cd311-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cd311-112">PARAMETERS</span></span>

### <span data-ttu-id="cd311-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd311-113">-AsJob</span></span>
<span data-ttu-id="cd311-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="cd311-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cd311-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd311-115">-DefaultProfile</span></span>
<span data-ttu-id="cd311-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd311-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd311-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd311-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="cd311-118">Erstellen Sie eine Firewallregel, bevor für das virtuelle Netzwerk der vnet-Dienstendpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cd311-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="cd311-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd311-119">-InputObject</span></span>
<span data-ttu-id="cd311-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cd311-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cd311-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cd311-121">-Name</span></span>
<span data-ttu-id="cd311-122">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cd311-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="cd311-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cd311-123">-NoWait</span></span>
<span data-ttu-id="cd311-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="cd311-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd311-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd311-125">-PassThru</span></span>
<span data-ttu-id="cd311-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd311-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cd311-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd311-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd311-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="cd311-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cd311-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="cd311-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cd311-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="cd311-130">-ServerName</span></span>
<span data-ttu-id="cd311-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="cd311-131">The name of the server.</span></span>

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

### <span data-ttu-id="cd311-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cd311-132">-SubnetId</span></span>
<span data-ttu-id="cd311-133">Die ARM Ressourcen-ID des Subnetzes des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="cd311-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="cd311-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd311-134">-SubscriptionId</span></span>
<span data-ttu-id="cd311-135">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cd311-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="cd311-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd311-136">-Confirm</span></span>
<span data-ttu-id="cd311-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd311-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd311-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd311-138">-WhatIf</span></span>
<span data-ttu-id="cd311-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd311-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd311-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd311-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd311-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd311-141">CommonParameters</span></span>
<span data-ttu-id="cd311-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd311-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd311-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd311-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd311-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cd311-144">INPUTS</span></span>

### <span data-ttu-id="cd311-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="cd311-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="cd311-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cd311-146">OUTPUTS</span></span>

### <span data-ttu-id="cd311-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cd311-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="cd311-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cd311-148">NOTES</span></span>

<span data-ttu-id="cd311-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cd311-149">ALIASES</span></span>

<span data-ttu-id="cd311-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cd311-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd311-151">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="cd311-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd311-152">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd311-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd311-153">INPUTOBJECT <IMariaDbIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="cd311-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd311-154">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd311-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cd311-155">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cd311-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cd311-156">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="cd311-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cd311-157">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="cd311-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd311-158">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="cd311-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cd311-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="cd311-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="cd311-160">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="cd311-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="cd311-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="cd311-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cd311-162">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="cd311-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cd311-163">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cd311-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="cd311-164">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cd311-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cd311-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cd311-165">RELATED LINKS</span></span>

