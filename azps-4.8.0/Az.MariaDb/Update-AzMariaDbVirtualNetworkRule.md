---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174658"
---
# <span data-ttu-id="e7f83-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e7f83-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="e7f83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7f83-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f83-103">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="e7f83-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e7f83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7f83-104">SYNTAX</span></span>

### <span data-ttu-id="e7f83-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="e7f83-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e7f83-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e7f83-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e7f83-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7f83-107">DESCRIPTION</span></span>
<span data-ttu-id="e7f83-108">Erstellt oder aktualisiert eine vorhandene virtuelle Netzwerkregel.</span><span class="sxs-lookup"><span data-stu-id="e7f83-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="e7f83-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7f83-109">EXAMPLES</span></span>

### <span data-ttu-id="e7f83-110">Beispiel 1: Regel für das MariaDB-virtuelles Netzwerk aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e7f83-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="e7f83-111">Mit diesem Befehl wird eine virtuelle Netzwerkregel aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e7f83-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="e7f83-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7f83-112">PARAMETERS</span></span>

### <span data-ttu-id="e7f83-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7f83-113">-AsJob</span></span>
<span data-ttu-id="e7f83-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e7f83-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e7f83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f83-115">-DefaultProfile</span></span>
<span data-ttu-id="e7f83-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7f83-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7f83-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7f83-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e7f83-118">Erstellen Sie eine Firewallregel, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="e7f83-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="e7f83-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e7f83-119">-InputObject</span></span>
<span data-ttu-id="e7f83-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e7f83-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e7f83-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e7f83-121">-Name</span></span>
<span data-ttu-id="e7f83-122">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e7f83-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e7f83-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e7f83-123">-NoWait</span></span>
<span data-ttu-id="e7f83-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e7f83-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e7f83-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7f83-125">-PassThru</span></span>
<span data-ttu-id="e7f83-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="e7f83-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e7f83-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f83-127">-ResourceGroupName</span></span>
<span data-ttu-id="e7f83-128">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="e7f83-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e7f83-129">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e7f83-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e7f83-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="e7f83-130">-ServerName</span></span>
<span data-ttu-id="e7f83-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e7f83-131">The name of the server.</span></span>

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

### <span data-ttu-id="e7f83-132">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="e7f83-132">-SubnetId</span></span>
<span data-ttu-id="e7f83-133">Die Arm-Ressourcen-ID des virtuellen Netzwerk-Subnets.</span><span class="sxs-lookup"><span data-stu-id="e7f83-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="e7f83-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e7f83-134">-SubscriptionId</span></span>
<span data-ttu-id="e7f83-135">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e7f83-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e7f83-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7f83-136">-Confirm</span></span>
<span data-ttu-id="e7f83-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7f83-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f83-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f83-138">-WhatIf</span></span>
<span data-ttu-id="e7f83-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7f83-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7f83-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7f83-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7f83-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f83-141">CommonParameters</span></span>
<span data-ttu-id="e7f83-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f83-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f83-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7f83-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f83-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7f83-144">INPUTS</span></span>

### <span data-ttu-id="e7f83-145">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="e7f83-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="e7f83-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7f83-146">OUTPUTS</span></span>

### <span data-ttu-id="e7f83-147">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e7f83-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="e7f83-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7f83-148">NOTES</span></span>

<span data-ttu-id="e7f83-149">Aliase</span><span class="sxs-lookup"><span data-stu-id="e7f83-149">ALIASES</span></span>

<span data-ttu-id="e7f83-150">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7f83-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e7f83-151">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e7f83-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e7f83-152">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="e7f83-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e7f83-153">Inputobject <IMariaDbIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="e7f83-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e7f83-154">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e7f83-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e7f83-155">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e7f83-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e7f83-156">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="e7f83-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e7f83-157">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="e7f83-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e7f83-158">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="e7f83-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e7f83-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="e7f83-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e7f83-160">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e7f83-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e7f83-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="e7f83-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e7f83-162">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e7f83-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e7f83-163">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e7f83-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="e7f83-164">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e7f83-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e7f83-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7f83-165">RELATED LINKS</span></span>

