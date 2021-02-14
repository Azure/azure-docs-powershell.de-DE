---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: 6168c557e3ae3a417f4c04195e6ef166ea3a01d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157257"
---
# <span data-ttu-id="8c210-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="8c210-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="8c210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c210-102">SYNOPSIS</span></span>
<span data-ttu-id="8c210-103">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="8c210-103">Updates an existing server.</span></span>
<span data-ttu-id="8c210-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8c210-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8c210-105">Verwenden Update-AzMySqlConfiguration sie stattdessen, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="8c210-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8c210-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c210-106">SYNTAX</span></span>

### <span data-ttu-id="8c210-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c210-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c210-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8c210-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8c210-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c210-109">DESCRIPTION</span></span>
<span data-ttu-id="8c210-110">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="8c210-110">Updates an existing server.</span></span>
<span data-ttu-id="8c210-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8c210-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="8c210-112">Verwenden Update-AzMySqlConfiguration sie stattdessen, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="8c210-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="8c210-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8c210-113">EXAMPLES</span></span>

### <span data-ttu-id="8c210-114">Beispiel 1: Aktualisieren des Server von MySql nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="8c210-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="8c210-115">Mit diesem Cmdlet wird der Server von MySql nach Ressourcengruppe und Servername aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8c210-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="8c210-116">Beispiel 2: Aktualisieren des Server "MySql" nach Identität.</span><span class="sxs-lookup"><span data-stu-id="8c210-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="8c210-117">Mit diesem Cmdlet wird der Server von MySql nach Identität aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8c210-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="8c210-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c210-118">PARAMETERS</span></span>

### <span data-ttu-id="8c210-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="8c210-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="8c210-120">Das Kennwort für die Administratoranmeldung.</span><span class="sxs-lookup"><span data-stu-id="8c210-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="8c210-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c210-121">-AsJob</span></span>
<span data-ttu-id="8c210-122">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="8c210-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="8c210-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="8c210-123">-BackupRetentionDay</span></span>
<span data-ttu-id="8c210-124">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="8c210-124">Backup retention days for the server.</span></span>
<span data-ttu-id="8c210-125">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="8c210-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="8c210-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c210-126">-DefaultProfile</span></span>
<span data-ttu-id="8c210-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c210-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c210-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c210-128">-InputObject</span></span>
<span data-ttu-id="8c210-129">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="8c210-129">Identity Parameter.</span></span>
<span data-ttu-id="8c210-130">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8c210-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8c210-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8c210-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="8c210-132">Legen Sie die minimale Version von TLS für Verbindungen mit dem Server bei aktiviertem SSL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8c210-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="8c210-133">Der Standardwert ist "TLSEnforcementDisabled.accepted": TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="8c210-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

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

### <span data-ttu-id="8c210-134">-Name</span><span class="sxs-lookup"><span data-stu-id="8c210-134">-Name</span></span>
<span data-ttu-id="8c210-135">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="8c210-135">The name of the server.</span></span>

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

### <span data-ttu-id="8c210-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8c210-136">-NoWait</span></span>
<span data-ttu-id="8c210-137">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="8c210-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8c210-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="8c210-138">-ReplicationRole</span></span>
<span data-ttu-id="8c210-139">Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="8c210-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="8c210-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c210-140">-ResourceGroupName</span></span>
<span data-ttu-id="8c210-141">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="8c210-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8c210-142">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="8c210-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8c210-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="8c210-143">-Sku</span></span>
<span data-ttu-id="8c210-144">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8c210-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="8c210-145">-Sku1</span><span class="sxs-lookup"><span data-stu-id="8c210-145">-SkuCapacity</span></span>
<span data-ttu-id="8c210-146">Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="8c210-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="8c210-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="8c210-147">-SkuFamily</span></span>
<span data-ttu-id="8c210-148">Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="8c210-148">The family of hardware.</span></span>

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

### <span data-ttu-id="8c210-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8c210-149">-SkuTier</span></span>
<span data-ttu-id="8c210-150">Die Stufe der jeweiligen SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="8c210-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="8c210-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="8c210-151">-SslEnforcement</span></span>
<span data-ttu-id="8c210-152">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="8c210-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="8c210-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="8c210-153">-StorageAutogrow</span></span>
<span data-ttu-id="8c210-154">Aktivieren Sie "Automatisches Anwachsen des Speichers".</span><span class="sxs-lookup"><span data-stu-id="8c210-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="8c210-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="8c210-155">-StorageInMb</span></span>
<span data-ttu-id="8c210-156">Für einen Server maximal zulässiger Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="8c210-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="8c210-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c210-157">-SubscriptionId</span></span>
<span data-ttu-id="8c210-158">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8c210-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8c210-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c210-159">-Tag</span></span>
<span data-ttu-id="8c210-160">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="8c210-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8c210-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c210-161">-Confirm</span></span>
<span data-ttu-id="8c210-162">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c210-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c210-163">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8c210-163">-WhatIf</span></span>
<span data-ttu-id="8c210-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c210-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c210-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c210-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c210-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c210-166">CommonParameters</span></span>
<span data-ttu-id="8c210-167">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c210-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c210-168">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c210-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c210-169">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8c210-169">INPUTS</span></span>

### <span data-ttu-id="8c210-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8c210-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8c210-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8c210-171">OUTPUTS</span></span>

### <span data-ttu-id="8c210-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="8c210-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8c210-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8c210-173">NOTES</span></span>

<span data-ttu-id="8c210-174">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8c210-174">ALIASES</span></span>

<span data-ttu-id="8c210-175">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="8c210-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8c210-176">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8c210-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c210-177">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8c210-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8c210-178">INPUTOBJECT <IMySqlIdentity> : Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="8c210-178">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="8c210-179">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="8c210-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8c210-180">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8c210-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8c210-181">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="8c210-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8c210-182">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="8c210-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c210-183">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="8c210-183">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="8c210-184">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="8c210-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8c210-185">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8c210-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8c210-186">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="8c210-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="8c210-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8c210-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8c210-188">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="8c210-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8c210-189">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="8c210-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8c210-190">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8c210-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8c210-191">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8c210-191">RELATED LINKS</span></span>

