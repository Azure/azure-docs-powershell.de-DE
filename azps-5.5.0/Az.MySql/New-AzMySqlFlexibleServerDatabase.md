---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9d8933aad3b3e24893062e43a3b3232bd0b57cfb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159337"
---
# <span data-ttu-id="2f286-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="2f286-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="2f286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f286-102">SYNOPSIS</span></span>
<span data-ttu-id="2f286-103">Erstellt eine neue Datenbank oder aktualisiert eine vorhandene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2f286-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="2f286-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f286-104">SYNTAX</span></span>

### <span data-ttu-id="2f286-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f286-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2f286-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2f286-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2f286-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f286-107">DESCRIPTION</span></span>
<span data-ttu-id="2f286-108">Erstellt eine neue Datenbank oder aktualisiert eine vorhandene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2f286-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="2f286-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f286-109">EXAMPLES</span></span>

### <span data-ttu-id="2f286-110">Beispiel 1: Erstellen einer neuen MySql -Serverdatenbank</span><span class="sxs-lookup"><span data-stu-id="2f286-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="2f286-111">Erstellen Sie eine Datenbank mit Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="2f286-111">Create a database with default settings.</span></span>

## <span data-ttu-id="2f286-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f286-112">PARAMETERS</span></span>

### <span data-ttu-id="2f286-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f286-113">-AsJob</span></span>
<span data-ttu-id="2f286-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2f286-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2f286-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="2f286-115">-Charset</span></span>
<span data-ttu-id="2f286-116">Das Zeichenset der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2f286-116">The charset of the database.</span></span>

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

### <span data-ttu-id="2f286-117">-Collation</span><span class="sxs-lookup"><span data-stu-id="2f286-117">-Collation</span></span>
<span data-ttu-id="2f286-118">Die Sortierung der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2f286-118">The collation of the database.</span></span>

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

### <span data-ttu-id="2f286-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f286-119">-DefaultProfile</span></span>
<span data-ttu-id="2f286-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f286-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f286-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f286-121">-InputObject</span></span>
<span data-ttu-id="2f286-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2f286-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f286-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2f286-123">-Name</span></span>
<span data-ttu-id="2f286-124">Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2f286-124">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f286-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2f286-125">-NoWait</span></span>
<span data-ttu-id="2f286-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2f286-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2f286-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f286-127">-ResourceGroupName</span></span>
<span data-ttu-id="2f286-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f286-128">The name of the resource group.</span></span>
<span data-ttu-id="2f286-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2f286-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f286-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f286-130">-ServerName</span></span>
<span data-ttu-id="2f286-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2f286-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f286-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f286-132">-SubscriptionId</span></span>
<span data-ttu-id="2f286-133">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2f286-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f286-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f286-134">-Confirm</span></span>
<span data-ttu-id="2f286-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f286-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f286-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2f286-136">-WhatIf</span></span>
<span data-ttu-id="2f286-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f286-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f286-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f286-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f286-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f286-139">CommonParameters</span></span>
<span data-ttu-id="2f286-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f286-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f286-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f286-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f286-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f286-142">INPUTS</span></span>

### <span data-ttu-id="2f286-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2f286-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="2f286-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f286-144">OUTPUTS</span></span>

### <span data-ttu-id="2f286-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="2f286-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="2f286-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2f286-146">NOTES</span></span>

<span data-ttu-id="2f286-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2f286-147">ALIASES</span></span>

<span data-ttu-id="2f286-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2f286-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2f286-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f286-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2f286-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2f286-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2f286-151">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2f286-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2f286-152">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2f286-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2f286-153">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2f286-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2f286-154">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="2f286-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2f286-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2f286-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2f286-156">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="2f286-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="2f286-157">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="2f286-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2f286-158">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f286-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2f286-159">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2f286-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="2f286-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2f286-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2f286-161">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2f286-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2f286-162">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2f286-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2f286-163">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2f286-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2f286-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2f286-164">RELATED LINKS</span></span>

