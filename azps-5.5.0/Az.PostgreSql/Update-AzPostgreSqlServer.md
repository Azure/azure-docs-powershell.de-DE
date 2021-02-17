---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: 4b0d2f01336de83acbd904e08b0d0cbc62c0aca6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169409"
---
# <span data-ttu-id="5da0c-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="5da0c-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="5da0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5da0c-102">SYNOPSIS</span></span>
<span data-ttu-id="5da0c-103">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="5da0c-103">Updates an existing server.</span></span>
<span data-ttu-id="5da0c-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5da0c-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="5da0c-105">Verwenden Update-AzPostSqlConfiguration sie stattdessen, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="5da0c-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="5da0c-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5da0c-106">SYNTAX</span></span>

### <span data-ttu-id="5da0c-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5da0c-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5da0c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5da0c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5da0c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5da0c-109">DESCRIPTION</span></span>
<span data-ttu-id="5da0c-110">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="5da0c-110">Updates an existing server.</span></span>
<span data-ttu-id="5da0c-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5da0c-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="5da0c-112">Verwenden Update-AzPostSqlConfiguration, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="5da0c-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="5da0c-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5da0c-113">EXAMPLES</span></span>

### <span data-ttu-id="5da0c-114">Beispiel 1: Aktualisieren des PostgreSqlservers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="5da0c-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="5da0c-115">Mit diesem Cmdlet wird der Server von PostgreSql nach Ressourcengruppe und Servername aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5da0c-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="5da0c-116">Beispiel 2: Aktualisieren des PostgreSql-Servers nach Identität.</span><span class="sxs-lookup"><span data-stu-id="5da0c-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="5da0c-117">Dieses Cmdlet aktualisiert den PostgreSql Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="5da0c-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="5da0c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5da0c-118">PARAMETERS</span></span>

### <span data-ttu-id="5da0c-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="5da0c-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="5da0c-120">Das Kennwort für die Administratoranmeldung.</span><span class="sxs-lookup"><span data-stu-id="5da0c-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="5da0c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5da0c-121">-AsJob</span></span>
<span data-ttu-id="5da0c-122">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="5da0c-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="5da0c-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="5da0c-123">-BackupRetentionDay</span></span>
<span data-ttu-id="5da0c-124">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="5da0c-124">Backup retention days for the server.</span></span>
<span data-ttu-id="5da0c-125">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="5da0c-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="5da0c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da0c-126">-DefaultProfile</span></span>
<span data-ttu-id="5da0c-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5da0c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5da0c-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5da0c-128">-InputObject</span></span>
<span data-ttu-id="5da0c-129">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="5da0c-129">Identity Parameter.</span></span>
<span data-ttu-id="5da0c-130">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5da0c-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5da0c-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="5da0c-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="5da0c-132">Legen Sie die minimale Version von TLS für Verbindungen mit dem Server bei aktiviertem SSL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5da0c-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="5da0c-133">Der Standardwert ist "TLSEnforcementDisabled.accepted": TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="5da0c-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da0c-134">-Name</span><span class="sxs-lookup"><span data-stu-id="5da0c-134">-Name</span></span>
<span data-ttu-id="5da0c-135">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5da0c-135">The name of the server.</span></span>

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

### <span data-ttu-id="5da0c-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5da0c-136">-NoWait</span></span>
<span data-ttu-id="5da0c-137">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="5da0c-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="5da0c-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="5da0c-138">-ReplicationRole</span></span>
<span data-ttu-id="5da0c-139">Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="5da0c-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="5da0c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da0c-140">-ResourceGroupName</span></span>
<span data-ttu-id="5da0c-141">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="5da0c-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5da0c-142">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="5da0c-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5da0c-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="5da0c-143">-Sku</span></span>
<span data-ttu-id="5da0c-144">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="5da0c-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="5da0c-145">-Sku1</span><span class="sxs-lookup"><span data-stu-id="5da0c-145">-SkuCapacity</span></span>
<span data-ttu-id="5da0c-146">Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="5da0c-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="5da0c-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="5da0c-147">-SkuFamily</span></span>
<span data-ttu-id="5da0c-148">Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="5da0c-148">The family of hardware.</span></span>

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

### <span data-ttu-id="5da0c-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5da0c-149">-SkuTier</span></span>
<span data-ttu-id="5da0c-150">Die Stufe der jeweiligen SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="5da0c-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="5da0c-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="5da0c-151">-SslEnforcement</span></span>
<span data-ttu-id="5da0c-152">Aktivieren Sie die Ssl-Erzwingung, oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="5da0c-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="5da0c-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="5da0c-153">-StorageAutogrow</span></span>
<span data-ttu-id="5da0c-154">Aktivieren Sie "Automatisches Anwachsen des Speichers".</span><span class="sxs-lookup"><span data-stu-id="5da0c-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="5da0c-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="5da0c-155">-StorageInMb</span></span>
<span data-ttu-id="5da0c-156">Für einen Server maximal zulässiger Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="5da0c-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="5da0c-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5da0c-157">-SubscriptionId</span></span>
<span data-ttu-id="5da0c-158">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5da0c-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5da0c-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="5da0c-159">-Tag</span></span>
<span data-ttu-id="5da0c-160">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="5da0c-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="5da0c-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5da0c-161">-Confirm</span></span>
<span data-ttu-id="5da0c-162">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5da0c-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5da0c-163">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5da0c-163">-WhatIf</span></span>
<span data-ttu-id="5da0c-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5da0c-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5da0c-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5da0c-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5da0c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da0c-166">CommonParameters</span></span>
<span data-ttu-id="5da0c-167">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da0c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da0c-168">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5da0c-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da0c-169">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5da0c-169">INPUTS</span></span>

### <span data-ttu-id="5da0c-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5da0c-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="5da0c-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5da0c-171">OUTPUTS</span></span>

### <span data-ttu-id="5da0c-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="5da0c-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="5da0c-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5da0c-173">NOTES</span></span>

<span data-ttu-id="5da0c-174">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5da0c-174">ALIASES</span></span>

<span data-ttu-id="5da0c-175">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="5da0c-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5da0c-176">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5da0c-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5da0c-177">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5da0c-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5da0c-178">INPUTOBJECT <IPostgreSqlIdentity> : Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="5da0c-178">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="5da0c-179">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="5da0c-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5da0c-180">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5da0c-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5da0c-181">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="5da0c-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5da0c-182">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="5da0c-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5da0c-183">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="5da0c-183">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5da0c-184">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5da0c-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5da0c-185">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="5da0c-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="5da0c-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="5da0c-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5da0c-187">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5da0c-187">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5da0c-188">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5da0c-188">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5da0c-189">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="5da0c-189">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5da0c-190">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5da0c-190">RELATED LINKS</span></span>

