---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 7a53cefa9aca7e4ea679b31763c19e82d4d1e841
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467527"
---
# <span data-ttu-id="1578d-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="1578d-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="1578d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1578d-102">SYNOPSIS</span></span>
<span data-ttu-id="1578d-103">Wiederherstellen eines Servers aus einer vorhandenen Sicherung</span><span class="sxs-lookup"><span data-stu-id="1578d-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="1578d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1578d-104">SYNTAX</span></span>

### <span data-ttu-id="1578d-105">GeoRestore (Standard)</span><span class="sxs-lookup"><span data-stu-id="1578d-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1578d-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="1578d-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1578d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1578d-107">DESCRIPTION</span></span>
<span data-ttu-id="1578d-108">Wiederherstellen eines Servers aus einer vorhandenen Sicherung</span><span class="sxs-lookup"><span data-stu-id="1578d-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="1578d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1578d-109">EXAMPLES</span></span>

### <span data-ttu-id="1578d-110">Beispiel 1: Wiederherstellen eines MySql-Servers mithilfe von "GeoReplica Restore"</span><span class="sxs-lookup"><span data-stu-id="1578d-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="1578d-111">Mit diesem Cmdlet wird der Server von MySql mithilfe von GeoReplica Restore wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="1578d-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="1578d-112">Beispiel 2: Wiederherstellen des Server von MySql mithilfe der PointInTime-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="1578d-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="1578d-113">Diese Cmdlets stellen den Server von MySql mithilfe der PointInTime-Wiederherstellung wieder zur Wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="1578d-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="1578d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1578d-114">PARAMETERS</span></span>

### <span data-ttu-id="1578d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1578d-115">-AsJob</span></span>
<span data-ttu-id="1578d-116">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="1578d-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="1578d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1578d-117">-DefaultProfile</span></span>
<span data-ttu-id="1578d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1578d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1578d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1578d-119">-InputObject</span></span>
<span data-ttu-id="1578d-120">Das Quellserverobjekt, aus dem sie wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1578d-120">The source server object to restore from.</span></span>
<span data-ttu-id="1578d-121">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1578d-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1578d-122">-Location</span><span class="sxs-lookup"><span data-stu-id="1578d-122">-Location</span></span>
<span data-ttu-id="1578d-123">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="1578d-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="1578d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1578d-124">-Name</span></span>
<span data-ttu-id="1578d-125">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="1578d-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1578d-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1578d-126">-NoWait</span></span>
<span data-ttu-id="1578d-127">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="1578d-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="1578d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1578d-128">-ResourceGroupName</span></span>
<span data-ttu-id="1578d-129">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="1578d-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1578d-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="1578d-130">-RestorePointInTime</span></span>
<span data-ttu-id="1578d-131">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="1578d-131">The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1578d-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="1578d-132">-Sku</span></span>
<span data-ttu-id="1578d-133">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="1578d-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="1578d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1578d-134">-SubscriptionId</span></span>
<span data-ttu-id="1578d-135">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1578d-135">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1578d-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="1578d-136">-Tag</span></span>
<span data-ttu-id="1578d-137">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="1578d-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="1578d-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="1578d-138">-UseGeoRestore</span></span>
<span data-ttu-id="1578d-139">Verwenden des Geomodus zum Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="1578d-139">Use Geo mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1578d-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="1578d-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="1578d-141">Verwenden des PointInTime-Modus zum Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="1578d-141">Use PointInTime mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1578d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1578d-142">-Confirm</span></span>
<span data-ttu-id="1578d-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1578d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1578d-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1578d-144">-WhatIf</span></span>
<span data-ttu-id="1578d-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1578d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1578d-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1578d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1578d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1578d-147">CommonParameters</span></span>
<span data-ttu-id="1578d-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1578d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1578d-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1578d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1578d-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1578d-150">INPUTS</span></span>

### <span data-ttu-id="1578d-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="1578d-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="1578d-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1578d-152">OUTPUTS</span></span>

### <span data-ttu-id="1578d-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="1578d-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="1578d-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1578d-154">NOTES</span></span>

<span data-ttu-id="1578d-155">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1578d-155">ALIASES</span></span>

<span data-ttu-id="1578d-156">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1578d-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1578d-157">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1578d-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1578d-158">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1578d-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1578d-159">INPUTOBJECT <IServer> : Das Quellserverobjekt, aus dem Sie wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="1578d-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="1578d-160">`Location <String>`: Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="1578d-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="1578d-161">`SkuName <String>`: Der Name der SKU, in der Regel Stufe + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="1578d-161">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="1578d-162">`[Tag <ITrackedResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="1578d-162">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="1578d-163">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="1578d-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="1578d-164">`[AdministratorLogin <String>]`: Der Anmeldename eines Administrators für einen Server.</span><span class="sxs-lookup"><span data-stu-id="1578d-164">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="1578d-165">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="1578d-165">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="1578d-166">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="1578d-166">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="1578d-167">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="1578d-167">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="1578d-168">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="1578d-168">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="1578d-169">Legen Sie diesen Wert auf "SystemAssigned" ein, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="1578d-169">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="1578d-170">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob die Serverinfrastrukturverschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1578d-170">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="1578d-171">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="1578d-171">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="1578d-172">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingen Sie eine minimale Version von Tls für den Server.</span><span class="sxs-lookup"><span data-stu-id="1578d-172">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="1578d-173">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Gibt an, ob der Zugriff auf öffentliche Netzwerke für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="1578d-173">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="1578d-174">Der Wert ist optional, muss aber bei übergebenem Wert "Enabled" oder "Disabled" sein.</span><span class="sxs-lookup"><span data-stu-id="1578d-174">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="1578d-175">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="1578d-175">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="1578d-176">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="1578d-176">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="1578d-177">`[SkuCapacity <Int32?>]`: Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="1578d-177">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="1578d-178">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="1578d-178">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="1578d-179">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1578d-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="1578d-180">`[SkuTier <SkuTier?>]`: Die Ebene einer bestimmten SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="1578d-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="1578d-181">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="1578d-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="1578d-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="1578d-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="1578d-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="1578d-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="1578d-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Speicher automatisch anwachsen".</span><span class="sxs-lookup"><span data-stu-id="1578d-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="1578d-185">`[StorageProfileStorageMb <Int32?>]`: Maximal zulässiger Speicherplatz für einen Server.</span><span class="sxs-lookup"><span data-stu-id="1578d-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="1578d-186">`[UserVisibleState <ServerState?>]`: Der Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="1578d-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="1578d-187">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="1578d-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="1578d-188">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1578d-188">RELATED LINKS</span></span>

