---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
ms.openlocfilehash: 9e113eddbbc05dc55da75cccd7650cdf3adfdc74
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458955"
---
# <span data-ttu-id="a9dfd-101">Remove-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="a9dfd-101">Remove-AzMySqlServer</span></span>

## <span data-ttu-id="a9dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="a9dfd-103">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-103">Deletes a server.</span></span>

## <span data-ttu-id="a9dfd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9dfd-104">SYNTAX</span></span>

### <span data-ttu-id="a9dfd-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9dfd-105">Delete (Default)</span></span>
```
Remove-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a9dfd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9dfd-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a9dfd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9dfd-107">DESCRIPTION</span></span>
<span data-ttu-id="a9dfd-108">Löscht einen Server.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-108">Deletes a server.</span></span>

## <span data-ttu-id="a9dfd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9dfd-109">EXAMPLES</span></span>

### <span data-ttu-id="a9dfd-110">Beispiel 1: Entfernen des Server "MySql" nach "resourceGroup" und dem Servernamen</span><span class="sxs-lookup"><span data-stu-id="a9dfd-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="a9dfd-111">Dieses Cmdlet entfernt "MySql-Server" nach "resourceGroup" und "Servername".</span><span class="sxs-lookup"><span data-stu-id="a9dfd-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="a9dfd-112">Beispiel 2: Entfernen des Server "MySql" nach Identität</span><span class="sxs-lookup"><span data-stu-id="a9dfd-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Remove-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="a9dfd-113">Mit diesen Cmdlets wird der Server "MySql" nach Identität entfernt.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="a9dfd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9dfd-114">PARAMETERS</span></span>

### <span data-ttu-id="a9dfd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9dfd-115">-AsJob</span></span>
<span data-ttu-id="a9dfd-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a9dfd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a9dfd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9dfd-117">-DefaultProfile</span></span>
<span data-ttu-id="a9dfd-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9dfd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9dfd-119">-InputObject</span></span>
<span data-ttu-id="a9dfd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a9dfd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a9dfd-121">-Name</span></span>
<span data-ttu-id="a9dfd-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-122">The name of the server.</span></span>

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

### <span data-ttu-id="a9dfd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a9dfd-123">-NoWait</span></span>
<span data-ttu-id="a9dfd-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a9dfd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a9dfd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9dfd-125">-PassThru</span></span>
<span data-ttu-id="a9dfd-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a9dfd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9dfd-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9dfd-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-128">The name of the resource group.</span></span>
<span data-ttu-id="a9dfd-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a9dfd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9dfd-130">-SubscriptionId</span></span>
<span data-ttu-id="a9dfd-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a9dfd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9dfd-132">-Confirm</span></span>
<span data-ttu-id="a9dfd-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9dfd-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a9dfd-134">-WhatIf</span></span>
<span data-ttu-id="a9dfd-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9dfd-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9dfd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9dfd-137">CommonParameters</span></span>
<span data-ttu-id="a9dfd-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9dfd-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9dfd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9dfd-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9dfd-140">INPUTS</span></span>

### <span data-ttu-id="a9dfd-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a9dfd-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a9dfd-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9dfd-142">OUTPUTS</span></span>

### <span data-ttu-id="a9dfd-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9dfd-143">System.Boolean</span></span>

## <span data-ttu-id="a9dfd-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9dfd-144">NOTES</span></span>

<span data-ttu-id="a9dfd-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a9dfd-145">ALIASES</span></span>

<span data-ttu-id="a9dfd-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a9dfd-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9dfd-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9dfd-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9dfd-149">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a9dfd-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9dfd-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a9dfd-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a9dfd-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a9dfd-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a9dfd-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9dfd-154">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a9dfd-155">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a9dfd-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a9dfd-157">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="a9dfd-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a9dfd-159">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a9dfd-160">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a9dfd-161">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a9dfd-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a9dfd-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9dfd-162">RELATED LINKS</span></span>

