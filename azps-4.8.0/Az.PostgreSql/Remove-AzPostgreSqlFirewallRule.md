---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 27f03ba80a01997d61bc50f6a644b4e3c4cffb7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165051"
---
# <span data-ttu-id="e64b8-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e64b8-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="e64b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e64b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e64b8-103">Löscht eine Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="e64b8-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="e64b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e64b8-104">SYNTAX</span></span>

### <span data-ttu-id="e64b8-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="e64b8-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e64b8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e64b8-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e64b8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e64b8-107">DESCRIPTION</span></span>
<span data-ttu-id="e64b8-108">Löscht eine Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="e64b8-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="e64b8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e64b8-109">EXAMPLES</span></span>

### <span data-ttu-id="e64b8-110">Beispiel 1: Entfernen der PostgreSQL-Firewall-Regel nach Namen</span><span class="sxs-lookup"><span data-stu-id="e64b8-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="e64b8-111">Dieses Cmdlet entfernt die PostgreSQL-Firewall-Regel nach Namen.</span><span class="sxs-lookup"><span data-stu-id="e64b8-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="e64b8-112">Beispiel 2: Entfernen der PostgreSQL-Firewall-Regel nach Identität</span><span class="sxs-lookup"><span data-stu-id="e64b8-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="e64b8-113">Diese Cmdlets entfernen die PostgreSQL-Firewall-Regel nach Identität.</span><span class="sxs-lookup"><span data-stu-id="e64b8-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="e64b8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e64b8-114">PARAMETERS</span></span>

### <span data-ttu-id="e64b8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e64b8-115">-AsJob</span></span>
<span data-ttu-id="e64b8-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e64b8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e64b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e64b8-117">-DefaultProfile</span></span>
<span data-ttu-id="e64b8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e64b8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e64b8-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e64b8-119">-InputObject</span></span>
<span data-ttu-id="e64b8-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e64b8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e64b8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e64b8-121">-Name</span></span>
<span data-ttu-id="e64b8-122">Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="e64b8-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="e64b8-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e64b8-123">-NoWait</span></span>
<span data-ttu-id="e64b8-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e64b8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e64b8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e64b8-125">-PassThru</span></span>
<span data-ttu-id="e64b8-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="e64b8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e64b8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e64b8-127">-ResourceGroupName</span></span>
<span data-ttu-id="e64b8-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e64b8-128">The name of the resource group.</span></span>
<span data-ttu-id="e64b8-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e64b8-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e64b8-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="e64b8-130">-ServerName</span></span>
<span data-ttu-id="e64b8-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e64b8-131">The name of the server.</span></span>

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

### <span data-ttu-id="e64b8-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e64b8-132">-SubscriptionId</span></span>
<span data-ttu-id="e64b8-133">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e64b8-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e64b8-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e64b8-134">-Confirm</span></span>
<span data-ttu-id="e64b8-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e64b8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e64b8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e64b8-136">-WhatIf</span></span>
<span data-ttu-id="e64b8-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e64b8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e64b8-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e64b8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e64b8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e64b8-139">CommonParameters</span></span>
<span data-ttu-id="e64b8-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e64b8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e64b8-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e64b8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e64b8-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e64b8-142">INPUTS</span></span>

### <span data-ttu-id="e64b8-143">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e64b8-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e64b8-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e64b8-144">OUTPUTS</span></span>

### <span data-ttu-id="e64b8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e64b8-145">System.Boolean</span></span>

## <span data-ttu-id="e64b8-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e64b8-146">NOTES</span></span>

<span data-ttu-id="e64b8-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="e64b8-147">ALIASES</span></span>

<span data-ttu-id="e64b8-148">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e64b8-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e64b8-149">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e64b8-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e64b8-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="e64b8-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e64b8-151">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="e64b8-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e64b8-152">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e64b8-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e64b8-153">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e64b8-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e64b8-154">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="e64b8-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e64b8-155">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="e64b8-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e64b8-156">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="e64b8-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e64b8-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e64b8-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e64b8-158">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e64b8-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="e64b8-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="e64b8-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e64b8-160">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e64b8-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e64b8-161">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e64b8-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e64b8-162">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e64b8-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e64b8-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e64b8-163">RELATED LINKS</span></span>

