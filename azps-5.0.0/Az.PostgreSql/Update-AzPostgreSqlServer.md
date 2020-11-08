---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: ecb568a356d0f1cf5ed36d966028e2d0ca4f813a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177763"
---
# <span data-ttu-id="4464d-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="4464d-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="4464d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4464d-102">SYNOPSIS</span></span>
<span data-ttu-id="4464d-103">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="4464d-103">Updates an existing server.</span></span>
<span data-ttu-id="4464d-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Server Definition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4464d-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="4464d-105">Verwenden Sie stattdessen Update-AzPostSqlConfiguration, wenn Sie Update Serverparameter wie wait_timeout oder net_retry_count verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4464d-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="4464d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4464d-106">SYNTAX</span></span>

### <span data-ttu-id="4464d-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="4464d-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4464d-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4464d-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4464d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4464d-109">DESCRIPTION</span></span>
<span data-ttu-id="4464d-110">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="4464d-110">Updates an existing server.</span></span>
<span data-ttu-id="4464d-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Server Definition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4464d-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="4464d-112">Verwenden Sie stattdessen Update-AzPostSqlConfiguration, wenn Sie Update Serverparameter wie wait_timeout oder net_retry_count verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4464d-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="4464d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4464d-113">EXAMPLES</span></span>

### <span data-ttu-id="4464d-114">Beispiel 1: Aktualisieren des PostgreSQL-Servers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="4464d-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="4464d-115">Dieses Cmdlet aktualisiert den PostgreSQL-Server nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="4464d-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="4464d-116">Beispiel 2: Aktualisieren des PostgreSQL-Servers nach Identität.</span><span class="sxs-lookup"><span data-stu-id="4464d-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="4464d-117">Dieses Cmdlet aktualisiert den PostgreSQL-Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="4464d-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="4464d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="4464d-118">PARAMETERS</span></span>

### <span data-ttu-id="4464d-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="4464d-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="4464d-120">Das Kennwort des Administrator Anmeldenamens.</span><span class="sxs-lookup"><span data-stu-id="4464d-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="4464d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4464d-121">-AsJob</span></span>
<span data-ttu-id="4464d-122">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="4464d-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="4464d-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="4464d-123">-BackupRetentionDay</span></span>
<span data-ttu-id="4464d-124">Aufbewahrungstage für Backups für den Server.</span><span class="sxs-lookup"><span data-stu-id="4464d-124">Backup retention days for the server.</span></span>
<span data-ttu-id="4464d-125">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="4464d-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="4464d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4464d-126">-DefaultProfile</span></span>
<span data-ttu-id="4464d-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4464d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4464d-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4464d-128">-InputObject</span></span>
<span data-ttu-id="4464d-129">Parameter Identity.</span><span class="sxs-lookup"><span data-stu-id="4464d-129">Identity Parameter.</span></span>
<span data-ttu-id="4464d-130">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4464d-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4464d-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4464d-131">-Name</span></span>
<span data-ttu-id="4464d-132">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="4464d-132">The name of the server.</span></span>

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

### <span data-ttu-id="4464d-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4464d-133">-NoWait</span></span>
<span data-ttu-id="4464d-134">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="4464d-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="4464d-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="4464d-135">-ReplicationRole</span></span>
<span data-ttu-id="4464d-136">Die Replikations Rolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="4464d-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="4464d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4464d-137">-ResourceGroupName</span></span>
<span data-ttu-id="4464d-138">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="4464d-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4464d-139">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="4464d-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4464d-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="4464d-140">-Sku</span></span>
<span data-ttu-id="4464d-141">Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="4464d-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="4464d-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4464d-142">-SkuCapacity</span></span>
<span data-ttu-id="4464d-143">Die Skalierungskapazität, die die Compute-Einheiten des Servers repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="4464d-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="4464d-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="4464d-144">-SkuFamily</span></span>
<span data-ttu-id="4464d-145">Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="4464d-145">The family of hardware.</span></span>

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

### <span data-ttu-id="4464d-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4464d-146">-SkuTier</span></span>
<span data-ttu-id="4464d-147">Die Stufe der jeweiligen SKU, z.b. Basic.</span><span class="sxs-lookup"><span data-stu-id="4464d-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="4464d-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="4464d-148">-SslEnforcement</span></span>
<span data-ttu-id="4464d-149">Aktivieren der SSL-Erzwingung oder nicht beim Herstellen einer Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="4464d-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="4464d-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="4464d-150">-StorageAutogrow</span></span>
<span data-ttu-id="4464d-151">Aktivieren der automatischen Vergrößerung von Speicher.</span><span class="sxs-lookup"><span data-stu-id="4464d-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="4464d-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="4464d-152">-StorageInMb</span></span>
<span data-ttu-id="4464d-153">Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="4464d-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="4464d-154">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4464d-154">-SubscriptionId</span></span>
<span data-ttu-id="4464d-155">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4464d-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="4464d-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="4464d-156">-Tag</span></span>
<span data-ttu-id="4464d-157">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="4464d-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="4464d-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4464d-158">-Confirm</span></span>
<span data-ttu-id="4464d-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4464d-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4464d-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4464d-160">-WhatIf</span></span>
<span data-ttu-id="4464d-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4464d-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4464d-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4464d-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4464d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4464d-163">CommonParameters</span></span>
<span data-ttu-id="4464d-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4464d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4464d-165">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4464d-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4464d-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4464d-166">INPUTS</span></span>

### <span data-ttu-id="4464d-167">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4464d-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="4464d-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4464d-168">OUTPUTS</span></span>

### <span data-ttu-id="4464d-169">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="4464d-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="4464d-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="4464d-170">NOTES</span></span>

<span data-ttu-id="4464d-171">Aliase</span><span class="sxs-lookup"><span data-stu-id="4464d-171">ALIASES</span></span>

<span data-ttu-id="4464d-172">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4464d-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4464d-173">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4464d-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4464d-174">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="4464d-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4464d-175">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="4464d-175">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="4464d-176">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4464d-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4464d-177">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="4464d-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4464d-178">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="4464d-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4464d-179">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="4464d-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4464d-180">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="4464d-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4464d-181">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4464d-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4464d-182">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="4464d-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="4464d-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4464d-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4464d-184">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="4464d-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4464d-185">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="4464d-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4464d-186">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="4464d-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4464d-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4464d-187">RELATED LINKS</span></span>

