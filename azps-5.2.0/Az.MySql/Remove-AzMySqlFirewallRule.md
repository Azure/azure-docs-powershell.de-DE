---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
ms.openlocfilehash: 481761efe01646a10118d8ebfd645375caafbfef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297467"
---
# <span data-ttu-id="f2914-101">Remove-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f2914-101">Remove-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="f2914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2914-102">SYNOPSIS</span></span>
<span data-ttu-id="f2914-103">Löscht eine Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="f2914-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="f2914-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2914-104">SYNTAX</span></span>

### <span data-ttu-id="f2914-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2914-105">Delete (Default)</span></span>
```
Remove-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f2914-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2914-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2914-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2914-107">DESCRIPTION</span></span>
<span data-ttu-id="f2914-108">Löscht eine Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="f2914-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="f2914-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f2914-109">EXAMPLES</span></span>

### <span data-ttu-id="f2914-110">Beispiel 1: Entfernen der MySql-Firewallregel nach Name</span><span class="sxs-lookup"><span data-stu-id="f2914-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="f2914-111">Mit diesem Cmdlet wird die MySql-Firewallregel nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="f2914-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="f2914-112">Beispiel 2: Entfernen der MySql-Firewallregel nach Identität</span><span class="sxs-lookup"><span data-stu-id="f2914-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Remove-AzMySqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="f2914-113">Mit diesen Cmdlets wird die MySql-Firewallregel nach Identität entfernt.</span><span class="sxs-lookup"><span data-stu-id="f2914-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="f2914-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2914-114">PARAMETERS</span></span>

### <span data-ttu-id="f2914-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2914-115">-AsJob</span></span>
<span data-ttu-id="f2914-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f2914-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f2914-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2914-117">-DefaultProfile</span></span>
<span data-ttu-id="f2914-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2914-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2914-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2914-119">-InputObject</span></span>
<span data-ttu-id="f2914-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f2914-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2914-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f2914-121">-Name</span></span>
<span data-ttu-id="f2914-122">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="f2914-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2914-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f2914-123">-NoWait</span></span>
<span data-ttu-id="f2914-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f2914-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f2914-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2914-125">-PassThru</span></span>
<span data-ttu-id="f2914-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2914-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f2914-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2914-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2914-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f2914-128">The name of the resource group.</span></span>
<span data-ttu-id="f2914-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="f2914-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f2914-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f2914-130">-ServerName</span></span>
<span data-ttu-id="f2914-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f2914-131">The name of the server.</span></span>

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

### <span data-ttu-id="f2914-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2914-132">-SubscriptionId</span></span>
<span data-ttu-id="f2914-133">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f2914-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f2914-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2914-134">-Confirm</span></span>
<span data-ttu-id="f2914-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2914-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2914-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f2914-136">-WhatIf</span></span>
<span data-ttu-id="f2914-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2914-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2914-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2914-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2914-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2914-139">CommonParameters</span></span>
<span data-ttu-id="f2914-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2914-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2914-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2914-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2914-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f2914-142">INPUTS</span></span>

### <span data-ttu-id="f2914-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f2914-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f2914-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f2914-144">OUTPUTS</span></span>

### <span data-ttu-id="f2914-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2914-145">System.Boolean</span></span>

## <span data-ttu-id="f2914-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f2914-146">NOTES</span></span>

<span data-ttu-id="f2914-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f2914-147">ALIASES</span></span>

<span data-ttu-id="f2914-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f2914-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2914-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f2914-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2914-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2914-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2914-151">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="f2914-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2914-152">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f2914-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f2914-153">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f2914-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f2914-154">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="f2914-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f2914-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f2914-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2914-156">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="f2914-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="f2914-157">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="f2914-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f2914-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f2914-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f2914-159">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="f2914-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="f2914-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f2914-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f2914-161">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f2914-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f2914-162">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f2914-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f2914-163">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f2914-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f2914-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f2914-164">RELATED LINKS</span></span>

