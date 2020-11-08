---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: ab2e820ec0e1c943cfeb5f8b3d83babece38ed95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173687"
---
# <span data-ttu-id="572cb-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="572cb-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="572cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="572cb-102">SYNOPSIS</span></span>
<span data-ttu-id="572cb-103">Rufen Sie die Verbindungszeichenfolge entsprechend dem Client Verbindungsanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="572cb-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="572cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="572cb-104">SYNTAX</span></span>

### <span data-ttu-id="572cb-105">Abrufen (Standard)</span><span class="sxs-lookup"><span data-stu-id="572cb-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="572cb-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="572cb-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="572cb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="572cb-107">DESCRIPTION</span></span>
<span data-ttu-id="572cb-108">Rufen Sie die Verbindungszeichenfolge entsprechend dem Client Verbindungsanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="572cb-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="572cb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="572cb-109">EXAMPLES</span></span>

### <span data-ttu-id="572cb-110">Beispiel 1: Abrufen der MySQL Server-Verbindungszeichenfolge nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="572cb-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="572cb-111">Dieses Cmdlet ruft die MySQL Server-Verbindungszeichenfolge nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="572cb-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="572cb-112">Beispiel 2: Abrufen der Verbindungszeichenfolge von MySQL Server nach Identität</span><span class="sxs-lookup"><span data-stu-id="572cb-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="572cb-113">Dieses Cmdlet ruft die MySQL Server-Verbindungszeichenfolge nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="572cb-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="572cb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="572cb-114">PARAMETERS</span></span>

### <span data-ttu-id="572cb-115">-Client</span><span class="sxs-lookup"><span data-stu-id="572cb-115">-Client</span></span>
<span data-ttu-id="572cb-116">Client Verbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="572cb-116">Client connection provider.</span></span>

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

### <span data-ttu-id="572cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572cb-117">-DefaultProfile</span></span>
<span data-ttu-id="572cb-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="572cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="572cb-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="572cb-119">-InputObject</span></span>
<span data-ttu-id="572cb-120">Das Quellserver Objekt, aus dem Replikat erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="572cb-120">The source server object to create replica from.</span></span>
<span data-ttu-id="572cb-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="572cb-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="572cb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="572cb-122">-Name</span></span>
<span data-ttu-id="572cb-123">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="572cb-123">The name of the server.</span></span>

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

### <span data-ttu-id="572cb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572cb-124">-ResourceGroupName</span></span>
<span data-ttu-id="572cb-125">Der Name der Ressourcengruppe, die die Ressource enthält, Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="572cb-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="572cb-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="572cb-126">-SubscriptionId</span></span>
<span data-ttu-id="572cb-127">Die Abonnement-ID, die ein Azure-Abonnement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="572cb-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="572cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572cb-128">CommonParameters</span></span>
<span data-ttu-id="572cb-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="572cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572cb-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="572cb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572cb-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="572cb-131">INPUTS</span></span>

### <span data-ttu-id="572cb-132">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="572cb-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="572cb-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="572cb-133">OUTPUTS</span></span>

### <span data-ttu-id="572cb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="572cb-134">System.String</span></span>

## <span data-ttu-id="572cb-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="572cb-135">NOTES</span></span>

<span data-ttu-id="572cb-136">Aliase</span><span class="sxs-lookup"><span data-stu-id="572cb-136">ALIASES</span></span>

<span data-ttu-id="572cb-137">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="572cb-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="572cb-138">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="572cb-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="572cb-139">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="572cb-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="572cb-140">Inputobject <IServer> : das Quellserver Objekt, aus dem Replikat erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="572cb-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="572cb-141">`Location <String>`: Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="572cb-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="572cb-142">`[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="572cb-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="572cb-143">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="572cb-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="572cb-144">`[AdministratorLogin <String>]`: Der Anmeldename des Administrators auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="572cb-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="572cb-145">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="572cb-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="572cb-146">`[EarliestRestoreDate <DateTime?>]`: Frühester Erstellungszeitpunkt des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="572cb-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="572cb-147">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="572cb-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="572cb-148">`[IdentityType <IdentityType?>]`: Der Identity-Typ.</span><span class="sxs-lookup"><span data-stu-id="572cb-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="572cb-149">Legen Sie diesen Wert auf "SystemAssigned", um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="572cb-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="572cb-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob die Server-Infrastruktur Verschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="572cb-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="572cb-151">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="572cb-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="572cb-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingen Sie eine minimale TLS-Version für den Server.</span><span class="sxs-lookup"><span data-stu-id="572cb-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="572cb-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Ob öffentlicher Netzwerkzugriff für diesen Server zulässig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="572cb-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="572cb-154">Der Wert ist optional, muss aber bei der Übergabe "aktiviert" oder "deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="572cb-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="572cb-155">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="572cb-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="572cb-156">`[ReplicationRole <String>]`: Die Replikations Rolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="572cb-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="572cb-157">`[SkuCapacity <Int32?>]`: Die Skalierungskapazität, die die Compute-Einheiten des Servers repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="572cb-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="572cb-158">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="572cb-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="572cb-159">`[SkuName <String>]`: Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="572cb-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="572cb-160">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="572cb-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="572cb-161">`[SkuTier <SkuTier?>]`: Die Stufe der jeweiligen SKU, z.b. Basic.</span><span class="sxs-lookup"><span data-stu-id="572cb-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="572cb-162">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren der SSL-Erzwingung oder nicht, wenn eine Verbindung mit dem Server hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="572cb-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="572cb-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup-Aufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="572cb-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="572cb-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie Geo-redundante oder nicht für Server-Backups.</span><span class="sxs-lookup"><span data-stu-id="572cb-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="572cb-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren der automatischen Vergrößerung von Speicher.</span><span class="sxs-lookup"><span data-stu-id="572cb-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="572cb-166">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="572cb-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="572cb-167">`[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="572cb-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="572cb-168">`[Version <ServerVersion?>]`: Server Version.</span><span class="sxs-lookup"><span data-stu-id="572cb-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="572cb-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="572cb-169">RELATED LINKS</span></span>

