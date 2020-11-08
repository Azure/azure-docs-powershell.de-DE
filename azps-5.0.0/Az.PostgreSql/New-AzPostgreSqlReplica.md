---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: e3c0d7e8d3b3d9fe42bc97c40ad54424b7bfd0da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177773"
---
# <span data-ttu-id="5205f-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="5205f-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="5205f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5205f-102">SYNOPSIS</span></span>
<span data-ttu-id="5205f-103">Erstellt ein neues Replikat aus einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5205f-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="5205f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5205f-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5205f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5205f-105">DESCRIPTION</span></span>
<span data-ttu-id="5205f-106">Erstellt ein neues Replikat aus einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5205f-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="5205f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5205f-107">EXAMPLES</span></span>

### <span data-ttu-id="5205f-108">Beispiel 1: Erstellen eines neuen PostgreSQL-Server Replikats</span><span class="sxs-lookup"><span data-stu-id="5205f-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="5205f-109">Dieses Cmdlet erstellt ein neues PostgreSQL-Server Replikat.</span><span class="sxs-lookup"><span data-stu-id="5205f-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="5205f-110">Beispiel 2: Erstellen eines neuen PostgreSQL-Server Replikats</span><span class="sxs-lookup"><span data-stu-id="5205f-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="5205f-111">Dieses Cmdlet erstellt ein neues PostgreSQL-Server Replikat.</span><span class="sxs-lookup"><span data-stu-id="5205f-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="5205f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5205f-112">PARAMETERS</span></span>

### <span data-ttu-id="5205f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5205f-113">-AsJob</span></span>
<span data-ttu-id="5205f-114">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="5205f-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="5205f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5205f-115">-DefaultProfile</span></span>
<span data-ttu-id="5205f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5205f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5205f-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="5205f-117">-Location</span></span>
<span data-ttu-id="5205f-118">Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="5205f-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="5205f-119">-Master</span><span class="sxs-lookup"><span data-stu-id="5205f-119">-Master</span></span>
<span data-ttu-id="5205f-120">Das Quellserver Objekt, aus dem Replikat erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5205f-120">The source server object to create replica from.</span></span>
<span data-ttu-id="5205f-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Master Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5205f-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5205f-122">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5205f-122">-NoWait</span></span>
<span data-ttu-id="5205f-123">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="5205f-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="5205f-124">-Replicaname</span><span class="sxs-lookup"><span data-stu-id="5205f-124">-ReplicaName</span></span>
<span data-ttu-id="5205f-125">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5205f-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5205f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5205f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5205f-127">Der Name der Ressourcengruppe, die die Ressource enthält, Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="5205f-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5205f-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="5205f-128">-Sku</span></span>
<span data-ttu-id="5205f-129">Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="5205f-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="5205f-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5205f-130">-SubscriptionId</span></span>
<span data-ttu-id="5205f-131">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5205f-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5205f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5205f-132">-Confirm</span></span>
<span data-ttu-id="5205f-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5205f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5205f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5205f-134">-WhatIf</span></span>
<span data-ttu-id="5205f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5205f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5205f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5205f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5205f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5205f-137">CommonParameters</span></span>
<span data-ttu-id="5205f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5205f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5205f-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5205f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5205f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5205f-140">INPUTS</span></span>

### <span data-ttu-id="5205f-141">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="5205f-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="5205f-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5205f-142">OUTPUTS</span></span>

### <span data-ttu-id="5205f-143">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="5205f-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="5205f-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="5205f-144">NOTES</span></span>

<span data-ttu-id="5205f-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="5205f-145">ALIASES</span></span>

<span data-ttu-id="5205f-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5205f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5205f-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5205f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5205f-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5205f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5205f-149">Master <IServer> : das Quellserver Objekt, aus dem Replikat erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5205f-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="5205f-150">`Location <String>`: Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="5205f-150">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="5205f-151">`[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="5205f-151">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="5205f-152">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5205f-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5205f-153">`[AdministratorLogin <String>]`: Der Anmeldename des Administrators auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="5205f-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="5205f-154">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="5205f-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="5205f-155">`[EarliestRestoreDate <DateTime?>]`: Frühester Erstellungszeitpunkt des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="5205f-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="5205f-156">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="5205f-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="5205f-157">`[IdentityType <IdentityType?>]`: Der Identity-Typ.</span><span class="sxs-lookup"><span data-stu-id="5205f-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="5205f-158">Legen Sie diesen Wert auf "SystemAssigned", um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="5205f-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="5205f-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob die Server-Infrastruktur Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5205f-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="5205f-160">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="5205f-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="5205f-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingen Sie eine minimale TLS-Version für den Server.</span><span class="sxs-lookup"><span data-stu-id="5205f-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="5205f-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Ob öffentlicher Netzwerkzugriff für diesen Server zulässig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="5205f-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="5205f-163">Der Wert ist optional, muss aber bei der Übergabe "aktiviert" oder "deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="5205f-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="5205f-164">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="5205f-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="5205f-165">`[ReplicationRole <String>]`: Die Replikations Rolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="5205f-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="5205f-166">`[SkuCapacity <Int32?>]`: Die Skalierungskapazität, die die Compute-Einheiten des Servers repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="5205f-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="5205f-167">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="5205f-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="5205f-168">`[SkuName <String>]`: Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="5205f-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="5205f-169">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="5205f-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="5205f-170">`[SkuTier <SkuTier?>]`: Die Stufe der jeweiligen SKU, z.b. Basic.</span><span class="sxs-lookup"><span data-stu-id="5205f-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="5205f-171">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren der SSL-Erzwingung oder nicht, wenn eine Verbindung mit dem Server hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5205f-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="5205f-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup-Aufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="5205f-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="5205f-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie Geo-redundante oder nicht für Server-Backups.</span><span class="sxs-lookup"><span data-stu-id="5205f-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="5205f-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren der automatischen Vergrößerung von Speicher.</span><span class="sxs-lookup"><span data-stu-id="5205f-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="5205f-175">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="5205f-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="5205f-176">`[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="5205f-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="5205f-177">`[Version <ServerVersion?>]`: Server Version.</span><span class="sxs-lookup"><span data-stu-id="5205f-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="5205f-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5205f-178">RELATED LINKS</span></span>

