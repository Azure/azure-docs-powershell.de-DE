---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 3e3e63bee89eb9ae89cb647b81ea7d0da792ae3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927912"
---
# <span data-ttu-id="44527-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="44527-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="44527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44527-102">SYNOPSIS</span></span>
<span data-ttu-id="44527-103">Erstellt ein Replikat eines MariaDB-Servers.</span><span class="sxs-lookup"><span data-stu-id="44527-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="44527-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44527-104">SYNTAX</span></span>

### <span data-ttu-id="44527-105">Servername (Standard)</span><span class="sxs-lookup"><span data-stu-id="44527-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44527-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="44527-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="44527-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44527-107">DESCRIPTION</span></span>
<span data-ttu-id="44527-108">Erstellt ein Replikat eines MariaDB-Servers.</span><span class="sxs-lookup"><span data-stu-id="44527-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="44527-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="44527-109">EXAMPLES</span></span>

### <span data-ttu-id="44527-110">Beispiel 1: Erstellen eines Replikat-DB für eine MariaDB</span><span class="sxs-lookup"><span data-stu-id="44527-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="44527-111">Mit diesem Befehl wird ein Replikat-DB für eine MariaDB erstellt.</span><span class="sxs-lookup"><span data-stu-id="44527-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="44527-112">Beispiel 2: Erstellen eines Replikat-DB für eine MariaDB</span><span class="sxs-lookup"><span data-stu-id="44527-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="44527-113">Mit diesem Befehl wird ein Replikat-DB für eine MariaDB erstellt.</span><span class="sxs-lookup"><span data-stu-id="44527-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="44527-114">Beispiel 3: Erstellen eines Replikat-DB für eine MariaDB</span><span class="sxs-lookup"><span data-stu-id="44527-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="44527-115">Mit diesem Befehl mit Parametereingabeobjekt wird ein Replikat-DB mit Parametereingabeobjekt für eine MariaDB erstellt.</span><span class="sxs-lookup"><span data-stu-id="44527-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="44527-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="44527-116">PARAMETERS</span></span>

### <span data-ttu-id="44527-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44527-117">-AsJob</span></span>
<span data-ttu-id="44527-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="44527-118">Run the command as a job</span></span>

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

### <span data-ttu-id="44527-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44527-119">-DefaultProfile</span></span>
<span data-ttu-id="44527-120">region DefaultParameters Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44527-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44527-121">-Location</span><span class="sxs-lookup"><span data-stu-id="44527-121">-Location</span></span>
<span data-ttu-id="44527-122">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="44527-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="44527-123">-Master</span><span class="sxs-lookup"><span data-stu-id="44527-123">-Master</span></span>
<span data-ttu-id="44527-124">Das Quellserverobjekt, von dem wiederherstellen werden soll.</span><span class="sxs-lookup"><span data-stu-id="44527-124">The source server object to restore from.</span></span>
<span data-ttu-id="44527-125">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="44527-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44527-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="44527-126">-MasterName</span></span>
<span data-ttu-id="44527-127">MariaDB-Servername.</span><span class="sxs-lookup"><span data-stu-id="44527-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="44527-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="44527-128">-NoWait</span></span>
<span data-ttu-id="44527-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="44527-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="44527-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="44527-130">-ReplicaName</span></span>
<span data-ttu-id="44527-131">Name des Replikats.</span><span class="sxs-lookup"><span data-stu-id="44527-131">Replica name.</span></span>

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

### <span data-ttu-id="44527-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44527-132">-ResourceGroupName</span></span>
<span data-ttu-id="44527-133">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="44527-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="44527-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="44527-134">-Sku</span></span>
<span data-ttu-id="44527-135">Der Name der Sku ist in der Regel Ebene + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="44527-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="44527-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44527-136">-SubscriptionId</span></span>
<span data-ttu-id="44527-137">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="44527-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="44527-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="44527-138">-Tag</span></span>
<span data-ttu-id="44527-139">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="44527-139">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44527-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44527-140">-Confirm</span></span>
<span data-ttu-id="44527-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44527-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44527-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44527-142">-WhatIf</span></span>
<span data-ttu-id="44527-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44527-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44527-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44527-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44527-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44527-145">CommonParameters</span></span>
<span data-ttu-id="44527-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44527-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44527-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44527-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44527-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="44527-148">INPUTS</span></span>

### <span data-ttu-id="44527-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="44527-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="44527-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="44527-150">OUTPUTS</span></span>

### <span data-ttu-id="44527-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="44527-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="44527-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="44527-152">NOTES</span></span>

<span data-ttu-id="44527-153">ALIASE</span><span class="sxs-lookup"><span data-stu-id="44527-153">ALIASES</span></span>

<span data-ttu-id="44527-154">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="44527-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44527-155">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="44527-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44527-156">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44527-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44527-157">MASTER: <IServer> Das Quellserverobjekt, von dem wiederherstellen werden soll.</span><span class="sxs-lookup"><span data-stu-id="44527-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="44527-158">`Location <String>`: Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="44527-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="44527-159">`[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="44527-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="44527-160">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="44527-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="44527-161">`[AdministratorLogin <String>]`: Der Anmeldename eines Servers des Administrators.</span><span class="sxs-lookup"><span data-stu-id="44527-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="44527-162">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="44527-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="44527-163">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="44527-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="44527-164">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="44527-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="44527-165">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="44527-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="44527-166">Legen Sie dies auf "SystemAssigned" festgelegt, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="44527-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="44527-167">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="44527-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="44527-168">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="44527-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="44527-169">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="44527-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="44527-170">`[SkuCapacity <Int32?>]`: Die skalierungs-/out-Kapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="44527-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="44527-171">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="44527-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="44527-172">`[SkuName <String>]`: Der Name der Sku , in der Regel, Ebene + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="44527-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="44527-173">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="44527-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="44527-174">`[SkuTier <SkuTier?>]`: Die Ebene der jeweiligen SKU, z. B. Basic.</span><span class="sxs-lookup"><span data-stu-id="44527-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="44527-175">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="44527-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="44527-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="44527-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="44527-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="44527-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="44527-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Automatisches Wachstum" für Speicher.</span><span class="sxs-lookup"><span data-stu-id="44527-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="44527-179">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="44527-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="44527-180">`[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="44527-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="44527-181">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="44527-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="44527-182">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="44527-182">RELATED LINKS</span></span>

