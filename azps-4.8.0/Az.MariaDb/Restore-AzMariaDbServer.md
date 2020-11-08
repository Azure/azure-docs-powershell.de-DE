---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009758"
---
# <span data-ttu-id="baf86-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="baf86-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="baf86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="baf86-102">SYNOPSIS</span></span>
<span data-ttu-id="baf86-103">Wiederherstellen eines MariaDB aus einem vorhandenen MariaDB</span><span class="sxs-lookup"><span data-stu-id="baf86-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="baf86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="baf86-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="baf86-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="baf86-105">DESCRIPTION</span></span>
<span data-ttu-id="baf86-106">Wiederherstellen eines MariaDB aus einem vorhandenen MariaDB</span><span class="sxs-lookup"><span data-stu-id="baf86-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="baf86-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="baf86-107">EXAMPLES</span></span>

### <span data-ttu-id="baf86-108">Beispiel 1: Wiederherstellen einer PointInTime-MariaDB nach dem Servernamen.</span><span class="sxs-lookup"><span data-stu-id="baf86-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="baf86-109">Mit diesem Befehl wird eine PointInTime-MariaDB nach dem Servernamen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="baf86-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="baf86-110">Beispiel 2: Wiederherstellen eines PointInTime-MariaDB nach Serverobjekt</span><span class="sxs-lookup"><span data-stu-id="baf86-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="baf86-111">Mit diesem Befehl wird ein PointInTime-MariaDB nach Serverobjekt wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="baf86-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="baf86-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="baf86-112">PARAMETERS</span></span>

### <span data-ttu-id="baf86-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baf86-113">-AsJob</span></span>
<span data-ttu-id="baf86-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="baf86-114">Run the command as a job</span></span>

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

### <span data-ttu-id="baf86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf86-115">-DefaultProfile</span></span>
<span data-ttu-id="baf86-116">Region DefaultParameters die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="baf86-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baf86-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="baf86-117">-InputObject</span></span>
<span data-ttu-id="baf86-118">Das Quellserver Objekt, von dem wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="baf86-118">The source server object to restore from.</span></span>
<span data-ttu-id="baf86-119">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="baf86-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="baf86-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="baf86-120">-Location</span></span>
<span data-ttu-id="baf86-121">Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="baf86-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="baf86-122">-Name</span><span class="sxs-lookup"><span data-stu-id="baf86-122">-Name</span></span>
<span data-ttu-id="baf86-123">Der Servername des dest, von dem wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="baf86-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="baf86-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="baf86-124">-NoWait</span></span>
<span data-ttu-id="baf86-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="baf86-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="baf86-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf86-126">-ResourceGroupName</span></span>
<span data-ttu-id="baf86-127">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="baf86-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="baf86-128">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="baf86-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="baf86-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="baf86-129">-RestorePointInTime</span></span>
<span data-ttu-id="baf86-130">Region PointInTimeRestore des Standorts, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="baf86-130">region PointInTimeRestore The location the resource resides in.</span></span>

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

### <span data-ttu-id="baf86-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="baf86-131">-ServerName</span></span>
<span data-ttu-id="baf86-132">Der Name des Quellservers, von dem wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="baf86-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="baf86-133">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="baf86-133">-SubscriptionId</span></span>
<span data-ttu-id="baf86-134">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="baf86-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="baf86-135">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="baf86-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="baf86-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="baf86-136">-Tag</span></span>
<span data-ttu-id="baf86-137">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="baf86-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="baf86-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="baf86-138">-Confirm</span></span>
<span data-ttu-id="baf86-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="baf86-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf86-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf86-140">-WhatIf</span></span>
<span data-ttu-id="baf86-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="baf86-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baf86-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="baf86-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baf86-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf86-143">CommonParameters</span></span>
<span data-ttu-id="baf86-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf86-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf86-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baf86-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf86-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="baf86-146">INPUTS</span></span>

### <span data-ttu-id="baf86-147">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="baf86-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="baf86-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="baf86-148">OUTPUTS</span></span>

### <span data-ttu-id="baf86-149">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="baf86-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="baf86-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="baf86-150">NOTES</span></span>

<span data-ttu-id="baf86-151">Aliase</span><span class="sxs-lookup"><span data-stu-id="baf86-151">ALIASES</span></span>

<span data-ttu-id="baf86-152">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="baf86-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="baf86-153">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="baf86-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="baf86-154">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="baf86-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="baf86-155">Inputobject <IServer> : das Quellserver Objekt, von dem wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="baf86-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="baf86-156">`Location <String>`: Der Speicherort, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="baf86-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="baf86-157">`[Tag <ITrackedResourceTags>]`: Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="baf86-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="baf86-158">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="baf86-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="baf86-159">`[AdministratorLogin <String>]`: Der Anmeldename des Administrators auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="baf86-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="baf86-160">Kann nur angegeben werden, wenn der Server erstellt wird (und für die Erstellung erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="baf86-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="baf86-161">`[EarliestRestoreDate <DateTime?>]`: Frühester Erstellungszeitpunkt des Wiederherstellungspunkts (ISO8601-Format)</span><span class="sxs-lookup"><span data-stu-id="baf86-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="baf86-162">`[FullyQualifiedDomainName <String>]`: Der vollqualifizierte Domänenname eines Servers.</span><span class="sxs-lookup"><span data-stu-id="baf86-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="baf86-163">`[IdentityType <IdentityType?>]`: Der Identity-Typ.</span><span class="sxs-lookup"><span data-stu-id="baf86-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="baf86-164">Legen Sie diesen Wert auf "SystemAssigned", um automatisch einen Azure Active Directory-Prinzipal für die Ressource zu erstellen und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="baf86-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="baf86-165">`[MasterServerId <String>]`: Die Masterserver-ID eines Replikatservers.</span><span class="sxs-lookup"><span data-stu-id="baf86-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="baf86-166">`[ReplicaCapacity <Int32?>]`: Die maximale Anzahl von Replikaten, die ein Masterserver aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="baf86-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="baf86-167">`[ReplicationRole <String>]`: Die Replikations Rolle des Servers.</span><span class="sxs-lookup"><span data-stu-id="baf86-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="baf86-168">`[SkuCapacity <Int32?>]`: Die Skalierungskapazität, die die Compute-Einheiten des Servers repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="baf86-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="baf86-169">`[SkuFamily <String>]`: Die Hardwarefamilie.</span><span class="sxs-lookup"><span data-stu-id="baf86-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="baf86-170">`[SkuName <String>]`: Der Name der SKU, in der Regel Tier + Familie + Kerne, beispielsweise B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="baf86-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="baf86-171">`[SkuSize <String>]`: Der Größencode, der von der Ressource entsprechend interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="baf86-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="baf86-172">`[SkuTier <SkuTier?>]`: Die Stufe der jeweiligen SKU, z.b. Basic.</span><span class="sxs-lookup"><span data-stu-id="baf86-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="baf86-173">`[SslEnforcement <SslEnforcementEnum?>]`: Aktivieren der SSL-Erzwingung oder nicht, wenn eine Verbindung mit dem Server hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="baf86-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="baf86-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup-Aufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="baf86-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="baf86-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Aktivieren Sie Geo-redundante oder nicht für Server-Backups.</span><span class="sxs-lookup"><span data-stu-id="baf86-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="baf86-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Aktivieren der automatischen Vergrößerung von Speicher.</span><span class="sxs-lookup"><span data-stu-id="baf86-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="baf86-177">`[StorageProfileStorageMb <Int32?>]`: Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="baf86-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="baf86-178">`[UserVisibleState <ServerState?>]`: Ein Zustand eines Servers, der für den Benutzer sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="baf86-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="baf86-179">`[Version <ServerVersion?>]`: Server Version.</span><span class="sxs-lookup"><span data-stu-id="baf86-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="baf86-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="baf86-180">RELATED LINKS</span></span>

