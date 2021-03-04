---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: 46408fc5cd6f718f26c4f55eb7f8bab56891d8b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926992"
---
# <span data-ttu-id="a7624-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="a7624-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="a7624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7624-102">SYNOPSIS</span></span>
<span data-ttu-id="a7624-103">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="a7624-103">Updates an existing server.</span></span>
<span data-ttu-id="a7624-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a7624-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="a7624-105">Verwenden Update-AzMySqlConfiguration sie stattdessen, wenn Sie Serverparameter aktualisieren möchten, z. B. wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="a7624-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="a7624-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7624-106">SYNTAX</span></span>

### <span data-ttu-id="a7624-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7624-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a7624-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a7624-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a7624-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7624-109">DESCRIPTION</span></span>
<span data-ttu-id="a7624-110">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="a7624-110">Updates an existing server.</span></span>
<span data-ttu-id="a7624-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a7624-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="a7624-112">Verwenden Update-AzMySqlConfiguration sie stattdessen, wenn Sie Serverparameter aktualisieren möchten, z. B. wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="a7624-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="a7624-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7624-113">EXAMPLES</span></span>

### <span data-ttu-id="a7624-114">Beispiel 1: Aktualisieren des MySql-Servers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="a7624-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="a7624-115">Dieses Cmdlet aktualisiert den MySql-Server nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="a7624-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="a7624-116">Beispiel 2: Aktualisieren des MySql-Servers nach Identität.</span><span class="sxs-lookup"><span data-stu-id="a7624-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="a7624-117">Dieses Cmdlet aktualisiert den MySql-Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="a7624-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="a7624-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7624-118">PARAMETERS</span></span>

### <span data-ttu-id="a7624-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="a7624-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="a7624-120">Das Kennwort der Administratoranmeldung.</span><span class="sxs-lookup"><span data-stu-id="a7624-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="a7624-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7624-121">-AsJob</span></span>
<span data-ttu-id="a7624-122">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="a7624-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="a7624-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="a7624-123">-BackupRetentionDay</span></span>
<span data-ttu-id="a7624-124">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="a7624-124">Backup retention days for the server.</span></span>
<span data-ttu-id="a7624-125">Die Tagesanzahl liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="a7624-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="a7624-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7624-126">-DefaultProfile</span></span>
<span data-ttu-id="a7624-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7624-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7624-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7624-128">-InputObject</span></span>
<span data-ttu-id="a7624-129">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="a7624-129">Identity Parameter.</span></span>
<span data-ttu-id="a7624-130">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a7624-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7624-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a7624-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="a7624-132">Legen Sie die minimale TLS-Version für Verbindungen mit dem Server bei aktiviertem SSL ein.</span><span class="sxs-lookup"><span data-stu-id="a7624-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="a7624-133">Standardmäßig sind TLSEnforcementDisabled.accepted-Werte: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="a7624-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7624-134">-Name</span><span class="sxs-lookup"><span data-stu-id="a7624-134">-Name</span></span>
<span data-ttu-id="a7624-135">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a7624-135">The name of the server.</span></span>

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

### <span data-ttu-id="a7624-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a7624-136">-NoWait</span></span>
<span data-ttu-id="a7624-137">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="a7624-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a7624-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="a7624-138">-ReplicationRole</span></span>
<span data-ttu-id="a7624-139">Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="a7624-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="a7624-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7624-140">-ResourceGroupName</span></span>
<span data-ttu-id="a7624-141">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a7624-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a7624-142">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a7624-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a7624-143">-Sku</span><span class="sxs-lookup"><span data-stu-id="a7624-143">-Sku</span></span>
<span data-ttu-id="a7624-144">Der Name der Sku ist in der Regel Ebene + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="a7624-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="a7624-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a7624-145">-SkuCapacity</span></span>
<span data-ttu-id="a7624-146">Die skalierungs-/out-Kapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="a7624-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="a7624-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="a7624-147">-SkuFamily</span></span>
<span data-ttu-id="a7624-148">Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="a7624-148">The family of hardware.</span></span>

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

### <span data-ttu-id="a7624-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a7624-149">-SkuTier</span></span>
<span data-ttu-id="a7624-150">Die Ebene der bestimmten SKU, z. B. Basic.</span><span class="sxs-lookup"><span data-stu-id="a7624-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="a7624-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="a7624-151">-SslEnforcement</span></span>
<span data-ttu-id="a7624-152">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="a7624-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="a7624-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="a7624-153">-StorageAutogrow</span></span>
<span data-ttu-id="a7624-154">Aktivieren Sie "Automatisches Wachstum" für "Speicher".</span><span class="sxs-lookup"><span data-stu-id="a7624-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="a7624-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="a7624-155">-StorageInMb</span></span>
<span data-ttu-id="a7624-156">Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a7624-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="a7624-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7624-157">-SubscriptionId</span></span>
<span data-ttu-id="a7624-158">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a7624-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a7624-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7624-159">-Tag</span></span>
<span data-ttu-id="a7624-160">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="a7624-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="a7624-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7624-161">-Confirm</span></span>
<span data-ttu-id="a7624-162">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7624-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7624-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7624-163">-WhatIf</span></span>
<span data-ttu-id="a7624-164">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7624-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7624-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7624-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7624-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7624-166">CommonParameters</span></span>
<span data-ttu-id="a7624-167">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7624-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7624-168">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7624-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7624-169">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7624-169">INPUTS</span></span>

### <span data-ttu-id="a7624-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a7624-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a7624-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7624-171">OUTPUTS</span></span>

### <span data-ttu-id="a7624-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="a7624-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a7624-173">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7624-173">NOTES</span></span>

<span data-ttu-id="a7624-174">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a7624-174">ALIASES</span></span>

<span data-ttu-id="a7624-175">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a7624-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7624-176">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a7624-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7624-177">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7624-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7624-178">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="a7624-178">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="a7624-179">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a7624-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a7624-180">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a7624-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a7624-181">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="a7624-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a7624-182">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a7624-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7624-183">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="a7624-183">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a7624-184">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="a7624-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a7624-185">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7624-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a7624-186">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="a7624-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="a7624-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="a7624-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a7624-188">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="a7624-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a7624-189">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a7624-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a7624-190">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a7624-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a7624-191">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7624-191">RELATED LINKS</span></span>

