---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restart-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 8e969551724a4965d17ce34e3b18c794705b764f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919424"
---
# <span data-ttu-id="7307f-101">Restart-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="7307f-101">Restart-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="7307f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7307f-102">SYNOPSIS</span></span>
<span data-ttu-id="7307f-103">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="7307f-103">Restarts a server.</span></span>

## <span data-ttu-id="7307f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7307f-104">SYNTAX</span></span>

### <span data-ttu-id="7307f-105">Neustart (Standard)</span><span class="sxs-lookup"><span data-stu-id="7307f-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7307f-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7307f-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7307f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7307f-107">DESCRIPTION</span></span>
<span data-ttu-id="7307f-108">Startet einen Server neu.</span><span class="sxs-lookup"><span data-stu-id="7307f-108">Restarts a server.</span></span>

## <span data-ttu-id="7307f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7307f-109">EXAMPLES</span></span>

### <span data-ttu-id="7307f-110">Beispiel 1: Neustarten des Servers nach Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="7307f-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="7307f-111">Neustarten des Servers nach Name</span><span class="sxs-lookup"><span data-stu-id="7307f-111">Restart the server by name</span></span>

### <span data-ttu-id="7307f-112">Beispiel 2: Neustarten des Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="7307f-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/restart"
PS C:\> Restart-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="7307f-113">Neustarten des Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="7307f-113">Restart the server by identity</span></span>

## <span data-ttu-id="7307f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7307f-114">PARAMETERS</span></span>

### <span data-ttu-id="7307f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7307f-115">-AsJob</span></span>
<span data-ttu-id="7307f-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="7307f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7307f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7307f-117">-DefaultProfile</span></span>
<span data-ttu-id="7307f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7307f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7307f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7307f-119">-InputObject</span></span>
<span data-ttu-id="7307f-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7307f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7307f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7307f-121">-Name</span></span>
<span data-ttu-id="7307f-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="7307f-122">The name of the server.</span></span>

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

### <span data-ttu-id="7307f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7307f-123">-NoWait</span></span>
<span data-ttu-id="7307f-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="7307f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7307f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7307f-125">-PassThru</span></span>
<span data-ttu-id="7307f-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7307f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7307f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7307f-127">-ResourceGroupName</span></span>
<span data-ttu-id="7307f-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7307f-128">The name of the resource group.</span></span>
<span data-ttu-id="7307f-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="7307f-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7307f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7307f-130">-SubscriptionId</span></span>
<span data-ttu-id="7307f-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7307f-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7307f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7307f-132">-Confirm</span></span>
<span data-ttu-id="7307f-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7307f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7307f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7307f-134">-WhatIf</span></span>
<span data-ttu-id="7307f-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7307f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7307f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7307f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7307f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7307f-137">CommonParameters</span></span>
<span data-ttu-id="7307f-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7307f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7307f-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7307f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7307f-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7307f-140">INPUTS</span></span>

### <span data-ttu-id="7307f-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7307f-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="7307f-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7307f-142">OUTPUTS</span></span>

### <span data-ttu-id="7307f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7307f-143">System.Boolean</span></span>

## <span data-ttu-id="7307f-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7307f-144">NOTES</span></span>

<span data-ttu-id="7307f-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7307f-145">ALIASES</span></span>

<span data-ttu-id="7307f-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7307f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7307f-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="7307f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7307f-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7307f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7307f-149">INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="7307f-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7307f-150">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7307f-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7307f-151">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7307f-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7307f-152">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="7307f-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7307f-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7307f-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7307f-154">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="7307f-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7307f-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7307f-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7307f-156">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="7307f-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="7307f-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7307f-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7307f-158">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="7307f-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7307f-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7307f-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7307f-160">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7307f-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7307f-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7307f-161">RELATED LINKS</span></span>

