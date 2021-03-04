---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3d6358d52663c71e06b8186d9123d24b0587d253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927011"
---
# <span data-ttu-id="5a46d-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="5a46d-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="5a46d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a46d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a46d-103">Aktualisiert einen vorhandenen flexiblen MySQL-Server.</span><span class="sxs-lookup"><span data-stu-id="5a46d-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="5a46d-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5a46d-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="5a46d-105">Verwenden Update-AzMySqlFlexibleServerConfiguration sie stattdessen, wenn Sie Serverparameter aktualisieren möchten, z. B. wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="5a46d-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="5a46d-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a46d-106">SYNTAX</span></span>

### <span data-ttu-id="5a46d-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a46d-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5a46d-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5a46d-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-MaintenanceWindow <String>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a46d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a46d-109">DESCRIPTION</span></span>
<span data-ttu-id="5a46d-110">Aktualisiert einen vorhandenen flexiblen MySQL-Server.</span><span class="sxs-lookup"><span data-stu-id="5a46d-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="5a46d-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5a46d-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="5a46d-112">Verwenden Update-AzMySqlFlexibleServerConfiguration sie stattdessen, wenn Sie Serverparameter aktualisieren möchten, z. B. wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="5a46d-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="5a46d-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a46d-113">EXAMPLES</span></span>

### <span data-ttu-id="5a46d-114">Beispiel 1: Aktualisieren des MySql-Servers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="5a46d-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="5a46d-115">Dieses Cmdlet aktualisiert den MySql-Server nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="5a46d-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="5a46d-116">Beispiel 2: Aktualisieren des MySql-Servers nach Identität.</span><span class="sxs-lookup"><span data-stu-id="5a46d-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="5a46d-117">Dieses Cmdlet aktualisiert den MySql-Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="5a46d-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="5a46d-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5a46d-118">PARAMETERS</span></span>

### <span data-ttu-id="5a46d-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="5a46d-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="5a46d-120">Das Kennwort der Administratoranmeldung.</span><span class="sxs-lookup"><span data-stu-id="5a46d-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="5a46d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a46d-121">-AsJob</span></span>
<span data-ttu-id="5a46d-122">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="5a46d-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="5a46d-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="5a46d-123">-BackupRetentionDay</span></span>
<span data-ttu-id="5a46d-124">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="5a46d-124">Backup retention days for the server.</span></span>
<span data-ttu-id="5a46d-125">Die Tagesanzahl liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="5a46d-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="5a46d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a46d-126">-DefaultProfile</span></span>
<span data-ttu-id="5a46d-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a46d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a46d-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="5a46d-128">-HaEnabled</span></span>
<span data-ttu-id="5a46d-129">Aktivieren oder Deaktivieren des Features für hohe Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="5a46d-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a46d-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a46d-130">-InputObject</span></span>
<span data-ttu-id="5a46d-131">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="5a46d-131">Identity Parameter.</span></span>
<span data-ttu-id="5a46d-132">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5a46d-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a46d-133">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="5a46d-133">-MaintenanceWindow</span></span>
<span data-ttu-id="5a46d-134">Zeitraum (UTC), der zur Wartung bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="5a46d-134">Period of time (UTC) designated for maintenance.</span></span>
<span data-ttu-id="5a46d-135">Beispiele: "So:23:30" zum Planen am Sonntag, 23:30 UTC.</span><span class="sxs-lookup"><span data-stu-id="5a46d-135">Examples: "Sun:23:30" to schedule on Sunday, 11:30pm UTC.</span></span>
<span data-ttu-id="5a46d-136">So stellen Sie in "Disabled" die Standardübereinzugseinstellung zurück</span><span class="sxs-lookup"><span data-stu-id="5a46d-136">To set back to default pass in "Disabled"</span></span>

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

### <span data-ttu-id="5a46d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="5a46d-137">-Name</span></span>
<span data-ttu-id="5a46d-138">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5a46d-138">The name of the server.</span></span>

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

### <span data-ttu-id="5a46d-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5a46d-139">-NoWait</span></span>
<span data-ttu-id="5a46d-140">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="5a46d-140">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="5a46d-141">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="5a46d-141">-ReplicationRole</span></span>
<span data-ttu-id="5a46d-142">Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="5a46d-142">The replication role of the server.</span></span>

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

### <span data-ttu-id="5a46d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a46d-143">-ResourceGroupName</span></span>
<span data-ttu-id="5a46d-144">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="5a46d-144">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5a46d-145">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="5a46d-145">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5a46d-146">-Sku</span><span class="sxs-lookup"><span data-stu-id="5a46d-146">-Sku</span></span>
<span data-ttu-id="5a46d-147">Der Name der Sku , in der Regel , Ebene + Familie + Kerne, z. B. Burstable_B1ms, Standard_D2ds_v4</span><span class="sxs-lookup"><span data-stu-id="5a46d-147">The name of the sku, typically, tier + family + cores, e.g. Burstable_B1ms, Standard_D2ds_v4</span></span>

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

### <span data-ttu-id="5a46d-148">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5a46d-148">-SkuTier</span></span>
<span data-ttu-id="5a46d-149">Die Ebene der bestimmten SKU.</span><span class="sxs-lookup"><span data-stu-id="5a46d-149">The tier of the particular SKU.</span></span>
<span data-ttu-id="5a46d-150">Akzeptierte Werte: Burstable, GeneralPurpose, Memory Optimized.</span><span class="sxs-lookup"><span data-stu-id="5a46d-150">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="5a46d-151">Standard: Burstable.</span><span class="sxs-lookup"><span data-stu-id="5a46d-151">Default: Burstable.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a46d-152">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="5a46d-152">-SslEnforcement</span></span>
<span data-ttu-id="5a46d-153">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="5a46d-153">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a46d-154">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="5a46d-154">-StorageAutogrow</span></span>
<span data-ttu-id="5a46d-155">Aktivieren Sie "Automatisches Wachstum" für "Speicher".</span><span class="sxs-lookup"><span data-stu-id="5a46d-155">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a46d-156">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="5a46d-156">-StorageInMb</span></span>
<span data-ttu-id="5a46d-157">Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="5a46d-157">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="5a46d-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a46d-158">-SubscriptionId</span></span>
<span data-ttu-id="5a46d-159">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5a46d-159">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5a46d-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a46d-160">-Tag</span></span>
<span data-ttu-id="5a46d-161">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="5a46d-161">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="5a46d-162">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a46d-162">-Confirm</span></span>
<span data-ttu-id="5a46d-163">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a46d-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a46d-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a46d-164">-WhatIf</span></span>
<span data-ttu-id="5a46d-165">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a46d-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a46d-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a46d-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a46d-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a46d-167">CommonParameters</span></span>
<span data-ttu-id="5a46d-168">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a46d-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a46d-169">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a46d-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a46d-170">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a46d-170">INPUTS</span></span>

### <span data-ttu-id="5a46d-171">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5a46d-171">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="5a46d-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a46d-172">OUTPUTS</span></span>

### <span data-ttu-id="5a46d-173">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="5a46d-173">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="5a46d-174">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5a46d-174">NOTES</span></span>

<span data-ttu-id="5a46d-175">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5a46d-175">ALIASES</span></span>

<span data-ttu-id="5a46d-176">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="5a46d-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5a46d-177">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="5a46d-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a46d-178">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5a46d-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5a46d-179">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="5a46d-179">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="5a46d-180">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="5a46d-180">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5a46d-181">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5a46d-181">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5a46d-182">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="5a46d-182">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5a46d-183">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="5a46d-183">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5a46d-184">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="5a46d-184">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="5a46d-185">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="5a46d-185">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5a46d-186">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5a46d-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5a46d-187">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="5a46d-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="5a46d-188">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="5a46d-188">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5a46d-189">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5a46d-189">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5a46d-190">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5a46d-190">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5a46d-191">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="5a46d-191">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5a46d-192">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5a46d-192">RELATED LINKS</span></span>

