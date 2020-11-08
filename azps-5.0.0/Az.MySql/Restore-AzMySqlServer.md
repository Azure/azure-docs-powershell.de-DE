---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 49ae121273b42d3718d1a334edcaa72fa2c57583
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176783"
---
# <span data-ttu-id="2161d-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="2161d-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="2161d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2161d-102">SYNOPSIS</span></span>
<span data-ttu-id="2161d-103">Wiederherstellen eines Servers aus einer vorhandenen Sicherung</span><span class="sxs-lookup"><span data-stu-id="2161d-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="2161d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2161d-104">SYNTAX</span></span>

### <span data-ttu-id="2161d-105">Georestore (Standard)</span><span class="sxs-lookup"><span data-stu-id="2161d-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2161d-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="2161d-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2161d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2161d-107">DESCRIPTION</span></span>
<span data-ttu-id="2161d-108">Wiederherstellen eines Servers aus einer vorhandenen Sicherung</span><span class="sxs-lookup"><span data-stu-id="2161d-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="2161d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2161d-109">EXAMPLES</span></span>

### <span data-ttu-id="2161d-110">Beispiel 1: Wiederherstellen des MySQL-Servers mithilfe der georeplica-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="2161d-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="2161d-111">Dieses Cmdlet stellt den MySQL-Server mithilfe der georeplikat-Wiederherstellung wieder her.</span><span class="sxs-lookup"><span data-stu-id="2161d-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="2161d-112">Beispiel 2: Wiederherstellen des MySQL-Servers mithilfe der PointInTime-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="2161d-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="2161d-113">Diese Cmdlets stellen den MySQL-Server mithilfe der PointInTime-Wiederherstellung wieder her.</span><span class="sxs-lookup"><span data-stu-id="2161d-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="2161d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2161d-114">PARAMETERS</span></span>

### <span data-ttu-id="2161d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2161d-115">-AsJob</span></span>
<span data-ttu-id="2161d-116">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="2161d-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="2161d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2161d-117">-DefaultProfile</span></span>
<span data-ttu-id="2161d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2161d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2161d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2161d-119">-InputObject</span></span>
<span data-ttu-id="2161d-120">Das Quellserver Objekt, von dem wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2161d-120">The source server object to restore from.</span></span>
<span data-ttu-id="2161d-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2161d-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2161d-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="2161d-122">-Location</span></span>
<span data-ttu-id="2161d-123">Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="2161d-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="2161d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2161d-124">-Name</span></span>
<span data-ttu-id="2161d-125">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="2161d-125">The name of the server.</span></span>

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

### <span data-ttu-id="2161d-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2161d-126">-NoWait</span></span>
<span data-ttu-id="2161d-127">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="2161d-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="2161d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2161d-128">-ResourceGroupName</span></span>
<span data-ttu-id="2161d-129">Der Name der Ressourcengruppe, die die Ressource enthält, Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="2161d-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2161d-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="2161d-130">-RestorePointInTime</span></span>
<span data-ttu-id="2161d-131">Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="2161d-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="2161d-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="2161d-132">-Sku</span></span>
<span data-ttu-id="2161d-133">Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="2161d-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="2161d-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2161d-134">-SubscriptionId</span></span>
<span data-ttu-id="2161d-135">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2161d-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="2161d-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="2161d-136">-Tag</span></span>
<span data-ttu-id="2161d-137">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="2161d-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="2161d-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="2161d-138">-UseGeoRestore</span></span>
<span data-ttu-id="2161d-139">Verwenden des Geo-Modus zum Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="2161d-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="2161d-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="2161d-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="2161d-141">Verwenden des PointInTime-Modus zum Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="2161d-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="2161d-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2161d-142">-Confirm</span></span>
<span data-ttu-id="2161d-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2161d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2161d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2161d-144">-WhatIf</span></span>
<span data-ttu-id="2161d-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2161d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2161d-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2161d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2161d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2161d-147">CommonParameters</span></span>
<span data-ttu-id="2161d-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2161d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2161d-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2161d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2161d-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2161d-150">INPUTS</span></span>

### <span data-ttu-id="2161d-151">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="2161d-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="2161d-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2161d-152">OUTPUTS</span></span>

### <span data-ttu-id="2161d-153">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="2161d-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="2161d-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="2161d-154">NOTES</span></span>

<span data-ttu-id="2161d-155">Aliase</span><span class="sxs-lookup"><span data-stu-id="2161d-155">ALIASES</span></span>

<span data-ttu-id="2161d-156">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2161d-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2161d-157">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2161d-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2161d-158">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2161d-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2161d-159">Inputobject <IServer> : das Quellserver Objekt, von dem wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2161d-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="2161d-160">`Location <String>`: Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="2161d-160">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="2161d-161">`[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="2161d-161">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="2161d-162">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2161d-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2161d-163">`[AdministratorLogin <String>]`: Der Anmeldename des Administrators auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="2161d-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="2161d-164">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="2161d-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="2161d-165">`[EarliestRestoreDate <DateTime?>]`: Frühester Erstellungszeitpunkt des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="2161d-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="2161d-166">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="2161d-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="2161d-167">`[IdentityType <IdentityType?>]`: Der Identity-Typ.</span><span class="sxs-lookup"><span data-stu-id="2161d-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="2161d-168">Legen Sie diesen Wert auf "SystemAssigned", um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="2161d-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="2161d-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob die Server-Infrastruktur Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2161d-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="2161d-170">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="2161d-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="2161d-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingen Sie eine minimale TLS-Version für den Server.</span><span class="sxs-lookup"><span data-stu-id="2161d-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="2161d-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Ob öffentlicher Netzwerkzugriff für diesen Server zulässig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="2161d-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="2161d-173">Der Wert ist optional, muss aber bei der Übergabe "aktiviert" oder "deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="2161d-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="2161d-174">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="2161d-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="2161d-175">`[ReplicationRole <String>]`: Die Replikations Rolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="2161d-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="2161d-176">`[SkuCapacity <Int32?>]`: Die Skalierungskapazität, die die Compute-Einheiten des Servers repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="2161d-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="2161d-177">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="2161d-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="2161d-178">`[SkuName <String>]`: Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="2161d-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="2161d-179">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="2161d-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="2161d-180">`[SkuTier <SkuTier?>]`: Die Stufe der jeweiligen SKU, z.b. Basic.</span><span class="sxs-lookup"><span data-stu-id="2161d-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="2161d-181">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren der SSL-Erzwingung oder nicht, wenn eine Verbindung mit dem Server hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2161d-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="2161d-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup-Aufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="2161d-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="2161d-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie Geo-redundante oder nicht für Server-Backups.</span><span class="sxs-lookup"><span data-stu-id="2161d-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="2161d-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren der automatischen Vergrößerung von Speicher.</span><span class="sxs-lookup"><span data-stu-id="2161d-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="2161d-185">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="2161d-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="2161d-186">`[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="2161d-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="2161d-187">`[Version <ServerVersion?>]`: Server Version.</span><span class="sxs-lookup"><span data-stu-id="2161d-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="2161d-188">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2161d-188">RELATED LINKS</span></span>

