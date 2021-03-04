---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: c85ece43045144d0befd6a6ed1e7ac1d7431796f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947840"
---
# <span data-ttu-id="6b78f-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="6b78f-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="6b78f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b78f-102">SYNOPSIS</span></span>
<span data-ttu-id="6b78f-103">Holen Sie sich die Verbindungszeichenfolge entsprechend dem Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="6b78f-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="6b78f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b78f-104">SYNTAX</span></span>

### <span data-ttu-id="6b78f-105">Get (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b78f-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b78f-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b78f-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b78f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b78f-107">DESCRIPTION</span></span>
<span data-ttu-id="6b78f-108">Holen Sie sich die Verbindungszeichenfolge entsprechend dem Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="6b78f-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="6b78f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b78f-109">EXAMPLES</span></span>

### <span data-ttu-id="6b78f-110">Beispiel 1: Get MySql server connection string by resource group and server name</span><span class="sxs-lookup"><span data-stu-id="6b78f-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="6b78f-111">Dieses Cmdlet ruft die MySql-Serververbindungszeichenfolge nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="6b78f-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="6b78f-112">Beispiel 2: Get MySql server connection string by identity</span><span class="sxs-lookup"><span data-stu-id="6b78f-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="6b78f-113">Dieses Cmdlet ruft die MySql-Serververbindungszeichenfolge nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="6b78f-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="6b78f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6b78f-114">PARAMETERS</span></span>

### <span data-ttu-id="6b78f-115">-Client</span><span class="sxs-lookup"><span data-stu-id="6b78f-115">-Client</span></span>
<span data-ttu-id="6b78f-116">Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="6b78f-116">Client connection provider.</span></span>

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

### <span data-ttu-id="6b78f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b78f-117">-DefaultProfile</span></span>
<span data-ttu-id="6b78f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b78f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b78f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b78f-119">-InputObject</span></span>
<span data-ttu-id="6b78f-120">Der Server für die Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6b78f-120">The server for the connection string.</span></span>
<span data-ttu-id="6b78f-121">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6b78f-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b78f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6b78f-122">-Name</span></span>
<span data-ttu-id="6b78f-123">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="6b78f-123">The name of the server.</span></span>

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

### <span data-ttu-id="6b78f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b78f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b78f-125">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="6b78f-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6b78f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b78f-126">-SubscriptionId</span></span>
<span data-ttu-id="6b78f-127">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6b78f-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="6b78f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b78f-128">CommonParameters</span></span>
<span data-ttu-id="6b78f-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b78f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b78f-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b78f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b78f-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b78f-131">INPUTS</span></span>

### <span data-ttu-id="6b78f-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="6b78f-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="6b78f-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b78f-133">OUTPUTS</span></span>

### <span data-ttu-id="6b78f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6b78f-134">System.String</span></span>

## <span data-ttu-id="6b78f-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6b78f-135">NOTES</span></span>

<span data-ttu-id="6b78f-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6b78f-136">ALIASES</span></span>

<span data-ttu-id="6b78f-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6b78f-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b78f-138">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="6b78f-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b78f-139">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b78f-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b78f-140">INPUTOBJECT <IServer> : Der Server für die Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6b78f-140">INPUTOBJECT <IServer>: The server for the connection string.</span></span>
  - <span data-ttu-id="6b78f-141">`Location <String>`: Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="6b78f-141">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="6b78f-142">`[Tag <ITrackedResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="6b78f-142">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="6b78f-143">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b78f-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6b78f-144">`[AdministratorLogin <String>]`: Der Anmeldename eines Servers des Administrators.</span><span class="sxs-lookup"><span data-stu-id="6b78f-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="6b78f-145">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="6b78f-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="6b78f-146">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="6b78f-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="6b78f-147">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="6b78f-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="6b78f-148">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="6b78f-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="6b78f-149">Legen Sie dies auf "SystemAssigned" festgelegt, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="6b78f-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="6b78f-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob der Server die Infrastrukturverschlüsselung aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="6b78f-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="6b78f-151">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="6b78f-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="6b78f-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingt eine minimale Tls-Version für den Server.</span><span class="sxs-lookup"><span data-stu-id="6b78f-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="6b78f-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Gibt an, ob der Zugriff auf das öffentliche Netzwerk für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6b78f-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="6b78f-154">Der Wert ist optional, aber wenn er übergeben wird, muss er "Aktiviert" oder "Deaktiviert" sein.</span><span class="sxs-lookup"><span data-stu-id="6b78f-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="6b78f-155">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="6b78f-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="6b78f-156">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="6b78f-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="6b78f-157">`[SkuCapacity <Int32?>]`: Die skalierungs-/out-Kapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b78f-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="6b78f-158">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="6b78f-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="6b78f-159">`[SkuName <String>]`: Der Name der Sku , in der Regel, Ebene + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="6b78f-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="6b78f-160">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b78f-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="6b78f-161">`[SkuTier <SkuTier?>]`: Die Ebene der jeweiligen SKU, z. B. Basic.</span><span class="sxs-lookup"><span data-stu-id="6b78f-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="6b78f-162">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="6b78f-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="6b78f-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="6b78f-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="6b78f-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="6b78f-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="6b78f-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Automatisches Wachstum" für Speicher.</span><span class="sxs-lookup"><span data-stu-id="6b78f-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="6b78f-166">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6b78f-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="6b78f-167">`[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="6b78f-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="6b78f-168">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="6b78f-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="6b78f-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6b78f-169">RELATED LINKS</span></span>

