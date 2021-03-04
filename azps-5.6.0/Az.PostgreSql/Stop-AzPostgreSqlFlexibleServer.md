---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/stop-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Stop-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Stop-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: d51946f9d358a7a7ccffff5e4621248d7c89fa9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919400"
---
# <span data-ttu-id="b864a-101">Stop-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="b864a-101">Stop-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="b864a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b864a-102">SYNOPSIS</span></span>
<span data-ttu-id="b864a-103">Beendet einen Server.</span><span class="sxs-lookup"><span data-stu-id="b864a-103">Stops a server.</span></span>

## <span data-ttu-id="b864a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b864a-104">SYNTAX</span></span>

### <span data-ttu-id="b864a-105">Beenden (Standard)</span><span class="sxs-lookup"><span data-stu-id="b864a-105">Stop (Default)</span></span>
```
Stop-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b864a-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b864a-106">StopViaIdentity</span></span>
```
Stop-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b864a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b864a-107">DESCRIPTION</span></span>
<span data-ttu-id="b864a-108">Beendet einen Server.</span><span class="sxs-lookup"><span data-stu-id="b864a-108">Stops a server.</span></span>

## <span data-ttu-id="b864a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b864a-109">EXAMPLES</span></span>

### <span data-ttu-id="b864a-110">Beispiel 1: Beenden des Servers nach Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="b864a-110">Example 1: Stop the server by resource name</span></span>
```powershell
PS C:\> Stop-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="b864a-111">Beenden des Servers nach Name</span><span class="sxs-lookup"><span data-stu-id="b864a-111">Stop the server by name</span></span>

### <span data-ttu-id="b864a-112">Beispiel 2: Beenden des Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="b864a-112">Example 2: Stop the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/stop"
PS C:\> Stop-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="b864a-113">Beenden des Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="b864a-113">Stop the server by identity</span></span>

## <span data-ttu-id="b864a-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b864a-114">PARAMETERS</span></span>

### <span data-ttu-id="b864a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b864a-115">-AsJob</span></span>
<span data-ttu-id="b864a-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b864a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b864a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b864a-117">-DefaultProfile</span></span>
<span data-ttu-id="b864a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b864a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b864a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b864a-119">-InputObject</span></span>
<span data-ttu-id="b864a-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b864a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b864a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b864a-121">-Name</span></span>
<span data-ttu-id="b864a-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="b864a-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b864a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b864a-123">-NoWait</span></span>
<span data-ttu-id="b864a-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b864a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b864a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b864a-125">-PassThru</span></span>
<span data-ttu-id="b864a-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b864a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b864a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b864a-127">-ResourceGroupName</span></span>
<span data-ttu-id="b864a-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b864a-128">The name of the resource group.</span></span>
<span data-ttu-id="b864a-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="b864a-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b864a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b864a-130">-SubscriptionId</span></span>
<span data-ttu-id="b864a-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="b864a-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b864a-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b864a-132">-Confirm</span></span>
<span data-ttu-id="b864a-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b864a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b864a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b864a-134">-WhatIf</span></span>
<span data-ttu-id="b864a-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b864a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b864a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b864a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b864a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b864a-137">CommonParameters</span></span>
<span data-ttu-id="b864a-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b864a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b864a-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b864a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b864a-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b864a-140">INPUTS</span></span>

### <span data-ttu-id="b864a-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b864a-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b864a-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b864a-142">OUTPUTS</span></span>

### <span data-ttu-id="b864a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b864a-143">System.Boolean</span></span>

## <span data-ttu-id="b864a-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b864a-144">NOTES</span></span>

<span data-ttu-id="b864a-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b864a-145">ALIASES</span></span>

<span data-ttu-id="b864a-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b864a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b864a-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b864a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b864a-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b864a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b864a-149">INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="b864a-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b864a-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b864a-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b864a-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b864a-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b864a-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="b864a-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b864a-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b864a-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b864a-154">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="b864a-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b864a-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b864a-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b864a-156">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="b864a-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="b864a-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b864a-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b864a-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="b864a-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b864a-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="b864a-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b864a-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="b864a-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b864a-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b864a-161">RELATED LINKS</span></span>

