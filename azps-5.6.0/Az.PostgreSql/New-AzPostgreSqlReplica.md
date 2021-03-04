---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: 5aed092485bf90418f467a2857716496f2979454
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936696"
---
# <span data-ttu-id="b9c49-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="b9c49-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="b9c49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c49-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c49-103">Erstellt ein neues Replikat aus einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b9c49-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="b9c49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9c49-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9c49-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9c49-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c49-106">Erstellt ein neues Replikat aus einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b9c49-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="b9c49-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9c49-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c49-108">Beispiel 1: Erstellen eines neuen PostgreSql-Serverreplikates</span><span class="sxs-lookup"><span data-stu-id="b9c49-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="b9c49-109">Dieses Cmdlet erstellt ein neues PostgreSql-Serverreplikate.</span><span class="sxs-lookup"><span data-stu-id="b9c49-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="b9c49-110">Beispiel 2: Erstellen eines neuen PostgreSql-Serverreplikates</span><span class="sxs-lookup"><span data-stu-id="b9c49-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="b9c49-111">Dieses Cmdlet erstellt ein neues PostgreSql-Serverreplikate.</span><span class="sxs-lookup"><span data-stu-id="b9c49-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="b9c49-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b9c49-112">PARAMETERS</span></span>

### <span data-ttu-id="b9c49-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9c49-113">-AsJob</span></span>
<span data-ttu-id="b9c49-114">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="b9c49-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="b9c49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c49-115">-DefaultProfile</span></span>
<span data-ttu-id="b9c49-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9c49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c49-117">-Location</span><span class="sxs-lookup"><span data-stu-id="b9c49-117">-Location</span></span>
<span data-ttu-id="b9c49-118">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="b9c49-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="b9c49-119">-Master</span><span class="sxs-lookup"><span data-stu-id="b9c49-119">-Master</span></span>
<span data-ttu-id="b9c49-120">Das Quellserverobjekt zum Erstellen eines Replikats.</span><span class="sxs-lookup"><span data-stu-id="b9c49-120">The source server object to create replica from.</span></span>
<span data-ttu-id="b9c49-121">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b9c49-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9c49-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b9c49-122">-NoWait</span></span>
<span data-ttu-id="b9c49-123">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="b9c49-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b9c49-124">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="b9c49-124">-ReplicaName</span></span>
<span data-ttu-id="b9c49-125">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="b9c49-125">The name of the server.</span></span>

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

### <span data-ttu-id="b9c49-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c49-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9c49-127">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="b9c49-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b9c49-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="b9c49-128">-Sku</span></span>
<span data-ttu-id="b9c49-129">Der Name der Sku ist in der Regel Ebene + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="b9c49-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="b9c49-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9c49-130">-SubscriptionId</span></span>
<span data-ttu-id="b9c49-131">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b9c49-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b9c49-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9c49-132">-Confirm</span></span>
<span data-ttu-id="b9c49-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9c49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c49-134">-WhatIf</span></span>
<span data-ttu-id="b9c49-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9c49-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c49-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9c49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c49-137">CommonParameters</span></span>
<span data-ttu-id="b9c49-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c49-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9c49-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c49-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9c49-140">INPUTS</span></span>

### <span data-ttu-id="b9c49-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="b9c49-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b9c49-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9c49-142">OUTPUTS</span></span>

### <span data-ttu-id="b9c49-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="b9c49-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b9c49-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b9c49-144">NOTES</span></span>

<span data-ttu-id="b9c49-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b9c49-145">ALIASES</span></span>

<span data-ttu-id="b9c49-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b9c49-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9c49-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b9c49-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9c49-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9c49-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9c49-149">MASTER: <IServer> Das Quellserverobjekt zum Erstellen eines Replikats.</span><span class="sxs-lookup"><span data-stu-id="b9c49-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="b9c49-150">`Location <String>`: Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="b9c49-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="b9c49-151">`[Tag <ITrackedResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="b9c49-151">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="b9c49-152">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b9c49-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b9c49-153">`[AdministratorLogin <String>]`: Der Anmeldename eines Servers des Administrators.</span><span class="sxs-lookup"><span data-stu-id="b9c49-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="b9c49-154">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="b9c49-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="b9c49-155">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="b9c49-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="b9c49-156">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="b9c49-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="b9c49-157">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="b9c49-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="b9c49-158">Legen Sie dies auf "SystemAssigned" festgelegt, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="b9c49-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="b9c49-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob der Server die Infrastrukturverschlüsselung aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="b9c49-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="b9c49-160">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="b9c49-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="b9c49-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingt eine minimale Tls-Version für den Server.</span><span class="sxs-lookup"><span data-stu-id="b9c49-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="b9c49-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Gibt an, ob der Zugriff auf das öffentliche Netzwerk für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="b9c49-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="b9c49-163">Der Wert ist optional, aber wenn er übergeben wird, muss er "Aktiviert" oder "Deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="b9c49-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="b9c49-164">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="b9c49-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="b9c49-165">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="b9c49-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="b9c49-166">`[SkuCapacity <Int32?>]`: Die skalierungs-/out-Kapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c49-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="b9c49-167">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="b9c49-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="b9c49-168">`[SkuName <String>]`: Der Name der Sku , in der Regel, Ebene + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="b9c49-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="b9c49-169">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9c49-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="b9c49-170">`[SkuTier <SkuTier?>]`: Die Ebene der jeweiligen SKU, z. B. Basic.</span><span class="sxs-lookup"><span data-stu-id="b9c49-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="b9c49-171">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="b9c49-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="b9c49-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="b9c49-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="b9c49-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="b9c49-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="b9c49-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Automatisches Wachstum" für Speicher.</span><span class="sxs-lookup"><span data-stu-id="b9c49-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="b9c49-175">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="b9c49-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="b9c49-176">`[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="b9c49-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="b9c49-177">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="b9c49-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="b9c49-178">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b9c49-178">RELATED LINKS</span></span>

