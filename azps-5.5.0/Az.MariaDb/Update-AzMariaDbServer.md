---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161380"
---
# <span data-ttu-id="0a5e4-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="0a5e4-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="0a5e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5e4-103">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-103">Updates an existing server.</span></span>
<span data-ttu-id="0a5e4-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="0a5e4-105">Verwenden Update-AzMariaDbConfiguration sie stattdessen, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="0a5e4-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a5e4-106">SYNTAX</span></span>

### <span data-ttu-id="0a5e4-107">Servername (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a5e4-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0a5e4-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="0a5e4-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0a5e4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a5e4-109">DESCRIPTION</span></span>
<span data-ttu-id="0a5e4-110">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-110">Updates an existing server.</span></span>
<span data-ttu-id="0a5e4-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="0a5e4-112">Verwenden Update-AzMariaDbConfiguration sie stattdessen, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="0a5e4-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a5e4-113">EXAMPLES</span></span>

### <span data-ttu-id="0a5e4-114">Beispiel 1: Aktualisieren von MariaDB</span><span class="sxs-lookup"><span data-stu-id="0a5e4-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="0a5e4-115">Mit diesem Befehl wird eine MariaDB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="0a5e4-116">Beispiel 2: Aktualisieren von MariaDB</span><span class="sxs-lookup"><span data-stu-id="0a5e4-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="0a5e4-117">Mit diesem Befehl wird eine MariaDB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="0a5e4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a5e4-118">PARAMETERS</span></span>

### <span data-ttu-id="0a5e4-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="0a5e4-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="0a5e4-120">Das Kennwort für die Administratoranmeldung.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="0a5e4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a5e4-121">-AsJob</span></span>
<span data-ttu-id="0a5e4-122">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="0a5e4-122">Run the command as a job</span></span>

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

### <span data-ttu-id="0a5e4-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="0a5e4-123">-BackupRetentionDay</span></span>
<span data-ttu-id="0a5e4-124">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="0a5e4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5e4-125">-DefaultProfile</span></span>
<span data-ttu-id="0a5e4-126">region DefaultParameters Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a5e4-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="0a5e4-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="0a5e4-128">Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a5e4-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a5e4-129">-InputObject</span></span>
<span data-ttu-id="0a5e4-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a5e4-131">-Name</span><span class="sxs-lookup"><span data-stu-id="0a5e4-131">-Name</span></span>
<span data-ttu-id="0a5e4-132">MariaDB Servername</span><span class="sxs-lookup"><span data-stu-id="0a5e4-132">MariaDB server name</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a5e4-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0a5e4-133">-NoWait</span></span>
<span data-ttu-id="0a5e4-134">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="0a5e4-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0a5e4-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="0a5e4-135">-ReplicationRole</span></span>
<span data-ttu-id="0a5e4-136">Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="0a5e4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a5e4-137">-ResourceGroupName</span></span>
<span data-ttu-id="0a5e4-138">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-138">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a5e4-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="0a5e4-139">-Sku</span></span>
<span data-ttu-id="0a5e4-140">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="0a5e4-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="0a5e4-141">-SslEnforcement</span></span>
<span data-ttu-id="0a5e4-142">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a5e4-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="0a5e4-143">-StorageAutogrow</span></span>
<span data-ttu-id="0a5e4-144">Aktivieren Sie "Automatisches Anwachsen des Speichers".</span><span class="sxs-lookup"><span data-stu-id="0a5e4-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a5e4-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="0a5e4-145">-StorageInMb</span></span>
<span data-ttu-id="0a5e4-146">Für einen Server maximal zulässiger Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="0a5e4-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a5e4-147">-SubscriptionId</span></span>
<span data-ttu-id="0a5e4-148">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a5e4-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a5e4-149">-Tag</span></span>
<span data-ttu-id="0a5e4-150">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="0a5e4-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a5e4-151">-Confirm</span></span>
<span data-ttu-id="0a5e4-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a5e4-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0a5e4-153">-WhatIf</span></span>
<span data-ttu-id="0a5e4-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a5e4-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a5e4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5e4-156">CommonParameters</span></span>
<span data-ttu-id="0a5e4-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5e4-158">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a5e4-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5e4-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a5e4-159">INPUTS</span></span>

### <span data-ttu-id="0a5e4-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="0a5e4-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="0a5e4-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a5e4-161">OUTPUTS</span></span>

### <span data-ttu-id="0a5e4-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="0a5e4-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0a5e4-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0a5e4-163">NOTES</span></span>

<span data-ttu-id="0a5e4-164">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0a5e4-164">ALIASES</span></span>

<span data-ttu-id="0a5e4-165">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0a5e4-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a5e4-166">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a5e4-167">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a5e4-168">INPUTOBJECT <IMariaDbIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0a5e4-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a5e4-169">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0a5e4-170">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0a5e4-171">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0a5e4-172">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="0a5e4-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a5e4-173">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0a5e4-174">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0a5e4-175">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0a5e4-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0a5e4-177">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0a5e4-178">`[SubscriptionId <String>]`: Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="0a5e4-179">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0a5e4-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0a5e4-180">RELATED LINKS</span></span>

