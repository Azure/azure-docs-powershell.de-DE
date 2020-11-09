---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 8df35a38889e2c91bd74625ae916fd10739d9db1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303423"
---
# <span data-ttu-id="8789f-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="8789f-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="8789f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8789f-102">SYNOPSIS</span></span>
<span data-ttu-id="8789f-103">Rufen Sie die Verbindungszeichenfolge entsprechend dem Client Verbindungsanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="8789f-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="8789f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8789f-104">SYNTAX</span></span>

### <span data-ttu-id="8789f-105">Abrufen (Standard)</span><span class="sxs-lookup"><span data-stu-id="8789f-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8789f-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8789f-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8789f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8789f-107">DESCRIPTION</span></span>
<span data-ttu-id="8789f-108">Rufen Sie die Verbindungszeichenfolge entsprechend dem Client Verbindungsanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="8789f-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="8789f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8789f-109">EXAMPLES</span></span>

### <span data-ttu-id="8789f-110">Beispiel 1: Abrufen der Verbindungszeichenfolge des PostgreSQL-Servers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="8789f-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="8789f-111">Dieses Cmdlet ruft die Verbindungszeichenfolge des PostgreSQL-Servers nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="8789f-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="8789f-112">Beispiel 2: Abrufen der Verbindungszeichenfolge des PostgreSQL-Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="8789f-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="8789f-113">Dieses Cmdlet ruft die Verbindungszeichenfolge des PostgreSQL-Servers nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="8789f-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="8789f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8789f-114">PARAMETERS</span></span>

### <span data-ttu-id="8789f-115">-Client</span><span class="sxs-lookup"><span data-stu-id="8789f-115">-Client</span></span>
<span data-ttu-id="8789f-116">Client Verbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="8789f-116">Client connection provider.</span></span>

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

### <span data-ttu-id="8789f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8789f-117">-DefaultProfile</span></span>
<span data-ttu-id="8789f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8789f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8789f-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8789f-119">-InputObject</span></span>
<span data-ttu-id="8789f-120">Das Quellserver Objekt, aus dem Replikat erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8789f-120">The source server object to create replica from.</span></span>
<span data-ttu-id="8789f-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8789f-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8789f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8789f-122">-Name</span></span>
<span data-ttu-id="8789f-123">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="8789f-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8789f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8789f-124">-ResourceGroupName</span></span>
<span data-ttu-id="8789f-125">Der Name der Ressourcengruppe, die die Ressource enthält, Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="8789f-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8789f-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8789f-126">-SubscriptionId</span></span>
<span data-ttu-id="8789f-127">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8789f-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8789f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8789f-128">CommonParameters</span></span>
<span data-ttu-id="8789f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8789f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8789f-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8789f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8789f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8789f-131">INPUTS</span></span>

### <span data-ttu-id="8789f-132">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="8789f-132">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8789f-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8789f-133">OUTPUTS</span></span>

### <span data-ttu-id="8789f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8789f-134">System.String</span></span>

## <span data-ttu-id="8789f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="8789f-135">NOTES</span></span>

<span data-ttu-id="8789f-136">Aliase</span><span class="sxs-lookup"><span data-stu-id="8789f-136">ALIASES</span></span>

<span data-ttu-id="8789f-137">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8789f-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8789f-138">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8789f-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8789f-139">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="8789f-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8789f-140">Inputobject <IServer> : das Quellserver Objekt, aus dem Replikat erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8789f-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="8789f-141">`Location <String>`: Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="8789f-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="8789f-142">`[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="8789f-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="8789f-143">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8789f-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8789f-144">`[AdministratorLogin <String>]`: Der Anmeldename des Administrators auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="8789f-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="8789f-145">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="8789f-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="8789f-146">`[EarliestRestoreDate <DateTime?>]`: Frühester Erstellungszeitpunkt des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="8789f-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="8789f-147">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="8789f-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="8789f-148">`[IdentityType <IdentityType?>]`: Der Identity-Typ.</span><span class="sxs-lookup"><span data-stu-id="8789f-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="8789f-149">Legen Sie diesen Wert auf "SystemAssigned", um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8789f-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="8789f-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob die Server-Infrastruktur Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8789f-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="8789f-151">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="8789f-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="8789f-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingen Sie eine minimale TLS-Version für den Server.</span><span class="sxs-lookup"><span data-stu-id="8789f-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="8789f-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Ob öffentlicher Netzwerkzugriff für diesen Server zulässig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="8789f-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="8789f-154">Der Wert ist optional, muss aber bei der Übergabe "aktiviert" oder "deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="8789f-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="8789f-155">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="8789f-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="8789f-156">`[ReplicationRole <String>]`: Die Replikations Rolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="8789f-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="8789f-157">`[SkuCapacity <Int32?>]`: Die Skalierungskapazität, die die Compute-Einheiten des Servers repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="8789f-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="8789f-158">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="8789f-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="8789f-159">`[SkuName <String>]`: Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8789f-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="8789f-160">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="8789f-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="8789f-161">`[SkuTier <SkuTier?>]`: Die Stufe der jeweiligen SKU, z.b. Basic.</span><span class="sxs-lookup"><span data-stu-id="8789f-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="8789f-162">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren der SSL-Erzwingung oder nicht, wenn eine Verbindung mit dem Server hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8789f-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="8789f-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup-Aufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="8789f-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="8789f-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie Geo-redundante oder nicht für Server-Backups.</span><span class="sxs-lookup"><span data-stu-id="8789f-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="8789f-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren der automatischen Vergrößerung von Speicher.</span><span class="sxs-lookup"><span data-stu-id="8789f-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="8789f-166">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="8789f-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="8789f-167">`[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="8789f-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="8789f-168">`[Version <ServerVersion?>]`: Server Version.</span><span class="sxs-lookup"><span data-stu-id="8789f-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="8789f-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8789f-169">RELATED LINKS</span></span>

