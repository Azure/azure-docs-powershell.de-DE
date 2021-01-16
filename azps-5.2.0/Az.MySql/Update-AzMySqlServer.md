---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: b205f3d4eb9b1ebce360596714ea2524fb2e3be2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360196"
---
# <span data-ttu-id="81f01-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="81f01-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="81f01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81f01-102">SYNOPSIS</span></span>
<span data-ttu-id="81f01-103">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="81f01-103">Updates an existing server.</span></span>
<span data-ttu-id="81f01-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="81f01-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="81f01-105">Verwenden Update-AzMySqlConfiguration, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="81f01-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="81f01-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81f01-106">SYNTAX</span></span>

### <span data-ttu-id="81f01-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="81f01-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="81f01-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="81f01-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="81f01-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81f01-109">DESCRIPTION</span></span>
<span data-ttu-id="81f01-110">Aktualisiert einen vorhandenen Server.</span><span class="sxs-lookup"><span data-stu-id="81f01-110">Updates an existing server.</span></span>
<span data-ttu-id="81f01-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="81f01-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="81f01-112">Verwenden Update-AzMySqlConfiguration, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="81f01-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="81f01-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81f01-113">EXAMPLES</span></span>

### <span data-ttu-id="81f01-114">Beispiel 1: Aktualisieren des Server von MySql nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="81f01-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="81f01-115">Mit diesem Cmdlet wird der Server von MySql nach Ressourcengruppe und Servername aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="81f01-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="81f01-116">Beispiel 2: Aktualisieren des Server "MySql" nach Identität.</span><span class="sxs-lookup"><span data-stu-id="81f01-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="81f01-117">Mit diesem Cmdlet wird der Server von MySql nach Identität aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="81f01-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="81f01-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81f01-118">PARAMETERS</span></span>

### <span data-ttu-id="81f01-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="81f01-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="81f01-120">Das Kennwort für die Administratoranmeldung.</span><span class="sxs-lookup"><span data-stu-id="81f01-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="81f01-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81f01-121">-AsJob</span></span>
<span data-ttu-id="81f01-122">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="81f01-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="81f01-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="81f01-123">-BackupRetentionDay</span></span>
<span data-ttu-id="81f01-124">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="81f01-124">Backup retention days for the server.</span></span>
<span data-ttu-id="81f01-125">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="81f01-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="81f01-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f01-126">-DefaultProfile</span></span>
<span data-ttu-id="81f01-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81f01-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81f01-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81f01-128">-InputObject</span></span>
<span data-ttu-id="81f01-129">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="81f01-129">Identity Parameter.</span></span>
<span data-ttu-id="81f01-130">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="81f01-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="81f01-131">-Name</span><span class="sxs-lookup"><span data-stu-id="81f01-131">-Name</span></span>
<span data-ttu-id="81f01-132">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="81f01-132">The name of the server.</span></span>

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

### <span data-ttu-id="81f01-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="81f01-133">-NoWait</span></span>
<span data-ttu-id="81f01-134">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="81f01-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="81f01-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="81f01-135">-ReplicationRole</span></span>
<span data-ttu-id="81f01-136">Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="81f01-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="81f01-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81f01-137">-ResourceGroupName</span></span>
<span data-ttu-id="81f01-138">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="81f01-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="81f01-139">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="81f01-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="81f01-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="81f01-140">-Sku</span></span>
<span data-ttu-id="81f01-141">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="81f01-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="81f01-142">-Sku1</span><span class="sxs-lookup"><span data-stu-id="81f01-142">-SkuCapacity</span></span>
<span data-ttu-id="81f01-143">Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="81f01-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="81f01-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="81f01-144">-SkuFamily</span></span>
<span data-ttu-id="81f01-145">Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="81f01-145">The family of hardware.</span></span>

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

### <span data-ttu-id="81f01-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="81f01-146">-SkuTier</span></span>
<span data-ttu-id="81f01-147">Die Ebene der jeweiligen SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="81f01-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="81f01-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="81f01-148">-SslEnforcement</span></span>
<span data-ttu-id="81f01-149">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="81f01-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="81f01-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="81f01-150">-StorageAutogrow</span></span>
<span data-ttu-id="81f01-151">Aktivieren Sie "Automatisches Anwachsen des Speichers".</span><span class="sxs-lookup"><span data-stu-id="81f01-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="81f01-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="81f01-152">-StorageInMb</span></span>
<span data-ttu-id="81f01-153">Für einen Server maximal zulässiger Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="81f01-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="81f01-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81f01-154">-SubscriptionId</span></span>
<span data-ttu-id="81f01-155">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="81f01-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="81f01-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="81f01-156">-Tag</span></span>
<span data-ttu-id="81f01-157">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="81f01-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="81f01-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81f01-158">-Confirm</span></span>
<span data-ttu-id="81f01-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="81f01-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81f01-160">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="81f01-160">-WhatIf</span></span>
<span data-ttu-id="81f01-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81f01-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81f01-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81f01-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81f01-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f01-163">CommonParameters</span></span>
<span data-ttu-id="81f01-164">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f01-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f01-165">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81f01-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f01-166">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81f01-166">INPUTS</span></span>

### <span data-ttu-id="81f01-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="81f01-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="81f01-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81f01-168">OUTPUTS</span></span>

### <span data-ttu-id="81f01-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="81f01-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="81f01-170">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="81f01-170">NOTES</span></span>

<span data-ttu-id="81f01-171">ALIASE</span><span class="sxs-lookup"><span data-stu-id="81f01-171">ALIASES</span></span>

<span data-ttu-id="81f01-172">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="81f01-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81f01-173">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="81f01-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81f01-174">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="81f01-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81f01-175">INPUTOBJECT <IMySqlIdentity> : Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="81f01-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="81f01-176">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="81f01-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="81f01-177">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="81f01-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="81f01-178">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="81f01-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="81f01-179">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="81f01-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81f01-180">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="81f01-180">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="81f01-181">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="81f01-181">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="81f01-182">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81f01-182">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="81f01-183">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="81f01-183">The name is case insensitive.</span></span>
  - <span data-ttu-id="81f01-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="81f01-184">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="81f01-185">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="81f01-185">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="81f01-186">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="81f01-186">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="81f01-187">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="81f01-187">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="81f01-188">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="81f01-188">RELATED LINKS</span></span>

