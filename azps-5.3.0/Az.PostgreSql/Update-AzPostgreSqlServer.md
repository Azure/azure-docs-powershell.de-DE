---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: ecb568a356d0f1cf5ed36d966028e2d0ca4f813a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468712"
---
# <span data-ttu-id="3b210-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="3b210-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="3b210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b210-102">SYNOPSIS</span></span>
<span data-ttu-id="3b210-103">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="3b210-103">Updates an existing server.</span></span>
<span data-ttu-id="3b210-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3b210-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="3b210-105">Verwenden Update-AzPostSqlConfiguration, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="3b210-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="3b210-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b210-106">SYNTAX</span></span>

### <span data-ttu-id="3b210-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b210-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3b210-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3b210-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3b210-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b210-109">DESCRIPTION</span></span>
<span data-ttu-id="3b210-110">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="3b210-110">Updates an existing server.</span></span>
<span data-ttu-id="3b210-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3b210-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="3b210-112">Verwenden Update-AzPostSqlConfiguration, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="3b210-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="3b210-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b210-113">EXAMPLES</span></span>

### <span data-ttu-id="3b210-114">Beispiel 1: Aktualisieren des PostgreSqlservers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="3b210-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="3b210-115">Mit diesem Cmdlet wird der Server von PostgreSql nach Ressourcengruppe und Servername aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3b210-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="3b210-116">Beispiel 2: Aktualisieren des PostgreSql-Servers nach Identität.</span><span class="sxs-lookup"><span data-stu-id="3b210-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="3b210-117">Dieses Cmdlet aktualisiert den PostgreSql Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="3b210-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="3b210-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b210-118">PARAMETERS</span></span>

### <span data-ttu-id="3b210-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3b210-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3b210-120">Das Kennwort für die Administratoranmeldung.</span><span class="sxs-lookup"><span data-stu-id="3b210-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="3b210-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b210-121">-AsJob</span></span>
<span data-ttu-id="3b210-122">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="3b210-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="3b210-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="3b210-123">-BackupRetentionDay</span></span>
<span data-ttu-id="3b210-124">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="3b210-124">Backup retention days for the server.</span></span>
<span data-ttu-id="3b210-125">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="3b210-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="3b210-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b210-126">-DefaultProfile</span></span>
<span data-ttu-id="3b210-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b210-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b210-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b210-128">-InputObject</span></span>
<span data-ttu-id="3b210-129">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="3b210-129">Identity Parameter.</span></span>
<span data-ttu-id="3b210-130">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3b210-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3b210-131">-Name</span><span class="sxs-lookup"><span data-stu-id="3b210-131">-Name</span></span>
<span data-ttu-id="3b210-132">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3b210-132">The name of the server.</span></span>

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

### <span data-ttu-id="3b210-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3b210-133">-NoWait</span></span>
<span data-ttu-id="3b210-134">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="3b210-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="3b210-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="3b210-135">-ReplicationRole</span></span>
<span data-ttu-id="3b210-136">Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="3b210-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="3b210-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b210-137">-ResourceGroupName</span></span>
<span data-ttu-id="3b210-138">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="3b210-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3b210-139">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="3b210-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3b210-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="3b210-140">-Sku</span></span>
<span data-ttu-id="3b210-141">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="3b210-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="3b210-142">-Sku1</span><span class="sxs-lookup"><span data-stu-id="3b210-142">-SkuCapacity</span></span>
<span data-ttu-id="3b210-143">Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b210-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="3b210-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="3b210-144">-SkuFamily</span></span>
<span data-ttu-id="3b210-145">Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="3b210-145">The family of hardware.</span></span>

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

### <span data-ttu-id="3b210-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3b210-146">-SkuTier</span></span>
<span data-ttu-id="3b210-147">Die Stufe der jeweiligen SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="3b210-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="3b210-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="3b210-148">-SslEnforcement</span></span>
<span data-ttu-id="3b210-149">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="3b210-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="3b210-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="3b210-150">-StorageAutogrow</span></span>
<span data-ttu-id="3b210-151">Aktivieren Sie "Automatisches Anwachsen des Speichers".</span><span class="sxs-lookup"><span data-stu-id="3b210-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="3b210-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="3b210-152">-StorageInMb</span></span>
<span data-ttu-id="3b210-153">Für einen Server maximal zulässiger Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="3b210-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="3b210-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b210-154">-SubscriptionId</span></span>
<span data-ttu-id="3b210-155">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3b210-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3b210-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b210-156">-Tag</span></span>
<span data-ttu-id="3b210-157">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="3b210-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="3b210-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b210-158">-Confirm</span></span>
<span data-ttu-id="3b210-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b210-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b210-160">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3b210-160">-WhatIf</span></span>
<span data-ttu-id="3b210-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b210-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b210-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b210-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b210-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b210-163">CommonParameters</span></span>
<span data-ttu-id="3b210-164">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b210-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b210-165">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b210-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b210-166">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b210-166">INPUTS</span></span>

### <span data-ttu-id="3b210-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3b210-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="3b210-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b210-168">OUTPUTS</span></span>

### <span data-ttu-id="3b210-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="3b210-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="3b210-170">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3b210-170">NOTES</span></span>

<span data-ttu-id="3b210-171">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3b210-171">ALIASES</span></span>

<span data-ttu-id="3b210-172">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="3b210-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b210-173">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3b210-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b210-174">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b210-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b210-175">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="3b210-175">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="3b210-176">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="3b210-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3b210-177">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3b210-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3b210-178">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="3b210-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3b210-179">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="3b210-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b210-180">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="3b210-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3b210-181">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b210-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3b210-182">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="3b210-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="3b210-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="3b210-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3b210-184">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3b210-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3b210-185">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3b210-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3b210-186">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3b210-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3b210-187">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3b210-187">RELATED LINKS</span></span>

