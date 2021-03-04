---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/remove-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
ms.openlocfilehash: 18e502fa0f41643355877dfbb144962e701e03f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924027"
---
# <span data-ttu-id="c3889-101">Remove-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c3889-101">Remove-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="c3889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3889-102">SYNOPSIS</span></span>
<span data-ttu-id="c3889-103">Löscht eine Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="c3889-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="c3889-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3889-104">SYNTAX</span></span>

### <span data-ttu-id="c3889-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3889-105">Delete (Default)</span></span>
```
Remove-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c3889-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c3889-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3889-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3889-107">DESCRIPTION</span></span>
<span data-ttu-id="c3889-108">Löscht eine Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="c3889-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="c3889-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c3889-109">EXAMPLES</span></span>

### <span data-ttu-id="c3889-110">Beispiel 1: Entfernen der MySql-Firewallregel nach Name</span><span class="sxs-lookup"><span data-stu-id="c3889-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="c3889-111">Dieses Cmdlet entfernt die MySql-Firewallregel nach Name.</span><span class="sxs-lookup"><span data-stu-id="c3889-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="c3889-112">Beispiel 2: Entfernen der MySql-Firewallregel nach Identität</span><span class="sxs-lookup"><span data-stu-id="c3889-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Remove-AzMySqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="c3889-113">Diese Cmdlets entfernen Die MySql-Firewallregel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="c3889-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="c3889-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c3889-114">PARAMETERS</span></span>

### <span data-ttu-id="c3889-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3889-115">-AsJob</span></span>
<span data-ttu-id="c3889-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c3889-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c3889-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3889-117">-DefaultProfile</span></span>
<span data-ttu-id="c3889-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3889-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3889-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3889-119">-InputObject</span></span>
<span data-ttu-id="c3889-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c3889-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c3889-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c3889-121">-Name</span></span>
<span data-ttu-id="c3889-122">Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="c3889-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="c3889-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c3889-123">-NoWait</span></span>
<span data-ttu-id="c3889-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c3889-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c3889-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3889-125">-PassThru</span></span>
<span data-ttu-id="c3889-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3889-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c3889-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3889-127">-ResourceGroupName</span></span>
<span data-ttu-id="c3889-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c3889-128">The name of the resource group.</span></span>
<span data-ttu-id="c3889-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="c3889-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c3889-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="c3889-130">-ServerName</span></span>
<span data-ttu-id="c3889-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="c3889-131">The name of the server.</span></span>

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

### <span data-ttu-id="c3889-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3889-132">-SubscriptionId</span></span>
<span data-ttu-id="c3889-133">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c3889-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c3889-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3889-134">-Confirm</span></span>
<span data-ttu-id="c3889-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3889-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3889-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3889-136">-WhatIf</span></span>
<span data-ttu-id="c3889-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3889-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3889-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3889-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3889-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3889-139">CommonParameters</span></span>
<span data-ttu-id="c3889-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3889-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3889-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3889-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3889-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c3889-142">INPUTS</span></span>

### <span data-ttu-id="c3889-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c3889-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c3889-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c3889-144">OUTPUTS</span></span>

### <span data-ttu-id="c3889-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3889-145">System.Boolean</span></span>

## <span data-ttu-id="c3889-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c3889-146">NOTES</span></span>

<span data-ttu-id="c3889-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c3889-147">ALIASES</span></span>

<span data-ttu-id="c3889-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c3889-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3889-149">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c3889-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3889-150">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c3889-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3889-151">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="c3889-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3889-152">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c3889-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c3889-153">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c3889-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c3889-154">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="c3889-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c3889-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="c3889-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3889-156">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="c3889-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c3889-157">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="c3889-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c3889-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c3889-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c3889-159">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="c3889-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="c3889-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="c3889-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c3889-161">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="c3889-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c3889-162">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c3889-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c3889-163">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c3889-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c3889-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c3889-164">RELATED LINKS</span></span>

