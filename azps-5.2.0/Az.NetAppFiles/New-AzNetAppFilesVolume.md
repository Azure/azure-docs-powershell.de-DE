---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359902"
---
# <span data-ttu-id="fcbe8-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="fcbe8-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="fcbe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcbe8-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbe8-103">Erstellt ein neues Azure NetApp Files (ANF)-Volume.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="fcbe8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcbe8-104">SYNTAX</span></span>

### <span data-ttu-id="fcbe8-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcbe8-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcbe8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcbe8-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcbe8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcbe8-107">DESCRIPTION</span></span>
<span data-ttu-id="fcbe8-108">Das **Cmdlet "New-AzNetAppFilesVolume"** erstellt ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="fcbe8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fcbe8-109">EXAMPLES</span></span>

### <span data-ttu-id="fcbe8-110">Beispiel 1: Erstellen eines ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="fcbe8-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="fcbe8-111">Mit diesem Befehl wird das neue ANF-Volume "MyAnfVolume" im Pool "MyAnfPool" erstellt.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="fcbe8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcbe8-112">PARAMETERS</span></span>

### <span data-ttu-id="fcbe8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fcbe8-113">-AccountName</span></span>
<span data-ttu-id="fcbe8-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="fcbe8-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-115">-Sicherung</span><span class="sxs-lookup"><span data-stu-id="fcbe8-115">-Backup</span></span>
<span data-ttu-id="fcbe8-116">Hashtablearray, das das Sicherungsobjekt darstellt</span><span class="sxs-lookup"><span data-stu-id="fcbe8-116">A hashtable array which represents the backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeBackupProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="fcbe8-117">-BackupId</span></span>
<span data-ttu-id="fcbe8-118">Sicherungs-ID.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-118">Backup ID.</span></span> <span data-ttu-id="fcbe8-119">UUID v4 oder Ressourcenbezeichner, mit dem die Sicherung identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="fcbe8-119">UUID v4 or resource identifier used to identify the Backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="fcbe8-120">-CreationToken</span></span>
<span data-ttu-id="fcbe8-121">Ein eindeutiger Dateipfad für das Volume</span><span class="sxs-lookup"><span data-stu-id="fcbe8-121">A unique file path for the volume</span></span>

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

### <span data-ttu-id="fcbe8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbe8-122">-DefaultProfile</span></span>
<span data-ttu-id="fcbe8-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="fcbe8-124">-ExportPolicy</span></span>
<span data-ttu-id="fcbe8-125">Hashtablearray, das die Exportrichtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="fcbe8-125">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="fcbe8-126">-KerberosEnabled</span></span>
<span data-ttu-id="fcbe8-127">Beschreiben, ob ein Volume Kerberos enabled ist</span><span class="sxs-lookup"><span data-stu-id="fcbe8-127">Describe if a volume is Kerberos Enabled</span></span>

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

### <span data-ttu-id="fcbe8-128">-Location</span><span class="sxs-lookup"><span data-stu-id="fcbe8-128">-Location</span></span>
<span data-ttu-id="fcbe8-129">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="fcbe8-129">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-130">-Name</span><span class="sxs-lookup"><span data-stu-id="fcbe8-130">-Name</span></span>
<span data-ttu-id="fcbe8-131">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="fcbe8-131">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="fcbe8-132">-PoolName</span></span>
<span data-ttu-id="fcbe8-133">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="fcbe8-133">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="fcbe8-134">-PoolObject</span></span>
<span data-ttu-id="fcbe8-135">Der Pool für das neue Volumenobjekt</span><span class="sxs-lookup"><span data-stu-id="fcbe8-135">The pool for the new volume object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="fcbe8-136">-ProtocolType</span></span>
<span data-ttu-id="fcbe8-137">Hashtablearray, das die Exportrichtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="fcbe8-137">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="fcbe8-138">-ReplicationObject</span></span>
<span data-ttu-id="fcbe8-139">Hashtablearray, das das Replikationsobjekt darstellt</span><span class="sxs-lookup"><span data-stu-id="fcbe8-139">A hashtable array which represents the replication object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcbe8-140">-ResourceGroupName</span></span>
<span data-ttu-id="fcbe8-141">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="fcbe8-141">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="fcbe8-142">-SecurityStyle</span></span>
<span data-ttu-id="fcbe8-143">Der Sicherheitsstil des Volumens.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-143">The security style of volume.</span></span> <span data-ttu-id="fcbe8-144">Mögliche Werte sind: 'ntfs', 'unix'</span><span class="sxs-lookup"><span data-stu-id="fcbe8-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="fcbe8-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="fcbe8-145">-ServiceLevel</span></span>
<span data-ttu-id="fcbe8-146">Der Servicelevel des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="fcbe8-146">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="fcbe8-147">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="fcbe8-147">-Snapshot</span></span>
<span data-ttu-id="fcbe8-148">Hashtablearray, das das Momentaufnahmeobjekt darstellt</span><span class="sxs-lookup"><span data-stu-id="fcbe8-148">A hashtable array which represents the snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeSnapshot
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="fcbe8-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="fcbe8-150">Wenn das Volume aktiviert (true) ist, enthält es ein schreibgeschütztes Snapshotverzeichnis, das Zugriff auf die Momentaufnahmen des Volumes bietet (Standardwert: TRUE).</span><span class="sxs-lookup"><span data-stu-id="fcbe8-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

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

### <span data-ttu-id="fcbe8-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="fcbe8-151">-SnapshotId</span></span>
<span data-ttu-id="fcbe8-152">Erstellen Sie Volumen aus einer Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-152">Create volume from a snapshot.</span></span> <span data-ttu-id="fcbe8-153">UUID v4 oder Ressourcenbezeichner zum Identifizieren der Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="fcbe8-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-154">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fcbe8-154">-SubnetId</span></span>
<span data-ttu-id="fcbe8-155">Der Azure-Ressourcen-URI für ein delegiertes Subnetz</span><span class="sxs-lookup"><span data-stu-id="fcbe8-155">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="fcbe8-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="fcbe8-156">-Tag</span></span>
<span data-ttu-id="fcbe8-157">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="fcbe8-157">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="fcbe8-158">-ThroughputMibps</span></span>
<span data-ttu-id="fcbe8-159">Maximaler Durchsatz in Mibps, der mit diesem Volume erzielt werden kann</span><span class="sxs-lookup"><span data-stu-id="fcbe8-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="fcbe8-160">-UsageThreshold</span></span>
<span data-ttu-id="fcbe8-161">Das für ein Dateisystem zulässige maximale Speicherkontingent in Byte</span><span class="sxs-lookup"><span data-stu-id="fcbe8-161">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="fcbe8-162">-VolumeType</span></span>
<span data-ttu-id="fcbe8-163">Der Typ der ANF-Lautstärke</span><span class="sxs-lookup"><span data-stu-id="fcbe8-163">The type of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbe8-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcbe8-164">-Confirm</span></span>
<span data-ttu-id="fcbe8-165">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcbe8-166">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fcbe8-166">-WhatIf</span></span>
<span data-ttu-id="fcbe8-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcbe8-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcbe8-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbe8-169">CommonParameters</span></span>
<span data-ttu-id="fcbe8-170">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcbe8-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbe8-171">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcbe8-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbe8-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fcbe8-172">INPUTS</span></span>

### <span data-ttu-id="fcbe8-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="fcbe8-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="fcbe8-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fcbe8-174">OUTPUTS</span></span>

### <span data-ttu-id="fcbe8-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="fcbe8-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="fcbe8-176">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fcbe8-176">NOTES</span></span>

## <span data-ttu-id="fcbe8-177">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fcbe8-177">RELATED LINKS</span></span>
