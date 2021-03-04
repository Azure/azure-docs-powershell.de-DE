---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/remove-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: c2bb8923a9844563f128866c324688d23413a641
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919432"
---
# <span data-ttu-id="15e4f-101">Remove-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="15e4f-101">Remove-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="15e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="15e4f-103">Löscht eine PostgreSQL-Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="15e4f-103">Deletes a PostgreSQL server firewall rule.</span></span>

## <span data-ttu-id="15e4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15e4f-104">SYNTAX</span></span>

### <span data-ttu-id="15e4f-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="15e4f-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="15e4f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15e4f-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15e4f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15e4f-107">DESCRIPTION</span></span>
<span data-ttu-id="15e4f-108">Löscht eine PostgreSQL-Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="15e4f-108">Deletes a PostgreSQL server firewall rule.</span></span>

## <span data-ttu-id="15e4f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15e4f-109">EXAMPLES</span></span>

### <span data-ttu-id="15e4f-110">Beispiel 1: Entfernen der PostgreSql-Firewallregel nach Name</span><span class="sxs-lookup"><span data-stu-id="15e4f-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFlexibleServerFirewallRule -Name firewall-rule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

```

<span data-ttu-id="15e4f-111">Dieses Cmdlet entfernt die PostgreSql-Firewallregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="15e4f-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="15e4f-112">Beispiel 2: Entfernen der PostgreSql-Firewallregel nach Identität</span><span class="sxs-lookup"><span data-stu-id="15e4f-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/firewall-rule-test"
PS C:\> Remove-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID
 
```

<span data-ttu-id="15e4f-113">Diese Cmdlets entfernen die PostgreSql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="15e4f-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="15e4f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="15e4f-114">PARAMETERS</span></span>

### <span data-ttu-id="15e4f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15e4f-115">-AsJob</span></span>
<span data-ttu-id="15e4f-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="15e4f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="15e4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e4f-117">-DefaultProfile</span></span>
<span data-ttu-id="15e4f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15e4f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15e4f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15e4f-119">-InputObject</span></span>
<span data-ttu-id="15e4f-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="15e4f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15e4f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="15e4f-121">-Name</span></span>
<span data-ttu-id="15e4f-122">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="15e4f-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="15e4f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="15e4f-123">-NoWait</span></span>
<span data-ttu-id="15e4f-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="15e4f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="15e4f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15e4f-125">-PassThru</span></span>
<span data-ttu-id="15e4f-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15e4f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="15e4f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15e4f-127">-ResourceGroupName</span></span>
<span data-ttu-id="15e4f-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15e4f-128">The name of the resource group.</span></span>
<span data-ttu-id="15e4f-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="15e4f-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="15e4f-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="15e4f-130">-ServerName</span></span>
<span data-ttu-id="15e4f-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="15e4f-131">The name of the server.</span></span>

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

### <span data-ttu-id="15e4f-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15e4f-132">-SubscriptionId</span></span>
<span data-ttu-id="15e4f-133">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="15e4f-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="15e4f-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15e4f-134">-Confirm</span></span>
<span data-ttu-id="15e4f-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15e4f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15e4f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15e4f-136">-WhatIf</span></span>
<span data-ttu-id="15e4f-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15e4f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15e4f-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15e4f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15e4f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e4f-139">CommonParameters</span></span>
<span data-ttu-id="15e4f-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15e4f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e4f-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15e4f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e4f-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15e4f-142">INPUTS</span></span>

### <span data-ttu-id="15e4f-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="15e4f-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="15e4f-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15e4f-144">OUTPUTS</span></span>

### <span data-ttu-id="15e4f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="15e4f-145">System.Boolean</span></span>

## <span data-ttu-id="15e4f-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="15e4f-146">NOTES</span></span>

<span data-ttu-id="15e4f-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="15e4f-147">ALIASES</span></span>

<span data-ttu-id="15e4f-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="15e4f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15e4f-149">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="15e4f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15e4f-150">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="15e4f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15e4f-151">INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="15e4f-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15e4f-152">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="15e4f-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="15e4f-153">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="15e4f-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="15e4f-154">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="15e4f-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="15e4f-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="15e4f-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15e4f-156">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="15e4f-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="15e4f-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15e4f-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="15e4f-158">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="15e4f-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="15e4f-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="15e4f-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="15e4f-160">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="15e4f-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="15e4f-161">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="15e4f-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="15e4f-162">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="15e4f-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="15e4f-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="15e4f-163">RELATED LINKS</span></span>

