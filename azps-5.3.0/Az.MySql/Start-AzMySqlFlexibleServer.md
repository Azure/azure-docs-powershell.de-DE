---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/start-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
ms.openlocfilehash: bdda5653a3b7f612fc96d3522bffe15e92649bbe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467524"
---
# <span data-ttu-id="2a923-101">Start-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="2a923-101">Start-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="2a923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a923-102">SYNOPSIS</span></span>
<span data-ttu-id="2a923-103">Startet einen Server.</span><span class="sxs-lookup"><span data-stu-id="2a923-103">Starts a server.</span></span>

## <span data-ttu-id="2a923-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a923-104">SYNTAX</span></span>

### <span data-ttu-id="2a923-105">Start (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a923-105">Start (Default)</span></span>
```
Start-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2a923-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2a923-106">StartViaIdentity</span></span>
```
Start-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2a923-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a923-107">DESCRIPTION</span></span>
<span data-ttu-id="2a923-108">Startet einen Server.</span><span class="sxs-lookup"><span data-stu-id="2a923-108">Starts a server.</span></span>

## <span data-ttu-id="2a923-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a923-109">EXAMPLES</span></span>

### <span data-ttu-id="2a923-110">Beispiel 1: Starten des Servers nach Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="2a923-110">Example 1: Start the server by resource name</span></span>
```powershell
PS C:\> Start-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="2a923-111">Starten des Servers nach Name</span><span class="sxs-lookup"><span data-stu-id="2a923-111">Start the server by name</span></span>

### <span data-ttu-id="2a923-112">Beispiel 2: Starten des Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="2a923-112">Example 2: Start the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/start"
PS C:\> Start-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="2a923-113">Starten des Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="2a923-113">Start the server by identity</span></span>

## <span data-ttu-id="2a923-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a923-114">PARAMETERS</span></span>

### <span data-ttu-id="2a923-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a923-115">-AsJob</span></span>
<span data-ttu-id="2a923-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2a923-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2a923-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a923-117">-DefaultProfile</span></span>
<span data-ttu-id="2a923-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a923-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a923-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a923-119">-InputObject</span></span>
<span data-ttu-id="2a923-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2a923-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2a923-121">-Name</span></span>
<span data-ttu-id="2a923-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2a923-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2a923-123">-NoWait</span></span>
<span data-ttu-id="2a923-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2a923-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2a923-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a923-125">-PassThru</span></span>
<span data-ttu-id="2a923-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2a923-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2a923-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a923-127">-ResourceGroupName</span></span>
<span data-ttu-id="2a923-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2a923-128">The name of the resource group.</span></span>
<span data-ttu-id="2a923-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2a923-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a923-130">-SubscriptionId</span></span>
<span data-ttu-id="2a923-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2a923-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a923-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a923-132">-Confirm</span></span>
<span data-ttu-id="2a923-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a923-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a923-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2a923-134">-WhatIf</span></span>
<span data-ttu-id="2a923-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a923-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a923-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a923-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a923-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a923-137">CommonParameters</span></span>
<span data-ttu-id="2a923-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a923-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a923-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a923-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a923-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a923-140">INPUTS</span></span>

### <span data-ttu-id="2a923-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2a923-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="2a923-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a923-142">OUTPUTS</span></span>

### <span data-ttu-id="2a923-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a923-143">System.Boolean</span></span>

## <span data-ttu-id="2a923-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2a923-144">NOTES</span></span>

<span data-ttu-id="2a923-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2a923-145">ALIASES</span></span>

<span data-ttu-id="2a923-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2a923-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a923-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a923-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a923-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a923-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a923-149">INPUTOBJECT <IMySqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2a923-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2a923-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2a923-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2a923-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2a923-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2a923-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="2a923-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2a923-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2a923-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2a923-154">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="2a923-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="2a923-155">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="2a923-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2a923-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2a923-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2a923-157">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="2a923-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="2a923-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2a923-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2a923-159">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2a923-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2a923-160">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2a923-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2a923-161">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2a923-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2a923-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2a923-162">RELATED LINKS</span></span>

