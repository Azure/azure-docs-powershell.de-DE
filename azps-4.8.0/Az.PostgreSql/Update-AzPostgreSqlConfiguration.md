---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165043"
---
# <span data-ttu-id="d2321-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2321-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="d2321-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2321-102">SYNOPSIS</span></span>
<span data-ttu-id="d2321-103">Aktualisiert eine Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="d2321-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="d2321-104">Verwenden Sie stattdessen Update-AzPostgreSqlServer, wenn Sie AdministratorLoginPassword, SKU usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d2321-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="d2321-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2321-105">SYNTAX</span></span>

### <span data-ttu-id="d2321-106">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2321-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2321-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d2321-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2321-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2321-108">DESCRIPTION</span></span>
<span data-ttu-id="d2321-109">Aktualisiert eine Konfiguration eines Servers.</span><span class="sxs-lookup"><span data-stu-id="d2321-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="d2321-110">Verwenden Sie stattdessen Update-AzPostgreSqlServer, wenn Sie AdministratorLoginPassword, SKU usw. aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d2321-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="d2321-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2321-111">EXAMPLES</span></span>

### <span data-ttu-id="d2321-112">Beispiel 1: Aktualisieren der PostgreSQL-Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="d2321-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="d2321-113">Dieses Cmdlet aktualisiert die PostgreSQL-Konfiguration mit dem Namen.</span><span class="sxs-lookup"><span data-stu-id="d2321-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="d2321-114">Beispiel 2: Aktualisieren der PostgreSQL-Konfiguration nach Identität.</span><span class="sxs-lookup"><span data-stu-id="d2321-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="d2321-115">Diese Cmdlets aktualisieren die PostgreSQL-Konfiguration nach Identität.</span><span class="sxs-lookup"><span data-stu-id="d2321-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="d2321-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2321-116">PARAMETERS</span></span>

### <span data-ttu-id="d2321-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2321-117">-AsJob</span></span>
<span data-ttu-id="d2321-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d2321-118">Run the command as a job</span></span>

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

### <span data-ttu-id="d2321-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2321-119">-DefaultProfile</span></span>
<span data-ttu-id="d2321-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2321-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2321-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d2321-121">-InputObject</span></span>
<span data-ttu-id="d2321-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d2321-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2321-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d2321-123">-Name</span></span>
<span data-ttu-id="d2321-124">Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2321-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="d2321-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d2321-125">-NoWait</span></span>
<span data-ttu-id="d2321-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d2321-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2321-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2321-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2321-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d2321-128">The name of the resource group.</span></span>
<span data-ttu-id="d2321-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d2321-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d2321-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="d2321-130">-ServerName</span></span>
<span data-ttu-id="d2321-131">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="d2321-131">The name of the server.</span></span>

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

### <span data-ttu-id="d2321-132">-Source</span><span class="sxs-lookup"><span data-stu-id="d2321-132">-Source</span></span>
<span data-ttu-id="d2321-133">Die Quelle der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2321-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="d2321-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d2321-134">-SubscriptionId</span></span>
<span data-ttu-id="d2321-135">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d2321-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d2321-136">-Wert</span><span class="sxs-lookup"><span data-stu-id="d2321-136">-Value</span></span>
<span data-ttu-id="d2321-137">Der Wert der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2321-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="d2321-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2321-138">-Confirm</span></span>
<span data-ttu-id="d2321-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2321-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2321-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2321-140">-WhatIf</span></span>
<span data-ttu-id="d2321-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2321-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2321-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2321-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2321-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2321-143">CommonParameters</span></span>
<span data-ttu-id="d2321-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2321-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2321-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2321-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2321-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2321-146">INPUTS</span></span>

### <span data-ttu-id="d2321-147">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d2321-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d2321-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2321-148">OUTPUTS</span></span>

### <span data-ttu-id="d2321-149">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2321-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="d2321-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2321-150">NOTES</span></span>

<span data-ttu-id="d2321-151">Aliase</span><span class="sxs-lookup"><span data-stu-id="d2321-151">ALIASES</span></span>

<span data-ttu-id="d2321-152">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2321-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2321-153">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2321-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2321-154">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d2321-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2321-155">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="d2321-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2321-156">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2321-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d2321-157">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d2321-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d2321-158">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="d2321-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d2321-159">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="d2321-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2321-160">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="d2321-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d2321-161">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d2321-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d2321-162">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d2321-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="d2321-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d2321-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d2321-164">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="d2321-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d2321-165">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d2321-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d2321-166">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d2321-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d2321-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2321-167">RELATED LINKS</span></span>

