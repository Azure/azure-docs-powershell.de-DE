---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: f6634f83e89abe4c775779c052ad9ee7b21bea6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151233"
---
# <span data-ttu-id="24351-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="24351-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="24351-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24351-102">SYNOPSIS</span></span>
<span data-ttu-id="24351-103">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="24351-103">Updates an existing server.</span></span>
<span data-ttu-id="24351-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="24351-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="24351-105">Verwenden Update-AzPostSqlFlexibleServerConfiguration sie stattdessen, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="24351-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="24351-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24351-106">SYNTAX</span></span>

### <span data-ttu-id="24351-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="24351-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="24351-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="24351-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24351-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24351-109">DESCRIPTION</span></span>
<span data-ttu-id="24351-110">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="24351-110">Updates an existing server.</span></span>
<span data-ttu-id="24351-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="24351-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="24351-112">Verwenden Update-AzPostgreSqlFlexibleServerConfiguration sie stattdessen, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="24351-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="24351-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="24351-113">EXAMPLES</span></span>

### <span data-ttu-id="24351-114">Beispiel 1: Aktualisieren des PostgreSqlservers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="24351-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="24351-115">Mit diesem Cmdlet wird der Server von PostgreSql nach Ressourcengruppe und Servername aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="24351-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="24351-116">Beispiel 2: Aktualisieren des PostgreSql-Servers nach Identität.</span><span class="sxs-lookup"><span data-stu-id="24351-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="24351-117">Dieses Cmdlet aktualisiert den PostgreSql Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="24351-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="24351-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24351-118">PARAMETERS</span></span>

### <span data-ttu-id="24351-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="24351-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="24351-120">Das Kennwort für die Administratoranmeldung.</span><span class="sxs-lookup"><span data-stu-id="24351-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24351-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24351-121">-AsJob</span></span>
<span data-ttu-id="24351-122">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="24351-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="24351-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="24351-123">-BackupRetentionDay</span></span>
<span data-ttu-id="24351-124">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="24351-124">Backup retention days for the server.</span></span>
<span data-ttu-id="24351-125">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="24351-125">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24351-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24351-126">-DefaultProfile</span></span>
<span data-ttu-id="24351-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24351-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24351-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="24351-128">-HaEnabled</span></span>
<span data-ttu-id="24351-129">Aktivieren oder Deaktivieren des Hochverfügbarkeitsfeatures</span><span class="sxs-lookup"><span data-stu-id="24351-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24351-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24351-130">-InputObject</span></span>
<span data-ttu-id="24351-131">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="24351-131">Identity Parameter.</span></span>
<span data-ttu-id="24351-132">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="24351-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="24351-133">-Name</span><span class="sxs-lookup"><span data-stu-id="24351-133">-Name</span></span>
<span data-ttu-id="24351-134">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="24351-134">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24351-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="24351-135">-NoWait</span></span>
<span data-ttu-id="24351-136">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="24351-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="24351-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="24351-137">-ReplicationRole</span></span>
<span data-ttu-id="24351-138">Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="24351-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="24351-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24351-139">-ResourceGroupName</span></span>
<span data-ttu-id="24351-140">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="24351-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="24351-141">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="24351-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="24351-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="24351-142">-Sku</span></span>
<span data-ttu-id="24351-143">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="24351-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="24351-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="24351-144">-SkuTier</span></span>
<span data-ttu-id="24351-145">Die Stufe der jeweiligen SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="24351-145">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24351-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="24351-146">-SslEnforcement</span></span>
<span data-ttu-id="24351-147">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="24351-147">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24351-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="24351-148">-StorageAutogrow</span></span>
<span data-ttu-id="24351-149">Aktivieren Sie "Automatisches Anwachsen des Speichers".</span><span class="sxs-lookup"><span data-stu-id="24351-149">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24351-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="24351-150">-StorageInMb</span></span>
<span data-ttu-id="24351-151">Für einen Server maximal zulässiger Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="24351-151">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24351-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24351-152">-SubscriptionId</span></span>
<span data-ttu-id="24351-153">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="24351-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="24351-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="24351-154">-Tag</span></span>
<span data-ttu-id="24351-155">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="24351-155">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24351-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24351-156">-Confirm</span></span>
<span data-ttu-id="24351-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24351-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24351-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="24351-158">-WhatIf</span></span>
<span data-ttu-id="24351-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24351-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24351-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24351-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24351-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24351-161">CommonParameters</span></span>
<span data-ttu-id="24351-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24351-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24351-163">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24351-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24351-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="24351-164">INPUTS</span></span>

### <span data-ttu-id="24351-165">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="24351-165">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="24351-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="24351-166">OUTPUTS</span></span>

### <span data-ttu-id="24351-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="24351-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="24351-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="24351-168">NOTES</span></span>

<span data-ttu-id="24351-169">ALIASE</span><span class="sxs-lookup"><span data-stu-id="24351-169">ALIASES</span></span>

<span data-ttu-id="24351-170">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="24351-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="24351-171">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="24351-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24351-172">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="24351-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="24351-173">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="24351-173">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="24351-174">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="24351-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="24351-175">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="24351-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="24351-176">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="24351-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="24351-177">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="24351-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24351-178">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="24351-178">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="24351-179">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="24351-179">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="24351-180">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="24351-180">The name is case insensitive.</span></span>
  - <span data-ttu-id="24351-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="24351-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="24351-182">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="24351-182">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="24351-183">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="24351-183">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="24351-184">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="24351-184">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="24351-185">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="24351-185">RELATED LINKS</span></span>

