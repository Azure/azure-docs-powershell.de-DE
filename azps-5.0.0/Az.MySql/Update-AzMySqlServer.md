---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: e23cc8b942033805d8ed8cd122b19e6a59bf457c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177821"
---
# <span data-ttu-id="f2299-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="f2299-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="f2299-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2299-102">SYNOPSIS</span></span>
<span data-ttu-id="f2299-103">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="f2299-103">Updates an existing server.</span></span>
<span data-ttu-id="f2299-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Server Definition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f2299-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="f2299-105">Verwenden Sie stattdessen Update-AzMySqlConfiguration, wenn Sie Update Serverparameter wie wait_timeout oder net_retry_count verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f2299-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="f2299-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2299-106">SYNTAX</span></span>

### <span data-ttu-id="f2299-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2299-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2299-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f2299-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2299-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2299-109">DESCRIPTION</span></span>
<span data-ttu-id="f2299-110">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="f2299-110">Updates an existing server.</span></span>
<span data-ttu-id="f2299-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Server Definition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f2299-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="f2299-112">Verwenden Sie stattdessen Update-AzMySqlConfiguration, wenn Sie Update Serverparameter wie wait_timeout oder net_retry_count verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f2299-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="f2299-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2299-113">EXAMPLES</span></span>

### <span data-ttu-id="f2299-114">Beispiel 1: Aktualisieren von MySQL Server nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="f2299-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="f2299-115">Dieses Cmdlet aktualisiert MySQL Server nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="f2299-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="f2299-116">Beispiel 2: Aktualisieren von MySQL Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="f2299-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="f2299-117">Dieses Cmdlet aktualisiert MySQL Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="f2299-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="f2299-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2299-118">PARAMETERS</span></span>

### <span data-ttu-id="f2299-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f2299-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f2299-120">Das Kennwort des Administrator Anmeldenamens.</span><span class="sxs-lookup"><span data-stu-id="f2299-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="f2299-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2299-121">-AsJob</span></span>
<span data-ttu-id="f2299-122">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="f2299-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="f2299-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="f2299-123">-BackupRetentionDay</span></span>
<span data-ttu-id="f2299-124">Aufbewahrungstage für Backups für den Server.</span><span class="sxs-lookup"><span data-stu-id="f2299-124">Backup retention days for the server.</span></span>
<span data-ttu-id="f2299-125">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="f2299-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="f2299-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2299-126">-DefaultProfile</span></span>
<span data-ttu-id="f2299-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2299-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2299-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f2299-128">-InputObject</span></span>
<span data-ttu-id="f2299-129">Parameter Identity.</span><span class="sxs-lookup"><span data-stu-id="f2299-129">Identity Parameter.</span></span>
<span data-ttu-id="f2299-130">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f2299-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f2299-131">-Name</span><span class="sxs-lookup"><span data-stu-id="f2299-131">-Name</span></span>
<span data-ttu-id="f2299-132">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f2299-132">The name of the server.</span></span>

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

### <span data-ttu-id="f2299-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f2299-133">-NoWait</span></span>
<span data-ttu-id="f2299-134">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="f2299-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="f2299-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="f2299-135">-ReplicationRole</span></span>
<span data-ttu-id="f2299-136">Die Replikations Rolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="f2299-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="f2299-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2299-137">-ResourceGroupName</span></span>
<span data-ttu-id="f2299-138">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="f2299-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f2299-139">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="f2299-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f2299-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="f2299-140">-Sku</span></span>
<span data-ttu-id="f2299-141">Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="f2299-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="f2299-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f2299-142">-SkuCapacity</span></span>
<span data-ttu-id="f2299-143">Die Skalierungskapazität, die die Compute-Einheiten des Servers repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="f2299-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="f2299-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="f2299-144">-SkuFamily</span></span>
<span data-ttu-id="f2299-145">Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="f2299-145">The family of hardware.</span></span>

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

### <span data-ttu-id="f2299-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f2299-146">-SkuTier</span></span>
<span data-ttu-id="f2299-147">Die Stufe der jeweiligen SKU, z.b. Basic.</span><span class="sxs-lookup"><span data-stu-id="f2299-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="f2299-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="f2299-148">-SslEnforcement</span></span>
<span data-ttu-id="f2299-149">Aktivieren der SSL-Erzwingung oder nicht beim Herstellen einer Verbindung mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="f2299-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="f2299-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="f2299-150">-StorageAutogrow</span></span>
<span data-ttu-id="f2299-151">Aktivieren der automatischen Vergrößerung von Speicher.</span><span class="sxs-lookup"><span data-stu-id="f2299-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="f2299-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="f2299-152">-StorageInMb</span></span>
<span data-ttu-id="f2299-153">Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="f2299-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="f2299-154">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f2299-154">-SubscriptionId</span></span>
<span data-ttu-id="f2299-155">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f2299-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f2299-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2299-156">-Tag</span></span>
<span data-ttu-id="f2299-157">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="f2299-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="f2299-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2299-158">-Confirm</span></span>
<span data-ttu-id="f2299-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2299-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2299-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2299-160">-WhatIf</span></span>
<span data-ttu-id="f2299-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2299-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2299-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2299-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2299-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2299-163">CommonParameters</span></span>
<span data-ttu-id="f2299-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2299-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2299-165">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2299-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2299-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2299-166">INPUTS</span></span>

### <span data-ttu-id="f2299-167">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f2299-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f2299-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2299-168">OUTPUTS</span></span>

### <span data-ttu-id="f2299-169">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="f2299-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="f2299-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2299-170">NOTES</span></span>

<span data-ttu-id="f2299-171">Aliase</span><span class="sxs-lookup"><span data-stu-id="f2299-171">ALIASES</span></span>

<span data-ttu-id="f2299-172">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2299-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2299-173">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f2299-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2299-174">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f2299-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2299-175">Inputobject <IMySqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f2299-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="f2299-176">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f2299-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f2299-177">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f2299-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f2299-178">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="f2299-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f2299-179">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f2299-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2299-180">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="f2299-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f2299-181">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f2299-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f2299-182">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f2299-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="f2299-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="f2299-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f2299-184">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f2299-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f2299-185">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f2299-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f2299-186">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f2299-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f2299-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2299-187">RELATED LINKS</span></span>

