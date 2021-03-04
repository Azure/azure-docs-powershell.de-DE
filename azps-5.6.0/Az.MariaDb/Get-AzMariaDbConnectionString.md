---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 6b0aad7829dc337869c26656135d039b5f74974f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934123"
---
# <span data-ttu-id="edbd4-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="edbd4-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="edbd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="edbd4-103">Holen Sie sich die Verbindungszeichenfolge einer MariaDB unter einem bestimmten Framework.</span><span class="sxs-lookup"><span data-stu-id="edbd4-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="edbd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edbd4-104">SYNTAX</span></span>

### <span data-ttu-id="edbd4-105">Servername (Standard)</span><span class="sxs-lookup"><span data-stu-id="edbd4-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="edbd4-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="edbd4-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="edbd4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edbd4-107">DESCRIPTION</span></span>
<span data-ttu-id="edbd4-108">Holen Sie sich die Verbindungszeichenfolge einer MariaDB unter einem bestimmten Framework.</span><span class="sxs-lookup"><span data-stu-id="edbd4-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="edbd4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="edbd4-109">EXAMPLES</span></span>

### <span data-ttu-id="edbd4-110">Beispiel 1: Herunterladen einer Verbindungszeichenfolge von MariaDB</span><span class="sxs-lookup"><span data-stu-id="edbd4-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="edbd4-111">Dieser Befehl ruft eine Verbindungszeichenfolge von MariaDB ab.</span><span class="sxs-lookup"><span data-stu-id="edbd4-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="edbd4-112">Beispiel 2: Erhalten einer Verbindungszeichenfolge von MariaDB</span><span class="sxs-lookup"><span data-stu-id="edbd4-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="edbd4-113">Dieser Befehl ruft eine Verbindungszeichenfolge von MariaDB ab.</span><span class="sxs-lookup"><span data-stu-id="edbd4-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="edbd4-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="edbd4-114">PARAMETERS</span></span>

### <span data-ttu-id="edbd4-115">-Client</span><span class="sxs-lookup"><span data-stu-id="edbd4-115">-Client</span></span>
<span data-ttu-id="edbd4-116">Verbindungsclienttyp</span><span class="sxs-lookup"><span data-stu-id="edbd4-116">Connect client type</span></span>

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

### <span data-ttu-id="edbd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edbd4-117">-DefaultProfile</span></span>
<span data-ttu-id="edbd4-118">region DefaultParameters Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edbd4-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edbd4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edbd4-119">-InputObject</span></span>
<span data-ttu-id="edbd4-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="edbd4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edbd4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="edbd4-121">-Name</span></span>
<span data-ttu-id="edbd4-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="edbd4-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbd4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edbd4-123">-ResourceGroupName</span></span>
<span data-ttu-id="edbd4-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="edbd4-124">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbd4-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="edbd4-125">-SubscriptionId</span></span>
<span data-ttu-id="edbd4-126">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="edbd4-126">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbd4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbd4-127">CommonParameters</span></span>
<span data-ttu-id="edbd4-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edbd4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbd4-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edbd4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbd4-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="edbd4-130">INPUTS</span></span>

### <span data-ttu-id="edbd4-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="edbd4-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="edbd4-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="edbd4-132">OUTPUTS</span></span>

### <span data-ttu-id="edbd4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="edbd4-133">System.String</span></span>

## <span data-ttu-id="edbd4-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="edbd4-134">NOTES</span></span>

<span data-ttu-id="edbd4-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="edbd4-135">ALIASES</span></span>

<span data-ttu-id="edbd4-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="edbd4-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="edbd4-137">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="edbd4-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="edbd4-138">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="edbd4-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="edbd4-139">INPUTOBJECT <IServer> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="edbd4-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="edbd4-140">`Location <String>`: Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="edbd4-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="edbd4-141">`[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="edbd4-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="edbd4-142">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="edbd4-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="edbd4-143">`[AdministratorLogin <String>]`: Der Anmeldename eines Servers des Administrators.</span><span class="sxs-lookup"><span data-stu-id="edbd4-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="edbd4-144">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="edbd4-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="edbd4-145">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="edbd4-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="edbd4-146">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="edbd4-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="edbd4-147">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="edbd4-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="edbd4-148">Legen Sie dies auf "SystemAssigned" festgelegt, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="edbd4-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="edbd4-149">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="edbd4-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="edbd4-150">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="edbd4-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="edbd4-151">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="edbd4-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="edbd4-152">`[SkuCapacity <Int32?>]`: Die skalierungs-/out-Kapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="edbd4-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="edbd4-153">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="edbd4-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="edbd4-154">`[SkuName <String>]`: Der Name der Sku , in der Regel, Ebene + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="edbd4-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="edbd4-155">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="edbd4-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="edbd4-156">`[SkuTier <SkuTier?>]`: Die Ebene der jeweiligen SKU, z. B. Basic.</span><span class="sxs-lookup"><span data-stu-id="edbd4-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="edbd4-157">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="edbd4-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="edbd4-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="edbd4-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="edbd4-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="edbd4-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="edbd4-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Automatisches Wachstum" für Speicher.</span><span class="sxs-lookup"><span data-stu-id="edbd4-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="edbd4-161">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="edbd4-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="edbd4-162">`[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="edbd4-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="edbd4-163">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="edbd4-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="edbd4-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="edbd4-164">RELATED LINKS</span></span>

