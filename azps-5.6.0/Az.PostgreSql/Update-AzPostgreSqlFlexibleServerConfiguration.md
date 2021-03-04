---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: e45d342f7bb02034b2adf0473e6d4d1eb3c2b370
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929944"
---
# <span data-ttu-id="f0d08-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0d08-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="f0d08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0d08-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d08-103">Aktualisiert eine Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="f0d08-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="f0d08-104">Verwenden Update-AzPostgreSqlFlexibleServer sie stattdessen, wenn Sie AdministratorLoginPassword, Sku usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f0d08-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="f0d08-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0d08-105">SYNTAX</span></span>

### <span data-ttu-id="f0d08-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0d08-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f0d08-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f0d08-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f0d08-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0d08-108">DESCRIPTION</span></span>
<span data-ttu-id="f0d08-109">Aktualisiert eine Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="f0d08-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="f0d08-110">Verwenden Update-AzPostgreSqlFlexibleServer sie stattdessen, wenn Sie AdministratorLoginPassword, Sku usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f0d08-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="f0d08-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0d08-111">EXAMPLES</span></span>

### <span data-ttu-id="f0d08-112">Beispiel 1: Updatae-angegebene PostgreSql-Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="f0d08-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="f0d08-113">Dieses Cmdlet aktualisiert die angegebene PostgreSql-Konfiguration nach Name.</span><span class="sxs-lookup"><span data-stu-id="f0d08-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="f0d08-114">Beispiel 1: Updatae-angegebene PostgreSql-Konfiguration nach Identität</span><span class="sxs-lookup"><span data-stu-id="f0d08-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="f0d08-115">Dieses Cmdlet aktualisiert die angegebene PostgreSql-Konfiguration nach Identität.</span><span class="sxs-lookup"><span data-stu-id="f0d08-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="f0d08-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f0d08-116">PARAMETERS</span></span>

### <span data-ttu-id="f0d08-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0d08-117">-AsJob</span></span>
<span data-ttu-id="f0d08-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f0d08-118">Run the command as a job</span></span>

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

### <span data-ttu-id="f0d08-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d08-119">-DefaultProfile</span></span>
<span data-ttu-id="f0d08-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0d08-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0d08-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0d08-121">-InputObject</span></span>
<span data-ttu-id="f0d08-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f0d08-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f0d08-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f0d08-123">-Name</span></span>
<span data-ttu-id="f0d08-124">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f0d08-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="f0d08-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f0d08-125">-NoWait</span></span>
<span data-ttu-id="f0d08-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f0d08-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f0d08-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d08-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0d08-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0d08-128">The name of the resource group.</span></span>
<span data-ttu-id="f0d08-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="f0d08-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f0d08-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="f0d08-130">-ServerName</span></span>
<span data-ttu-id="f0d08-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f0d08-131">The name of the server.</span></span>

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

### <span data-ttu-id="f0d08-132">-Source</span><span class="sxs-lookup"><span data-stu-id="f0d08-132">-Source</span></span>
<span data-ttu-id="f0d08-133">Quelle der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f0d08-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="f0d08-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0d08-134">-SubscriptionId</span></span>
<span data-ttu-id="f0d08-135">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f0d08-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f0d08-136">-Wert</span><span class="sxs-lookup"><span data-stu-id="f0d08-136">-Value</span></span>
<span data-ttu-id="f0d08-137">Wert der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f0d08-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="f0d08-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0d08-138">-Confirm</span></span>
<span data-ttu-id="f0d08-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0d08-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0d08-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d08-140">-WhatIf</span></span>
<span data-ttu-id="f0d08-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0d08-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0d08-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0d08-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0d08-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d08-143">CommonParameters</span></span>
<span data-ttu-id="f0d08-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d08-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d08-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0d08-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d08-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0d08-146">INPUTS</span></span>

### <span data-ttu-id="f0d08-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f0d08-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="f0d08-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0d08-148">OUTPUTS</span></span>

### <span data-ttu-id="f0d08-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="f0d08-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="f0d08-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f0d08-150">NOTES</span></span>

<span data-ttu-id="f0d08-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f0d08-151">ALIASES</span></span>

<span data-ttu-id="f0d08-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f0d08-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0d08-153">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="f0d08-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0d08-154">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f0d08-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0d08-155">INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="f0d08-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0d08-156">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f0d08-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f0d08-157">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f0d08-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f0d08-158">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="f0d08-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f0d08-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f0d08-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0d08-160">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="f0d08-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f0d08-161">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0d08-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f0d08-162">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="f0d08-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="f0d08-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f0d08-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f0d08-164">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f0d08-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f0d08-165">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f0d08-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f0d08-166">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f0d08-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f0d08-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f0d08-167">RELATED LINKS</span></span>

