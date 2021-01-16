---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlServer.md
ms.openlocfilehash: 6b0544bb2394b4d69c496ec4f2502360ddf173bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293344"
---
# <span data-ttu-id="76069-101">Remove-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="76069-101">Remove-AzPostgreSqlServer</span></span>

## <span data-ttu-id="76069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76069-102">SYNOPSIS</span></span>
<span data-ttu-id="76069-103">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="76069-103">Deletes a server.</span></span>

## <span data-ttu-id="76069-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76069-104">SYNTAX</span></span>

### <span data-ttu-id="76069-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="76069-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76069-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76069-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76069-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76069-107">DESCRIPTION</span></span>
<span data-ttu-id="76069-108">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="76069-108">Deletes a server.</span></span>

## <span data-ttu-id="76069-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76069-109">EXAMPLES</span></span>

### <span data-ttu-id="76069-110">Beispiel 1: Entfernen des PostgreSql-Servers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="76069-110">Example 1: Remove PostgreSql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="76069-111">Dieses Cmdlet entfernt "PostgreSql-Server" nach "resourceGroup" und "Servername".</span><span class="sxs-lookup"><span data-stu-id="76069-111">This cmdlet removes PostgreSql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="76069-112">Beispiel 2: Entfernen des PostgreSql-Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="76069-112">Example 2: Remove PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer"
PS C:\> Remove-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="76069-113">Diese Cmdlets entfernen den PostgreSql-Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="76069-113">These cmdlets remove PostgreSql server by identity.</span></span>

## <span data-ttu-id="76069-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76069-114">PARAMETERS</span></span>

### <span data-ttu-id="76069-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76069-115">-AsJob</span></span>
<span data-ttu-id="76069-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="76069-116">Run the command as a job</span></span>

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

### <span data-ttu-id="76069-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76069-117">-DefaultProfile</span></span>
<span data-ttu-id="76069-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76069-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76069-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76069-119">-InputObject</span></span>
<span data-ttu-id="76069-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="76069-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="76069-121">-Name</span><span class="sxs-lookup"><span data-stu-id="76069-121">-Name</span></span>
<span data-ttu-id="76069-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="76069-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76069-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="76069-123">-NoWait</span></span>
<span data-ttu-id="76069-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="76069-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76069-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76069-125">-PassThru</span></span>
<span data-ttu-id="76069-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="76069-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="76069-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76069-127">-ResourceGroupName</span></span>
<span data-ttu-id="76069-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="76069-128">The name of the resource group.</span></span>
<span data-ttu-id="76069-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="76069-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="76069-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76069-130">-SubscriptionId</span></span>
<span data-ttu-id="76069-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="76069-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="76069-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76069-132">-Confirm</span></span>
<span data-ttu-id="76069-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76069-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76069-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76069-134">-WhatIf</span></span>
<span data-ttu-id="76069-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76069-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76069-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76069-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76069-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76069-137">CommonParameters</span></span>
<span data-ttu-id="76069-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76069-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76069-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76069-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76069-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76069-140">INPUTS</span></span>

### <span data-ttu-id="76069-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="76069-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="76069-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76069-142">OUTPUTS</span></span>

### <span data-ttu-id="76069-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76069-143">System.Boolean</span></span>

## <span data-ttu-id="76069-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76069-144">NOTES</span></span>

<span data-ttu-id="76069-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="76069-145">ALIASES</span></span>

<span data-ttu-id="76069-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="76069-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76069-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76069-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76069-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76069-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76069-149">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="76069-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76069-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="76069-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="76069-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="76069-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="76069-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="76069-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="76069-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="76069-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76069-154">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="76069-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="76069-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="76069-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="76069-156">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="76069-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="76069-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="76069-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="76069-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="76069-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="76069-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="76069-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="76069-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="76069-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="76069-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76069-161">RELATED LINKS</span></span>

