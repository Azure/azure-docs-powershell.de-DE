---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: ae0a5f2130ea4b5120fdbe78ab4cc23a7eba29a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941499"
---
# <span data-ttu-id="c5aca-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="c5aca-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="c5aca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5aca-102">SYNOPSIS</span></span>
<span data-ttu-id="c5aca-103">Holen Sie sich die Verbindungszeichenfolge entsprechend dem Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="c5aca-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="c5aca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5aca-104">SYNTAX</span></span>

### <span data-ttu-id="c5aca-105">Get (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5aca-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c5aca-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c5aca-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5aca-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5aca-107">DESCRIPTION</span></span>
<span data-ttu-id="c5aca-108">Holen Sie sich die Verbindungszeichenfolge entsprechend dem Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="c5aca-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="c5aca-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c5aca-109">EXAMPLES</span></span>

### <span data-ttu-id="c5aca-110">Beispiel 1: Holen Sie sich die PostgreSql-Serververbindungszeichenfolge nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="c5aca-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="c5aca-111">Dieses Cmdlet ruft die PostgreSql-Serververbindungszeichenfolge nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="c5aca-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="c5aca-112">Beispiel 2: Serververbindungszeichenfolge für PostgreSql nach Identität</span><span class="sxs-lookup"><span data-stu-id="c5aca-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="c5aca-113">Dieses Cmdlet ruft die PostgreSql-Serververbindungszeichenfolge nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="c5aca-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="c5aca-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c5aca-114">PARAMETERS</span></span>

### <span data-ttu-id="c5aca-115">-Client</span><span class="sxs-lookup"><span data-stu-id="c5aca-115">-Client</span></span>
<span data-ttu-id="c5aca-116">Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="c5aca-116">Client connection provider.</span></span>

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

### <span data-ttu-id="c5aca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5aca-117">-DefaultProfile</span></span>
<span data-ttu-id="c5aca-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5aca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5aca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5aca-119">-InputObject</span></span>
<span data-ttu-id="c5aca-120">Der Server für die Verbindungszeichenfolge Zum Erstellen finden Sie im Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c5aca-120">The server for the connection string To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c5aca-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c5aca-121">-Name</span></span>
<span data-ttu-id="c5aca-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="c5aca-122">The name of the server.</span></span>

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

### <span data-ttu-id="c5aca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5aca-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5aca-124">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="c5aca-124">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c5aca-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5aca-125">-SubscriptionId</span></span>
<span data-ttu-id="c5aca-126">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c5aca-126">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c5aca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5aca-127">CommonParameters</span></span>
<span data-ttu-id="c5aca-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5aca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5aca-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5aca-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5aca-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c5aca-130">INPUTS</span></span>

### <span data-ttu-id="c5aca-131">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="c5aca-131">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="c5aca-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c5aca-132">OUTPUTS</span></span>

### <span data-ttu-id="c5aca-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c5aca-133">System.String</span></span>

## <span data-ttu-id="c5aca-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c5aca-134">NOTES</span></span>

<span data-ttu-id="c5aca-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c5aca-135">ALIASES</span></span>

<span data-ttu-id="c5aca-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c5aca-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c5aca-137">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c5aca-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c5aca-138">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c5aca-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c5aca-139">INPUTOBJECT <IServer> : Der Server für die Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c5aca-139">INPUTOBJECT <IServer>: The server for the connection string</span></span>
  - <span data-ttu-id="c5aca-140">`Location <String>`: Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="c5aca-140">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="c5aca-141">`[Tag <ITrackedResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="c5aca-141">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="c5aca-142">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c5aca-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c5aca-143">`[AdministratorLogin <String>]`: Der Anmeldename eines Servers des Administrators.</span><span class="sxs-lookup"><span data-stu-id="c5aca-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="c5aca-144">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="c5aca-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="c5aca-145">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="c5aca-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="c5aca-146">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="c5aca-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="c5aca-147">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="c5aca-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="c5aca-148">Legen Sie dies auf "SystemAssigned" festgelegt, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="c5aca-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="c5aca-149">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob der Server die Infrastrukturverschlüsselung aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="c5aca-149">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="c5aca-150">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="c5aca-150">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="c5aca-151">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingt eine minimale Tls-Version für den Server.</span><span class="sxs-lookup"><span data-stu-id="c5aca-151">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="c5aca-152">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Gibt an, ob der Zugriff auf das öffentliche Netzwerk für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="c5aca-152">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="c5aca-153">Der Wert ist optional, aber wenn er übergeben wird, muss er "Aktiviert" oder "Deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="c5aca-153">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="c5aca-154">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="c5aca-154">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="c5aca-155">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="c5aca-155">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="c5aca-156">`[SkuCapacity <Int32?>]`: Die skalierungs-/out-Kapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="c5aca-156">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="c5aca-157">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="c5aca-157">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="c5aca-158">`[SkuName <String>]`: Der Name der Sku , in der Regel, Ebene + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c5aca-158">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="c5aca-159">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5aca-159">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="c5aca-160">`[SkuTier <SkuTier?>]`: Die Ebene der jeweiligen SKU, z. B. Basic.</span><span class="sxs-lookup"><span data-stu-id="c5aca-160">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="c5aca-161">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="c5aca-161">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="c5aca-162">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="c5aca-162">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="c5aca-163">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="c5aca-163">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="c5aca-164">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Automatisches Wachstum" für Speicher.</span><span class="sxs-lookup"><span data-stu-id="c5aca-164">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="c5aca-165">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="c5aca-165">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="c5aca-166">`[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="c5aca-166">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="c5aca-167">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="c5aca-167">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="c5aca-168">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c5aca-168">RELATED LINKS</span></span>

