---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 54463e38982a711f98515879f826a3cd2e068384
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467559"
---
# <span data-ttu-id="e337b-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="e337b-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="e337b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e337b-102">SYNOPSIS</span></span>
<span data-ttu-id="e337b-103">Erstellt eine neue Replikatdatei aus einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e337b-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="e337b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e337b-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e337b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e337b-105">DESCRIPTION</span></span>
<span data-ttu-id="e337b-106">Erstellt eine neue Replikatdatei aus einer vorhandenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e337b-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="e337b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e337b-107">EXAMPLES</span></span>

### <span data-ttu-id="e337b-108">Beispiel 1: Erstellen einer neuen MySql-Serverreplikate</span><span class="sxs-lookup"><span data-stu-id="e337b-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="e337b-109">Dieses Cmdlet erstellt eine neue MySql-Serverreplikate.</span><span class="sxs-lookup"><span data-stu-id="e337b-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="e337b-110">Beispiel 2: Erstellen einer neuen MySql-Serverreplikate</span><span class="sxs-lookup"><span data-stu-id="e337b-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="e337b-111">Dieses Cmdlet mit Parametermaster(inputobject) erstellt eine neue MySql-Serverreplikate.</span><span class="sxs-lookup"><span data-stu-id="e337b-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="e337b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e337b-112">PARAMETERS</span></span>

### <span data-ttu-id="e337b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e337b-113">-AsJob</span></span>
<span data-ttu-id="e337b-114">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="e337b-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="e337b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e337b-115">-DefaultProfile</span></span>
<span data-ttu-id="e337b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e337b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e337b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e337b-117">-Location</span></span>
<span data-ttu-id="e337b-118">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="e337b-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="e337b-119">-Master</span><span class="sxs-lookup"><span data-stu-id="e337b-119">-Master</span></span>
<span data-ttu-id="e337b-120">Das Quellserverobjekt, aus dem eine Replikat erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e337b-120">The source server object to create replica from.</span></span>
<span data-ttu-id="e337b-121">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e337b-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e337b-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e337b-122">-NoWait</span></span>
<span data-ttu-id="e337b-123">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="e337b-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="e337b-124">-Replica</span><span class="sxs-lookup"><span data-stu-id="e337b-124">-Replica</span></span>
<span data-ttu-id="e337b-125">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="e337b-125">The name of the server.</span></span>

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

### <span data-ttu-id="e337b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e337b-126">-ResourceGroupName</span></span>
<span data-ttu-id="e337b-127">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e337b-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e337b-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="e337b-128">-Sku</span></span>
<span data-ttu-id="e337b-129">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="e337b-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="e337b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e337b-130">-SubscriptionId</span></span>
<span data-ttu-id="e337b-131">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e337b-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e337b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e337b-132">-Confirm</span></span>
<span data-ttu-id="e337b-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e337b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e337b-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e337b-134">-WhatIf</span></span>
<span data-ttu-id="e337b-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e337b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e337b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e337b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e337b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e337b-137">CommonParameters</span></span>
<span data-ttu-id="e337b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e337b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e337b-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e337b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e337b-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e337b-140">INPUTS</span></span>

### <span data-ttu-id="e337b-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="e337b-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e337b-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e337b-142">OUTPUTS</span></span>

### <span data-ttu-id="e337b-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="e337b-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e337b-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e337b-144">NOTES</span></span>

<span data-ttu-id="e337b-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e337b-145">ALIASES</span></span>

<span data-ttu-id="e337b-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e337b-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e337b-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e337b-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e337b-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e337b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e337b-149">MASTER: <IServer> Das Quellserverobjekt, aus dem eine Replikaterstellung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e337b-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="e337b-150">`Location <String>`: Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="e337b-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="e337b-151">`SkuName <String>`: Der Name der SKU, in der Regel Stufe + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="e337b-151">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="e337b-152">`[Tag <ITrackedResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="e337b-152">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="e337b-153">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="e337b-153">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e337b-154">`[AdministratorLogin <String>]`: Der Anmeldename eines Administrators für einen Server.</span><span class="sxs-lookup"><span data-stu-id="e337b-154">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="e337b-155">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="e337b-155">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="e337b-156">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="e337b-156">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="e337b-157">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="e337b-157">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="e337b-158">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="e337b-158">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="e337b-159">Legen Sie diesen Wert auf "SystemAssigned" ein, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e337b-159">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="e337b-160">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status, der zeigt, ob die Serverinfrastrukturverschlüsselung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e337b-160">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="e337b-161">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="e337b-161">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="e337b-162">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Erzwingen Sie eine minimale Version von Tls für den Server.</span><span class="sxs-lookup"><span data-stu-id="e337b-162">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="e337b-163">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Gibt an, ob der Zugriff auf öffentliche Netzwerke für diesen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="e337b-163">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="e337b-164">Der Wert ist optional, muss aber bei übergebenem Wert "Enabled" oder "Disabled" sein.</span><span class="sxs-lookup"><span data-stu-id="e337b-164">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="e337b-165">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="e337b-165">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="e337b-166">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="e337b-166">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="e337b-167">`[SkuCapacity <Int32?>]`: Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="e337b-167">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="e337b-168">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="e337b-168">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="e337b-169">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e337b-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="e337b-170">`[SkuTier <SkuTier?>]`: Die Ebene einer bestimmten SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="e337b-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="e337b-171">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="e337b-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="e337b-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="e337b-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="e337b-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="e337b-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="e337b-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Speicher automatisch anwachsen".</span><span class="sxs-lookup"><span data-stu-id="e337b-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="e337b-175">`[StorageProfileStorageMb <Int32?>]`: Maximal zulässiger Speicherplatz für einen Server.</span><span class="sxs-lookup"><span data-stu-id="e337b-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="e337b-176">`[UserVisibleState <ServerState?>]`: Der Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="e337b-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="e337b-177">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="e337b-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="e337b-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e337b-178">RELATED LINKS</span></span>

