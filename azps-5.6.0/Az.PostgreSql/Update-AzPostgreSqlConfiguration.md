---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: c0af624683e3d12cc1b12c057caa419c5633d45f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919379"
---
# <span data-ttu-id="2e452-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e452-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="2e452-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e452-102">SYNOPSIS</span></span>
<span data-ttu-id="2e452-103">Aktualisiert eine Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="2e452-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="2e452-104">Verwenden Update-AzPostgreSqlServer sie stattdessen, wenn Sie AdministratorLoginPassword, Sku usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="2e452-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="2e452-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e452-105">SYNTAX</span></span>

### <span data-ttu-id="2e452-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e452-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2e452-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2e452-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2e452-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e452-108">DESCRIPTION</span></span>
<span data-ttu-id="2e452-109">Aktualisiert eine Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="2e452-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="2e452-110">Verwenden Update-AzPostgreSqlServer sie stattdessen, wenn Sie AdministratorLoginPassword, Sku usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="2e452-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="2e452-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2e452-111">EXAMPLES</span></span>

### <span data-ttu-id="2e452-112">Beispiel 1: Aktualisieren der PostgreSql-Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="2e452-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="2e452-113">Dieses Cmdlet aktualisiert die PostgreSql-Konfiguration nach Name.</span><span class="sxs-lookup"><span data-stu-id="2e452-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="2e452-114">Beispiel 2: Aktualisieren der PostgreSql-Konfiguration nach Identität.</span><span class="sxs-lookup"><span data-stu-id="2e452-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="2e452-115">Diese Cmdlets aktualisieren die PostgreSql-Konfiguration nach Identität.</span><span class="sxs-lookup"><span data-stu-id="2e452-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="2e452-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2e452-116">PARAMETERS</span></span>

### <span data-ttu-id="2e452-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e452-117">-AsJob</span></span>
<span data-ttu-id="2e452-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2e452-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2e452-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e452-119">-DefaultProfile</span></span>
<span data-ttu-id="2e452-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e452-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e452-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e452-121">-InputObject</span></span>
<span data-ttu-id="2e452-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2e452-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2e452-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2e452-123">-Name</span></span>
<span data-ttu-id="2e452-124">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e452-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="2e452-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2e452-125">-NoWait</span></span>
<span data-ttu-id="2e452-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2e452-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2e452-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e452-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e452-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2e452-128">The name of the resource group.</span></span>
<span data-ttu-id="2e452-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2e452-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2e452-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="2e452-130">-ServerName</span></span>
<span data-ttu-id="2e452-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2e452-131">The name of the server.</span></span>

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

### <span data-ttu-id="2e452-132">-Source</span><span class="sxs-lookup"><span data-stu-id="2e452-132">-Source</span></span>
<span data-ttu-id="2e452-133">Quelle der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e452-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="2e452-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e452-134">-SubscriptionId</span></span>
<span data-ttu-id="2e452-135">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2e452-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2e452-136">-Wert</span><span class="sxs-lookup"><span data-stu-id="2e452-136">-Value</span></span>
<span data-ttu-id="2e452-137">Wert der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e452-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="2e452-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e452-138">-Confirm</span></span>
<span data-ttu-id="2e452-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e452-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e452-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e452-140">-WhatIf</span></span>
<span data-ttu-id="2e452-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e452-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e452-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e452-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e452-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e452-143">CommonParameters</span></span>
<span data-ttu-id="2e452-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e452-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e452-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e452-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e452-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2e452-146">INPUTS</span></span>

### <span data-ttu-id="2e452-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2e452-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="2e452-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2e452-148">OUTPUTS</span></span>

### <span data-ttu-id="2e452-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e452-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="2e452-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2e452-150">NOTES</span></span>

<span data-ttu-id="2e452-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2e452-151">ALIASES</span></span>

<span data-ttu-id="2e452-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2e452-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2e452-153">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2e452-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e452-154">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e452-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2e452-155">INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="2e452-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e452-156">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2e452-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2e452-157">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2e452-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2e452-158">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="2e452-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2e452-159">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2e452-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e452-160">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="2e452-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2e452-161">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2e452-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2e452-162">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2e452-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="2e452-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2e452-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2e452-164">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2e452-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2e452-165">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2e452-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2e452-166">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2e452-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2e452-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2e452-167">RELATED LINKS</span></span>

