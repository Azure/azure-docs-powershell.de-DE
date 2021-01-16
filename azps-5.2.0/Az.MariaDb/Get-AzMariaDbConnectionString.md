---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290218"
---
# <span data-ttu-id="ab817-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="ab817-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="ab817-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab817-102">SYNOPSIS</span></span>
<span data-ttu-id="ab817-103">Sie können die Verbindungszeichenfolge einer MariaDB unter einem bestimmten Framework erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab817-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="ab817-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab817-104">SYNTAX</span></span>

### <span data-ttu-id="ab817-105">Servername (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab817-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ab817-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="ab817-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab817-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab817-107">DESCRIPTION</span></span>
<span data-ttu-id="ab817-108">Sie können die Verbindungszeichenfolge einer MariaDB unter einem bestimmten Framework erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab817-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="ab817-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab817-109">EXAMPLES</span></span>

### <span data-ttu-id="ab817-110">Beispiel 1: Erhalten einer Verbindungszeichenfolge von MariaDB</span><span class="sxs-lookup"><span data-stu-id="ab817-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="ab817-111">Dieser Befehl ruft eine Verbindungszeichenfolge von MariaDB ab.</span><span class="sxs-lookup"><span data-stu-id="ab817-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="ab817-112">Beispiel 2: Erhalten einer Verbindungszeichenfolge von MariaDB</span><span class="sxs-lookup"><span data-stu-id="ab817-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="ab817-113">Dieser Befehl ruft eine Verbindungszeichenfolge von MariaDB ab.</span><span class="sxs-lookup"><span data-stu-id="ab817-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="ab817-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab817-114">PARAMETERS</span></span>

### <span data-ttu-id="ab817-115">-Client</span><span class="sxs-lookup"><span data-stu-id="ab817-115">-Client</span></span>
<span data-ttu-id="ab817-116">Clienttyp "Verbinden"</span><span class="sxs-lookup"><span data-stu-id="ab817-116">Connect client type</span></span>

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

### <span data-ttu-id="ab817-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab817-117">-DefaultProfile</span></span>
<span data-ttu-id="ab817-118">region DefaultParameters Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab817-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab817-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab817-119">-InputObject</span></span>
<span data-ttu-id="ab817-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ab817-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ab817-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ab817-121">-Name</span></span>
<span data-ttu-id="ab817-122">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="ab817-122">The name of the server.</span></span>

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

### <span data-ttu-id="ab817-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab817-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab817-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="ab817-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="ab817-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab817-125">-SubscriptionId</span></span>
<span data-ttu-id="ab817-126">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="ab817-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="ab817-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab817-127">CommonParameters</span></span>
<span data-ttu-id="ab817-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab817-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab817-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab817-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab817-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab817-130">INPUTS</span></span>

### <span data-ttu-id="ab817-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="ab817-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="ab817-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab817-132">OUTPUTS</span></span>

### <span data-ttu-id="ab817-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ab817-133">System.String</span></span>

## <span data-ttu-id="ab817-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ab817-134">NOTES</span></span>

<span data-ttu-id="ab817-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ab817-135">ALIASES</span></span>

<span data-ttu-id="ab817-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ab817-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ab817-137">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ab817-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab817-138">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ab817-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ab817-139">INPUTOBJECT <IServer> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ab817-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="ab817-140">`Location <String>`: Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="ab817-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="ab817-141">`[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="ab817-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="ab817-142">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="ab817-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ab817-143">`[AdministratorLogin <String>]`: Der Anmeldename eines Servers des Administrators.</span><span class="sxs-lookup"><span data-stu-id="ab817-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="ab817-144">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="ab817-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="ab817-145">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="ab817-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="ab817-146">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="ab817-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="ab817-147">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="ab817-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="ab817-148">Legen Sie diesen Wert auf "SystemAssigned" ein, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ab817-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="ab817-149">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="ab817-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="ab817-150">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="ab817-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="ab817-151">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="ab817-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="ab817-152">`[SkuCapacity <Int32?>]`: Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="ab817-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="ab817-153">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="ab817-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="ab817-154">`[SkuName <String>]`: Der Name der SKU, in der Regel Stufe + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="ab817-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="ab817-155">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab817-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="ab817-156">`[SkuTier <SkuTier?>]`: Die Ebene einer bestimmten SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="ab817-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="ab817-157">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="ab817-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="ab817-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="ab817-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="ab817-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="ab817-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="ab817-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Speicher automatisch anwachsen".</span><span class="sxs-lookup"><span data-stu-id="ab817-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="ab817-161">`[StorageProfileStorageMb <Int32?>]`: Maximal zulässiger Speicherplatz für einen Server.</span><span class="sxs-lookup"><span data-stu-id="ab817-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="ab817-162">`[UserVisibleState <ServerState?>]`: Der Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="ab817-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="ab817-163">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="ab817-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="ab817-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ab817-164">RELATED LINKS</span></span>

