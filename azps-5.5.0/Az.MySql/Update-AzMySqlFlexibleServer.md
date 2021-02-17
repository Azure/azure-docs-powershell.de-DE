---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3e1f79f431e5f0ff5c39c03a7f3c41a20c2543e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147260"
---
# <span data-ttu-id="407c9-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="407c9-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="407c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="407c9-102">SYNOPSIS</span></span>
<span data-ttu-id="407c9-103">Aktualisiert einen vorhandenen flexiblen MySQL-Server.</span><span class="sxs-lookup"><span data-stu-id="407c9-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="407c9-104">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="407c9-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="407c9-105">Verwenden Update-AzMySqlFlexibleServerConfiguration sie stattdessen, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="407c9-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="407c9-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="407c9-106">SYNTAX</span></span>

### <span data-ttu-id="407c9-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="407c9-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="407c9-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="407c9-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="407c9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="407c9-109">DESCRIPTION</span></span>
<span data-ttu-id="407c9-110">Aktualisiert einen vorhandenen flexiblen MySQL-Server.</span><span class="sxs-lookup"><span data-stu-id="407c9-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="407c9-111">Der Anforderungstext kann eine bis viele der Eigenschaften enthalten, die in der normalen Serverdefinition vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="407c9-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="407c9-112">Verwenden Update-AzMySqlFlexibleServerConfiguration sie stattdessen, wenn Sie Serverparameter wie Wait_timeout oder net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="407c9-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="407c9-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="407c9-113">EXAMPLES</span></span>

### <span data-ttu-id="407c9-114">Beispiel 1: Aktualisieren des Server von MySql nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="407c9-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="407c9-115">Mit diesem Cmdlet wird der Server von MySql nach Ressourcengruppe und Servername aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="407c9-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="407c9-116">Beispiel 2: Aktualisieren des Server "MySql" nach Identität.</span><span class="sxs-lookup"><span data-stu-id="407c9-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="407c9-117">Mit diesem Cmdlet wird der Server von MySql nach Identität aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="407c9-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="407c9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="407c9-118">PARAMETERS</span></span>

### <span data-ttu-id="407c9-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="407c9-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="407c9-120">Das Kennwort für die Administratoranmeldung.</span><span class="sxs-lookup"><span data-stu-id="407c9-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="407c9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="407c9-121">-AsJob</span></span>
<span data-ttu-id="407c9-122">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="407c9-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="407c9-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="407c9-123">-BackupRetentionDay</span></span>
<span data-ttu-id="407c9-124">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="407c9-124">Backup retention days for the server.</span></span>
<span data-ttu-id="407c9-125">Die Anzahl der Tage liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="407c9-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="407c9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="407c9-126">-DefaultProfile</span></span>
<span data-ttu-id="407c9-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="407c9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="407c9-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="407c9-128">-HaEnabled</span></span>
<span data-ttu-id="407c9-129">Aktivieren oder Deaktivieren des Hochverfügbarkeitsfeatures</span><span class="sxs-lookup"><span data-stu-id="407c9-129">Enable or disable high availability feature.</span></span>

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

### <span data-ttu-id="407c9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="407c9-130">-InputObject</span></span>
<span data-ttu-id="407c9-131">Identitätsparameter.</span><span class="sxs-lookup"><span data-stu-id="407c9-131">Identity Parameter.</span></span>
<span data-ttu-id="407c9-132">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="407c9-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="407c9-133">-Name</span><span class="sxs-lookup"><span data-stu-id="407c9-133">-Name</span></span>
<span data-ttu-id="407c9-134">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="407c9-134">The name of the server.</span></span>

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

### <span data-ttu-id="407c9-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="407c9-135">-NoWait</span></span>
<span data-ttu-id="407c9-136">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="407c9-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="407c9-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="407c9-137">-ReplicationRole</span></span>
<span data-ttu-id="407c9-138">Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="407c9-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="407c9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="407c9-139">-ResourceGroupName</span></span>
<span data-ttu-id="407c9-140">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="407c9-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="407c9-141">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="407c9-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="407c9-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="407c9-142">-Sku</span></span>
<span data-ttu-id="407c9-143">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="407c9-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="407c9-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="407c9-144">-SkuTier</span></span>
<span data-ttu-id="407c9-145">Die Stufe der jeweiligen SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="407c9-145">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="407c9-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="407c9-146">-SslEnforcement</span></span>
<span data-ttu-id="407c9-147">Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="407c9-147">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="407c9-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="407c9-148">-StorageAutogrow</span></span>
<span data-ttu-id="407c9-149">Aktivieren Sie "Automatisches Anwachsen des Speichers".</span><span class="sxs-lookup"><span data-stu-id="407c9-149">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="407c9-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="407c9-150">-StorageInMb</span></span>
<span data-ttu-id="407c9-151">Für einen Server maximal zulässiger Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="407c9-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="407c9-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="407c9-152">-SubscriptionId</span></span>
<span data-ttu-id="407c9-153">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="407c9-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="407c9-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="407c9-154">-Tag</span></span>
<span data-ttu-id="407c9-155">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="407c9-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="407c9-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="407c9-156">-Confirm</span></span>
<span data-ttu-id="407c9-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="407c9-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="407c9-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="407c9-158">-WhatIf</span></span>
<span data-ttu-id="407c9-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="407c9-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="407c9-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="407c9-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="407c9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="407c9-161">CommonParameters</span></span>
<span data-ttu-id="407c9-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="407c9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="407c9-163">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="407c9-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="407c9-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="407c9-164">INPUTS</span></span>

### <span data-ttu-id="407c9-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="407c9-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="407c9-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="407c9-166">OUTPUTS</span></span>

### <span data-ttu-id="407c9-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="407c9-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="407c9-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="407c9-168">NOTES</span></span>

<span data-ttu-id="407c9-169">ALIASE</span><span class="sxs-lookup"><span data-stu-id="407c9-169">ALIASES</span></span>

<span data-ttu-id="407c9-170">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="407c9-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="407c9-171">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="407c9-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="407c9-172">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="407c9-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="407c9-173">INPUTOBJECT <IMySqlIdentity> : Identity Parameter.</span><span class="sxs-lookup"><span data-stu-id="407c9-173">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="407c9-174">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="407c9-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="407c9-175">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="407c9-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="407c9-176">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="407c9-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="407c9-177">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="407c9-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="407c9-178">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="407c9-178">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="407c9-179">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="407c9-179">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="407c9-180">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="407c9-180">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="407c9-181">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="407c9-181">The name is case insensitive.</span></span>
  - <span data-ttu-id="407c9-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="407c9-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="407c9-183">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="407c9-183">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="407c9-184">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="407c9-184">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="407c9-185">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="407c9-185">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="407c9-186">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="407c9-186">RELATED LINKS</span></span>

