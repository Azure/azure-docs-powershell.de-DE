---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293332"
---
# <span data-ttu-id="e0821-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0821-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="e0821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0821-102">SYNOPSIS</span></span>
<span data-ttu-id="e0821-103">Aktualisiert die Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="e0821-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="e0821-104">Verwenden Update-AzPostgreSqlServer, wenn Sie "AdministratorLoginPassword", "SKU" usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e0821-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="e0821-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0821-105">SYNTAX</span></span>

### <span data-ttu-id="e0821-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0821-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0821-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e0821-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0821-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0821-108">DESCRIPTION</span></span>
<span data-ttu-id="e0821-109">Aktualisiert die Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="e0821-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="e0821-110">Verwenden Update-AzPostgreSqlServer, wenn Sie "AdministratorLoginPassword", "SKU" usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e0821-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="e0821-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0821-111">EXAMPLES</span></span>

### <span data-ttu-id="e0821-112">Beispiel 1: Aktualisieren der Konfiguration von PostgreSql nach Name</span><span class="sxs-lookup"><span data-stu-id="e0821-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="e0821-113">Dieses Cmdlet aktualisiert die Konfiguration von PostgreSql nach Name.</span><span class="sxs-lookup"><span data-stu-id="e0821-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="e0821-114">Beispiel 2: Aktualisieren der Konfiguration von PostgreSql nach Identität.</span><span class="sxs-lookup"><span data-stu-id="e0821-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="e0821-115">Diese Cmdlets aktualisieren die Konfiguration von PostgreSql nach Identität.</span><span class="sxs-lookup"><span data-stu-id="e0821-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="e0821-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0821-116">PARAMETERS</span></span>

### <span data-ttu-id="e0821-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0821-117">-AsJob</span></span>
<span data-ttu-id="e0821-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e0821-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e0821-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0821-119">-DefaultProfile</span></span>
<span data-ttu-id="e0821-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0821-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0821-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0821-121">-InputObject</span></span>
<span data-ttu-id="e0821-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e0821-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0821-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e0821-123">-Name</span></span>
<span data-ttu-id="e0821-124">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0821-124">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0821-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e0821-125">-NoWait</span></span>
<span data-ttu-id="e0821-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e0821-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e0821-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0821-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0821-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0821-128">The name of the resource group.</span></span>
<span data-ttu-id="e0821-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="e0821-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e0821-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e0821-130">-ServerName</span></span>
<span data-ttu-id="e0821-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e0821-131">The name of the server.</span></span>

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

### <span data-ttu-id="e0821-132">-Source</span><span class="sxs-lookup"><span data-stu-id="e0821-132">-Source</span></span>
<span data-ttu-id="e0821-133">Quelle der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0821-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="e0821-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0821-134">-SubscriptionId</span></span>
<span data-ttu-id="e0821-135">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e0821-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e0821-136">-Value</span><span class="sxs-lookup"><span data-stu-id="e0821-136">-Value</span></span>
<span data-ttu-id="e0821-137">Wert der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0821-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="e0821-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0821-138">-Confirm</span></span>
<span data-ttu-id="e0821-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0821-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0821-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e0821-140">-WhatIf</span></span>
<span data-ttu-id="e0821-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0821-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0821-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0821-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0821-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0821-143">CommonParameters</span></span>
<span data-ttu-id="e0821-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0821-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0821-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0821-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0821-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0821-146">INPUTS</span></span>

### <span data-ttu-id="e0821-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e0821-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e0821-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0821-148">OUTPUTS</span></span>

### <span data-ttu-id="e0821-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0821-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="e0821-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e0821-150">NOTES</span></span>

<span data-ttu-id="e0821-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e0821-151">ALIASES</span></span>

<span data-ttu-id="e0821-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e0821-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0821-153">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e0821-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0821-154">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0821-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0821-155">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e0821-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0821-156">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0821-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e0821-157">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e0821-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e0821-158">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="e0821-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e0821-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e0821-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0821-160">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="e0821-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e0821-161">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0821-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e0821-162">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="e0821-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="e0821-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e0821-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e0821-164">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e0821-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e0821-165">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e0821-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e0821-166">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="e0821-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e0821-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e0821-167">RELATED LINKS</span></span>

