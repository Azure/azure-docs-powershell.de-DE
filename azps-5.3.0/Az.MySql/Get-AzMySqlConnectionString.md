---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: d6dda5e26603c2276210e4bf00b8b9c040568f12
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468276"
---
# <span data-ttu-id="f3722-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="f3722-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="f3722-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3722-102">SYNOPSIS</span></span>
<span data-ttu-id="f3722-103">Erhalten Sie die Verbindungszeichenfolge entsprechend dem Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="f3722-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="f3722-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3722-104">SYNTAX</span></span>

### <span data-ttu-id="f3722-105">Get (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3722-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f3722-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f3722-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3722-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3722-107">DESCRIPTION</span></span>
<span data-ttu-id="f3722-108">Erhalten Sie die Verbindungszeichenfolge entsprechend dem Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="f3722-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="f3722-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3722-109">EXAMPLES</span></span>

### <span data-ttu-id="f3722-110">Beispiel 1: Get MySql server connection string by resource group and server name</span><span class="sxs-lookup"><span data-stu-id="f3722-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="f3722-111">Dieses Cmdlet ruft die MySql -Serververbindungszeichenfolge nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="f3722-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="f3722-112">Beispiel 2: Erhalten der MySql -Serververbindungszeichenfolge nach Identität</span><span class="sxs-lookup"><span data-stu-id="f3722-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="f3722-113">Dieses Cmdlet ruft die MySql -Serververbindungszeichenfolge nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="f3722-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="f3722-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3722-114">PARAMETERS</span></span>

### <span data-ttu-id="f3722-115">-Client</span><span class="sxs-lookup"><span data-stu-id="f3722-115">-Client</span></span>
<span data-ttu-id="f3722-116">Clientverbindungsanbieter.</span><span class="sxs-lookup"><span data-stu-id="f3722-116">Client connection provider.</span></span>

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

### <span data-ttu-id="f3722-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3722-117">-DefaultProfile</span></span>
<span data-ttu-id="f3722-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3722-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3722-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3722-119">-InputObject</span></span>
<span data-ttu-id="f3722-120">Das Quellserverobjekt, aus dem eine Replikat erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3722-120">The source server object to create replica from.</span></span>
<span data-ttu-id="f3722-121">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f3722-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3722-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f3722-122">-Name</span></span>
<span data-ttu-id="f3722-123">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="f3722-123">The name of the server.</span></span>

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

### <span data-ttu-id="f3722-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3722-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3722-125">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="f3722-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f3722-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3722-126">-SubscriptionId</span></span>
<span data-ttu-id="f3722-127">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3722-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f3722-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3722-128">CommonParameters</span></span>
<span data-ttu-id="f3722-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3722-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3722-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3722-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3722-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3722-131">INPUTS</span></span>

### <span data-ttu-id="f3722-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="f3722-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="f3722-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3722-133">OUTPUTS</span></span>

### <span data-ttu-id="f3722-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f3722-134">System.String</span></span>

## <span data-ttu-id="f3722-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f3722-135">NOTES</span></span>

<span data-ttu-id="f3722-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f3722-136">ALIASES</span></span>

<span data-ttu-id="f3722-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f3722-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f3722-138">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f3722-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3722-139">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f3722-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f3722-140">INPUTOBJECT <IServer> : Das Quellserverobjekt, aus dem eine Replikaterstellung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3722-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="f3722-141">`Location <String>`: Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="f3722-141">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="f3722-142">`SkuName <String>`: Der Name der SKU, in der Regel Stufe + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="f3722-142">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="f3722-143">`[Tag <ITrackedResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="f3722-143">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="f3722-144">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="f3722-144">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f3722-145">`[AdministratorLogin <String>]`: Der Anmeldename eines Administrators für einen Server.</span><span class="sxs-lookup"><span data-stu-id="f3722-145">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="f3722-146">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="f3722-146">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="f3722-147">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="f3722-147">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="f3722-148">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="f3722-148">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="f3722-149">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="f3722-149">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="f3722-150">Legen Sie diesen Wert auf "SystemAssigned" ein, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="f3722-150">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="f3722-151">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob die Serverinfrastrukturverschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f3722-151">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="f3722-152">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="f3722-152">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="f3722-153">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingen Sie eine minimale Version von Tls für den Server.</span><span class="sxs-lookup"><span data-stu-id="f3722-153">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="f3722-154">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Gibt an, ob der Zugriff auf öffentliche Netzwerke für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="f3722-154">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="f3722-155">Der Wert ist optional, muss aber bei übergebenem Wert "Enabled" oder "Disabled" sein.</span><span class="sxs-lookup"><span data-stu-id="f3722-155">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="f3722-156">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="f3722-156">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="f3722-157">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="f3722-157">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="f3722-158">`[SkuCapacity <Int32?>]`: Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3722-158">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="f3722-159">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="f3722-159">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="f3722-160">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3722-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="f3722-161">`[SkuTier <SkuTier?>]`: Die Ebene einer bestimmten SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="f3722-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="f3722-162">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="f3722-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="f3722-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="f3722-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="f3722-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="f3722-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="f3722-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Speicher automatisch anwachsen".</span><span class="sxs-lookup"><span data-stu-id="f3722-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="f3722-166">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="f3722-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="f3722-167">`[UserVisibleState <ServerState?>]`: Der Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="f3722-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="f3722-168">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="f3722-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="f3722-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f3722-169">RELATED LINKS</span></span>

