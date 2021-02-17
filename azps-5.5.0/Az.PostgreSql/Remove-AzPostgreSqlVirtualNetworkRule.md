---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: bacd5e1636457fac172cd54c9fcf4407247d88ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156601"
---
# <span data-ttu-id="121f9-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="121f9-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="121f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="121f9-102">SYNOPSIS</span></span>
<span data-ttu-id="121f9-103">Löscht die Regel für das virtuelle Netzwerk mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="121f9-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="121f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="121f9-104">SYNTAX</span></span>

### <span data-ttu-id="121f9-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="121f9-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="121f9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="121f9-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="121f9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="121f9-107">DESCRIPTION</span></span>
<span data-ttu-id="121f9-108">Löscht die Regel für das virtuelle Netzwerk mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="121f9-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="121f9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="121f9-109">EXAMPLES</span></span>

### <span data-ttu-id="121f9-110">Beispiel 1: Entfernen der virtuellen Netzwerkregel des PostgreSqlservers nach Name</span><span class="sxs-lookup"><span data-stu-id="121f9-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="121f9-111">Dieses Cmdlet entfernt die virtuelle Netzwerkregel des PostgreSql-Servers nach Name.</span><span class="sxs-lookup"><span data-stu-id="121f9-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="121f9-112">Beispiel 2: Entfernen der virtuellen Netzwerkregel des PostgreSqlservers nach Identität</span><span class="sxs-lookup"><span data-stu-id="121f9-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="121f9-113">Mit diesen Cmdlets wird die virtuelle Netzwerkregel des PostgreSqlservers nach Identität entfernt.</span><span class="sxs-lookup"><span data-stu-id="121f9-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="121f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="121f9-114">PARAMETERS</span></span>

### <span data-ttu-id="121f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="121f9-115">-AsJob</span></span>
<span data-ttu-id="121f9-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="121f9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="121f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121f9-117">-DefaultProfile</span></span>
<span data-ttu-id="121f9-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="121f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="121f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="121f9-119">-InputObject</span></span>
<span data-ttu-id="121f9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="121f9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="121f9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="121f9-121">-Name</span></span>
<span data-ttu-id="121f9-122">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="121f9-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121f9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="121f9-123">-NoWait</span></span>
<span data-ttu-id="121f9-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="121f9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="121f9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="121f9-125">-PassThru</span></span>
<span data-ttu-id="121f9-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="121f9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="121f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="121f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="121f9-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="121f9-128">The name of the resource group.</span></span>
<span data-ttu-id="121f9-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="121f9-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121f9-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="121f9-130">-ServerName</span></span>
<span data-ttu-id="121f9-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="121f9-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121f9-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="121f9-132">-SubscriptionId</span></span>
<span data-ttu-id="121f9-133">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="121f9-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="121f9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="121f9-134">-Confirm</span></span>
<span data-ttu-id="121f9-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="121f9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="121f9-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="121f9-136">-WhatIf</span></span>
<span data-ttu-id="121f9-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="121f9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="121f9-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="121f9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="121f9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121f9-139">CommonParameters</span></span>
<span data-ttu-id="121f9-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="121f9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121f9-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="121f9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121f9-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="121f9-142">INPUTS</span></span>

### <span data-ttu-id="121f9-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="121f9-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="121f9-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="121f9-144">OUTPUTS</span></span>

### <span data-ttu-id="121f9-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="121f9-145">System.Boolean</span></span>

## <span data-ttu-id="121f9-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="121f9-146">NOTES</span></span>

<span data-ttu-id="121f9-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="121f9-147">ALIASES</span></span>

<span data-ttu-id="121f9-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="121f9-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="121f9-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="121f9-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="121f9-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="121f9-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="121f9-151">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="121f9-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="121f9-152">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="121f9-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="121f9-153">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="121f9-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="121f9-154">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="121f9-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="121f9-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="121f9-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="121f9-156">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="121f9-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="121f9-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="121f9-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="121f9-158">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="121f9-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="121f9-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="121f9-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="121f9-160">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="121f9-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="121f9-161">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="121f9-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="121f9-162">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="121f9-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="121f9-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="121f9-163">RELATED LINKS</span></span>

