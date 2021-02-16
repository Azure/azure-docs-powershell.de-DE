---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146321"
---
# <span data-ttu-id="26d84-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="26d84-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="26d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26d84-102">SYNOPSIS</span></span>
<span data-ttu-id="26d84-103">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="26d84-103">Restarts a server.</span></span>

## <span data-ttu-id="26d84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26d84-104">SYNTAX</span></span>

### <span data-ttu-id="26d84-105">Neu starten (Standard)</span><span class="sxs-lookup"><span data-stu-id="26d84-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26d84-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="26d84-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="26d84-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26d84-107">DESCRIPTION</span></span>
<span data-ttu-id="26d84-108">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="26d84-108">Restarts a server.</span></span>

## <span data-ttu-id="26d84-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26d84-109">EXAMPLES</span></span>

### <span data-ttu-id="26d84-110">Beispiel 1: Neustarten des PostgreSql-Servers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="26d84-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="26d84-111">Dieses Cmdlet startet den PostgreSql-Server nach Ressourcengruppe und Servername neu.</span><span class="sxs-lookup"><span data-stu-id="26d84-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="26d84-112">Beispiel 2: Neustarten des PostgreSqlservers nach Identität</span><span class="sxs-lookup"><span data-stu-id="26d84-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="26d84-113">Diese Cmdlets starten den Server von PostgreSql nach Identität neu.</span><span class="sxs-lookup"><span data-stu-id="26d84-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="26d84-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26d84-114">PARAMETERS</span></span>

### <span data-ttu-id="26d84-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26d84-115">-AsJob</span></span>
<span data-ttu-id="26d84-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="26d84-116">Run the command as a job</span></span>

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

### <span data-ttu-id="26d84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26d84-117">-DefaultProfile</span></span>
<span data-ttu-id="26d84-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26d84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26d84-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26d84-119">-InputObject</span></span>
<span data-ttu-id="26d84-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="26d84-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26d84-121">-Name</span><span class="sxs-lookup"><span data-stu-id="26d84-121">-Name</span></span>
<span data-ttu-id="26d84-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="26d84-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d84-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="26d84-123">-NoWait</span></span>
<span data-ttu-id="26d84-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="26d84-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="26d84-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26d84-125">-PassThru</span></span>
<span data-ttu-id="26d84-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="26d84-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="26d84-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26d84-127">-ResourceGroupName</span></span>
<span data-ttu-id="26d84-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="26d84-128">The name of the resource group.</span></span>
<span data-ttu-id="26d84-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="26d84-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d84-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26d84-130">-SubscriptionId</span></span>
<span data-ttu-id="26d84-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="26d84-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d84-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26d84-132">-Confirm</span></span>
<span data-ttu-id="26d84-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26d84-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26d84-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="26d84-134">-WhatIf</span></span>
<span data-ttu-id="26d84-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26d84-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26d84-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26d84-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26d84-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26d84-137">CommonParameters</span></span>
<span data-ttu-id="26d84-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26d84-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26d84-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26d84-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26d84-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26d84-140">INPUTS</span></span>

### <span data-ttu-id="26d84-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="26d84-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="26d84-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26d84-142">OUTPUTS</span></span>

### <span data-ttu-id="26d84-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26d84-143">System.Boolean</span></span>

## <span data-ttu-id="26d84-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="26d84-144">NOTES</span></span>

<span data-ttu-id="26d84-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="26d84-145">ALIASES</span></span>

<span data-ttu-id="26d84-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="26d84-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="26d84-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="26d84-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26d84-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="26d84-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="26d84-149">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="26d84-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="26d84-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="26d84-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="26d84-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="26d84-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="26d84-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="26d84-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="26d84-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="26d84-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="26d84-154">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="26d84-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="26d84-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="26d84-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="26d84-156">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="26d84-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="26d84-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="26d84-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="26d84-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="26d84-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="26d84-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="26d84-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="26d84-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="26d84-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="26d84-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="26d84-161">RELATED LINKS</span></span>

