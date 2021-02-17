---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152361"
---
# <span data-ttu-id="23f14-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="23f14-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="23f14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23f14-102">SYNOPSIS</span></span>
<span data-ttu-id="23f14-103">Erstellt eine Replikat eines MariaDB-Servers.</span><span class="sxs-lookup"><span data-stu-id="23f14-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="23f14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23f14-104">SYNTAX</span></span>

### <span data-ttu-id="23f14-105">Servername (Standard)</span><span class="sxs-lookup"><span data-stu-id="23f14-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="23f14-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="23f14-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="23f14-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23f14-107">DESCRIPTION</span></span>
<span data-ttu-id="23f14-108">Erstellt eine Replikat eines MariaDB-Servers.</span><span class="sxs-lookup"><span data-stu-id="23f14-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="23f14-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23f14-109">EXAMPLES</span></span>

### <span data-ttu-id="23f14-110">Beispiel 1: Erstellen eines Replikat-DB für eine MariaDB</span><span class="sxs-lookup"><span data-stu-id="23f14-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="23f14-111">Mit diesem Befehl wird ein Replikat-DB für eine MariaDB erstellt.</span><span class="sxs-lookup"><span data-stu-id="23f14-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="23f14-112">Beispiel 2: Erstellen eines Replikat-DB für eine MariaDB</span><span class="sxs-lookup"><span data-stu-id="23f14-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="23f14-113">Mit diesem Befehl wird ein Replikat-DB für eine MariaDB erstellt.</span><span class="sxs-lookup"><span data-stu-id="23f14-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="23f14-114">Beispiel 3: Erstellen eines Replikat-DB für eine MariaDB</span><span class="sxs-lookup"><span data-stu-id="23f14-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="23f14-115">Dieser Befehl mit Parametereingabeobjekt erstellt einen Replikat-DB mit Parametereingabeobjekt für eine MariaDB.</span><span class="sxs-lookup"><span data-stu-id="23f14-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="23f14-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23f14-116">PARAMETERS</span></span>

### <span data-ttu-id="23f14-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23f14-117">-AsJob</span></span>
<span data-ttu-id="23f14-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="23f14-118">Run the command as a job</span></span>

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

### <span data-ttu-id="23f14-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f14-119">-DefaultProfile</span></span>
<span data-ttu-id="23f14-120">region DefaultParameters Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23f14-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23f14-121">-Location</span><span class="sxs-lookup"><span data-stu-id="23f14-121">-Location</span></span>
<span data-ttu-id="23f14-122">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="23f14-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="23f14-123">-Master</span><span class="sxs-lookup"><span data-stu-id="23f14-123">-Master</span></span>
<span data-ttu-id="23f14-124">Das Quellserverobjekt, aus dem sie wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="23f14-124">The source server object to restore from.</span></span>
<span data-ttu-id="23f14-125">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="23f14-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="23f14-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="23f14-126">-MasterName</span></span>
<span data-ttu-id="23f14-127">MariaDB-Servername.</span><span class="sxs-lookup"><span data-stu-id="23f14-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="23f14-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="23f14-128">-NoWait</span></span>
<span data-ttu-id="23f14-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="23f14-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="23f14-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="23f14-130">-ReplicaName</span></span>
<span data-ttu-id="23f14-131">Replikatname.</span><span class="sxs-lookup"><span data-stu-id="23f14-131">Replica name.</span></span>

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

### <span data-ttu-id="23f14-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f14-132">-ResourceGroupName</span></span>
<span data-ttu-id="23f14-133">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="23f14-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="23f14-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="23f14-134">-Sku</span></span>
<span data-ttu-id="23f14-135">Der Name der SKU , normalerweise Stufen + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="23f14-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="23f14-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23f14-136">-SubscriptionId</span></span>
<span data-ttu-id="23f14-137">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="23f14-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="23f14-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="23f14-138">-Tag</span></span>
<span data-ttu-id="23f14-139">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="23f14-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="23f14-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23f14-140">-Confirm</span></span>
<span data-ttu-id="23f14-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23f14-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f14-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="23f14-142">-WhatIf</span></span>
<span data-ttu-id="23f14-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23f14-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f14-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23f14-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f14-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f14-145">CommonParameters</span></span>
<span data-ttu-id="23f14-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f14-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f14-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23f14-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f14-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23f14-148">INPUTS</span></span>

### <span data-ttu-id="23f14-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="23f14-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="23f14-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23f14-150">OUTPUTS</span></span>

### <span data-ttu-id="23f14-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="23f14-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="23f14-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="23f14-152">NOTES</span></span>

<span data-ttu-id="23f14-153">ALIASE</span><span class="sxs-lookup"><span data-stu-id="23f14-153">ALIASES</span></span>

<span data-ttu-id="23f14-154">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="23f14-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23f14-155">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="23f14-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23f14-156">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23f14-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23f14-157">MASTER: <IServer> Das Quellserverobjekt, aus dem sie wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="23f14-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="23f14-158">`Location <String>`: Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="23f14-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="23f14-159">`[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="23f14-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="23f14-160">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="23f14-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="23f14-161">`[AdministratorLogin <String>]`: Der Anmeldename eines Servers des Administrators.</span><span class="sxs-lookup"><span data-stu-id="23f14-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="23f14-162">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="23f14-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="23f14-163">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="23f14-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="23f14-164">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="23f14-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="23f14-165">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="23f14-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="23f14-166">Legen Sie diesen Wert auf "SystemAssigned" ein, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="23f14-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="23f14-167">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="23f14-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="23f14-168">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="23f14-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="23f14-169">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="23f14-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="23f14-170">`[SkuCapacity <Int32?>]`: Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="23f14-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="23f14-171">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="23f14-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="23f14-172">`[SkuName <String>]`: Der Name der SKU, in der Regel Stufe + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="23f14-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="23f14-173">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="23f14-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="23f14-174">`[SkuTier <SkuTier?>]`: Die Ebene einer bestimmten SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="23f14-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="23f14-175">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="23f14-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="23f14-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="23f14-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="23f14-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="23f14-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="23f14-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Speicher automatisch anwachsen".</span><span class="sxs-lookup"><span data-stu-id="23f14-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="23f14-179">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="23f14-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="23f14-180">`[UserVisibleState <ServerState?>]`: Der Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="23f14-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="23f14-181">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="23f14-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="23f14-182">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="23f14-182">RELATED LINKS</span></span>

