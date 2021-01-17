---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360435"
---
# <span data-ttu-id="0d2d3-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="0d2d3-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="0d2d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2d3-103">Wiederherstellen einer MariaDB aus einer vorhandenen MariaDB</span><span class="sxs-lookup"><span data-stu-id="0d2d3-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="0d2d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d2d3-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d2d3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d2d3-105">DESCRIPTION</span></span>
<span data-ttu-id="0d2d3-106">Wiederherstellen einer MariaDB aus einer vorhandenen MariaDB</span><span class="sxs-lookup"><span data-stu-id="0d2d3-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="0d2d3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d2d3-107">EXAMPLES</span></span>

### <span data-ttu-id="0d2d3-108">Beispiel 1: Wiederherstellen einer PointInTime MariaDB nach Servername.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0d2d3-109">Mit diesem Befehl wird eine PointInTime MariaDB nach Servername wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="0d2d3-110">Beispiel 2: Wiederherstellen einer PointInTime MariaDB nach Serverobjekt</span><span class="sxs-lookup"><span data-stu-id="0d2d3-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0d2d3-111">Mit diesem Befehl wird eine PointInTime MariaDB nach Serverobjekt wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="0d2d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d2d3-112">PARAMETERS</span></span>

### <span data-ttu-id="0d2d3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d2d3-113">-AsJob</span></span>
<span data-ttu-id="0d2d3-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="0d2d3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0d2d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d2d3-115">-DefaultProfile</span></span>
<span data-ttu-id="0d2d3-116">region DefaultParameters Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d2d3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d2d3-117">-InputObject</span></span>
<span data-ttu-id="0d2d3-118">Das Quellserverobjekt, aus dem sie wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-118">The source server object to restore from.</span></span>
<span data-ttu-id="0d2d3-119">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d2d3-120">-Location</span><span class="sxs-lookup"><span data-stu-id="0d2d3-120">-Location</span></span>
<span data-ttu-id="0d2d3-121">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0d2d3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0d2d3-122">-Name</span></span>
<span data-ttu-id="0d2d3-123">Der dest-Servername, aus dem sie wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="0d2d3-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0d2d3-124">-NoWait</span></span>
<span data-ttu-id="0d2d3-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="0d2d3-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0d2d3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d2d3-126">-ResourceGroupName</span></span>
<span data-ttu-id="0d2d3-127">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0d2d3-128">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0d2d3-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="0d2d3-129">-RestorePointInTime</span></span>
<span data-ttu-id="0d2d3-130">Region PointInTimeRestore Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d2d3-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0d2d3-131">-ServerName</span></span>
<span data-ttu-id="0d2d3-132">Der Quellservername, aus dem sie wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="0d2d3-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d2d3-133">-SubscriptionId</span></span>
<span data-ttu-id="0d2d3-134">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0d2d3-135">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0d2d3-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="0d2d3-136">-Tag</span></span>
<span data-ttu-id="0d2d3-137">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="0d2d3-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d2d3-138">-Confirm</span></span>
<span data-ttu-id="0d2d3-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d2d3-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0d2d3-140">-WhatIf</span></span>
<span data-ttu-id="0d2d3-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d2d3-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d2d3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2d3-143">CommonParameters</span></span>
<span data-ttu-id="0d2d3-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2d3-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d2d3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2d3-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d2d3-146">INPUTS</span></span>

### <span data-ttu-id="0d2d3-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="0d2d3-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0d2d3-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d2d3-148">OUTPUTS</span></span>

### <span data-ttu-id="0d2d3-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="0d2d3-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="0d2d3-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0d2d3-150">NOTES</span></span>

<span data-ttu-id="0d2d3-151">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0d2d3-151">ALIASES</span></span>

<span data-ttu-id="0d2d3-152">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0d2d3-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d2d3-153">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d2d3-154">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d2d3-155">INPUTOBJECT <IServer> : Das Quellserverobjekt, aus dem Sie wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="0d2d3-156">`Location <String>`: Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="0d2d3-157">`[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="0d2d3-158">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0d2d3-159">`[AdministratorLogin <String>]`: Der Anmeldename eines Administrators für einen Server.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="0d2d3-160">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="0d2d3-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="0d2d3-161">`[EarliestRestoreDate <DateTime?>]`: Früheste Erstellungszeit des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="0d2d3-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="0d2d3-162">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="0d2d3-163">`[IdentityType <IdentityType?>]`: Der Identitätstyp.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="0d2d3-164">Legen Sie diesen Wert auf "SystemAssigned" ein, um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="0d2d3-165">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="0d2d3-166">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver haben kann.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="0d2d3-167">`[ReplicationRole <String>]`: Die Replikationsrolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="0d2d3-168">`[SkuCapacity <Int32?>]`: Die Skalierungs-/Outkapazität, die die Recheneinheiten des Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="0d2d3-169">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="0d2d3-170">`[SkuName <String>]`: Der Name der SKU, in der Regel Stufe + Familie + Kerne, z. B. B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="0d2d3-171">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="0d2d3-172">`[SkuTier <SkuTier?>]`: Die Ebene einer bestimmten SKU, z. B. "Standard".</span><span class="sxs-lookup"><span data-stu-id="0d2d3-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="0d2d3-173">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren Sie die Ssl-Erzwingung oder nicht, wenn Sie eine Verbindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="0d2d3-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="0d2d3-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie georedundant oder nicht für die Serversicherung.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="0d2d3-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren Sie "Speicher automatisch anwachsen".</span><span class="sxs-lookup"><span data-stu-id="0d2d3-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="0d2d3-177">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="0d2d3-178">`[UserVisibleState <ServerState?>]`: Der Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="0d2d3-179">`[Version <ServerVersion?>]`: Serverversion.</span><span class="sxs-lookup"><span data-stu-id="0d2d3-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="0d2d3-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0d2d3-180">RELATED LINKS</span></span>

