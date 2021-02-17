---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 2867c6f57967da64178e798f3e517715b44d07c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173025"
---
# <span data-ttu-id="2ce66-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="2ce66-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="2ce66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ce66-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce66-103">Erstellt eine neue Datenbank oder aktualisiert eine vorhandene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2ce66-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="2ce66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ce66-104">SYNTAX</span></span>

### <span data-ttu-id="2ce66-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ce66-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2ce66-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2ce66-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ce66-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ce66-107">DESCRIPTION</span></span>
<span data-ttu-id="2ce66-108">Erstellt eine neue Datenbank oder aktualisiert eine vorhandene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2ce66-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="2ce66-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ce66-109">EXAMPLES</span></span>

### <span data-ttu-id="2ce66-110">Beispiel 1: Aktualisieren einer MySql -Serverdatenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="2ce66-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="2ce66-111">Aktualisieren einer Datenbank nach Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="2ce66-111">Update a database by resource name.</span></span>

### <span data-ttu-id="2ce66-112">Beispiel 2: Aktualisieren der Datenbank MySql nach Parametern.</span><span class="sxs-lookup"><span data-stu-id="2ce66-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="2ce66-113">Aktualisieren einer Datenbank nach Parameter</span><span class="sxs-lookup"><span data-stu-id="2ce66-113">Update a database by parameter</span></span>

## <span data-ttu-id="2ce66-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ce66-114">PARAMETERS</span></span>

### <span data-ttu-id="2ce66-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ce66-115">-AsJob</span></span>
<span data-ttu-id="2ce66-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2ce66-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2ce66-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="2ce66-117">-Charset</span></span>
<span data-ttu-id="2ce66-118">Das Zeichenset der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2ce66-118">The charset of the database.</span></span>

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

### <span data-ttu-id="2ce66-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="2ce66-119">-Collation</span></span>
<span data-ttu-id="2ce66-120">Die Sortierung der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2ce66-120">The collation of the database.</span></span>

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

### <span data-ttu-id="2ce66-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce66-121">-DefaultProfile</span></span>
<span data-ttu-id="2ce66-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ce66-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ce66-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ce66-123">-InputObject</span></span>
<span data-ttu-id="2ce66-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2ce66-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2ce66-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2ce66-125">-Name</span></span>
<span data-ttu-id="2ce66-126">Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2ce66-126">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce66-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2ce66-127">-NoWait</span></span>
<span data-ttu-id="2ce66-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2ce66-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2ce66-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ce66-129">-ResourceGroupName</span></span>
<span data-ttu-id="2ce66-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2ce66-130">The name of the resource group.</span></span>
<span data-ttu-id="2ce66-131">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2ce66-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2ce66-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2ce66-132">-ServerName</span></span>
<span data-ttu-id="2ce66-133">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2ce66-133">The name of the server.</span></span>

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

### <span data-ttu-id="2ce66-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ce66-134">-SubscriptionId</span></span>
<span data-ttu-id="2ce66-135">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2ce66-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2ce66-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ce66-136">-Confirm</span></span>
<span data-ttu-id="2ce66-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ce66-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ce66-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2ce66-138">-WhatIf</span></span>
<span data-ttu-id="2ce66-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ce66-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ce66-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ce66-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ce66-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce66-141">CommonParameters</span></span>
<span data-ttu-id="2ce66-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce66-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce66-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ce66-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce66-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ce66-144">INPUTS</span></span>

### <span data-ttu-id="2ce66-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2ce66-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="2ce66-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ce66-146">OUTPUTS</span></span>

### <span data-ttu-id="2ce66-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="2ce66-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="2ce66-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2ce66-148">NOTES</span></span>

<span data-ttu-id="2ce66-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2ce66-149">ALIASES</span></span>

<span data-ttu-id="2ce66-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2ce66-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ce66-151">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2ce66-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ce66-152">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ce66-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ce66-153">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2ce66-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ce66-154">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2ce66-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2ce66-155">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2ce66-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2ce66-156">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="2ce66-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2ce66-157">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2ce66-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ce66-158">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="2ce66-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="2ce66-159">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="2ce66-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2ce66-160">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2ce66-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2ce66-161">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2ce66-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="2ce66-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2ce66-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2ce66-163">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2ce66-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2ce66-164">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2ce66-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2ce66-165">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2ce66-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2ce66-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2ce66-166">RELATED LINKS</span></span>

