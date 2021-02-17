---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147249"
---
# <span data-ttu-id="64afd-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="64afd-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="64afd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64afd-102">SYNOPSIS</span></span>
<span data-ttu-id="64afd-103">Erstellt ein neues Azure NetApp Files (ANF)-Volume.</span><span class="sxs-lookup"><span data-stu-id="64afd-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="64afd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64afd-104">SYNTAX</span></span>

### <span data-ttu-id="64afd-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="64afd-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64afd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64afd-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64afd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64afd-107">DESCRIPTION</span></span>
<span data-ttu-id="64afd-108">Das **Cmdlet "New-AzNetAppFilesVolume"** erstellt ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="64afd-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="64afd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64afd-109">EXAMPLES</span></span>

### <span data-ttu-id="64afd-110">Beispiel 1: Erstellen eines ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="64afd-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="64afd-111">Mit diesem Befehl wird das neue ANF-Volume "MyAnfVolume" im Pool "MyAnfPool" erstellt.</span><span class="sxs-lookup"><span data-stu-id="64afd-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="64afd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64afd-112">PARAMETERS</span></span>

### <span data-ttu-id="64afd-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="64afd-113">-AccountName</span></span>
<span data-ttu-id="64afd-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="64afd-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="64afd-115">-Sicherung</span><span class="sxs-lookup"><span data-stu-id="64afd-115">-Backup</span></span>
<span data-ttu-id="64afd-116">Hashtablearray, das das Sicherungsobjekt darstellt</span><span class="sxs-lookup"><span data-stu-id="64afd-116">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="64afd-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="64afd-117">-BackupId</span></span>
<span data-ttu-id="64afd-118">Sicherungs-ID.</span><span class="sxs-lookup"><span data-stu-id="64afd-118">Backup ID.</span></span> <span data-ttu-id="64afd-119">UUID v4 oder Ressourcenbezeichner, mit dem die Sicherung identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="64afd-119">UUID v4 or resource identifier used to identify the Backup</span></span>

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

### <span data-ttu-id="64afd-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="64afd-120">-CreationToken</span></span>
<span data-ttu-id="64afd-121">Ein eindeutiger Dateipfad für das Volume</span><span class="sxs-lookup"><span data-stu-id="64afd-121">A unique file path for the volume</span></span>

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

### <span data-ttu-id="64afd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64afd-122">-DefaultProfile</span></span>
<span data-ttu-id="64afd-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64afd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64afd-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="64afd-124">-ExportPolicy</span></span>
<span data-ttu-id="64afd-125">Hashtablearray, das die Exportrichtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="64afd-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="64afd-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="64afd-126">-KerberosEnabled</span></span>
<span data-ttu-id="64afd-127">Beschreiben, ob ein Volume Kerberos enabled ist</span><span class="sxs-lookup"><span data-stu-id="64afd-127">Describe if a volume is Kerberos Enabled</span></span>

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

### <span data-ttu-id="64afd-128">-Location</span><span class="sxs-lookup"><span data-stu-id="64afd-128">-Location</span></span>
<span data-ttu-id="64afd-129">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="64afd-129">The location of the resource</span></span>

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

### <span data-ttu-id="64afd-130">-Name</span><span class="sxs-lookup"><span data-stu-id="64afd-130">-Name</span></span>
<span data-ttu-id="64afd-131">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="64afd-131">The name of the ANF volume</span></span>

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

### <span data-ttu-id="64afd-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="64afd-132">-PoolName</span></span>
<span data-ttu-id="64afd-133">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="64afd-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="64afd-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="64afd-134">-PoolObject</span></span>
<span data-ttu-id="64afd-135">Der Pool für das neue Volumenobjekt</span><span class="sxs-lookup"><span data-stu-id="64afd-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="64afd-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="64afd-136">-ProtocolType</span></span>
<span data-ttu-id="64afd-137">Hashtablearray, das die Exportrichtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="64afd-137">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="64afd-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="64afd-138">-ReplicationObject</span></span>
<span data-ttu-id="64afd-139">Hashtablearray, das das Replikationsobjekt darstellt</span><span class="sxs-lookup"><span data-stu-id="64afd-139">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="64afd-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64afd-140">-ResourceGroupName</span></span>
<span data-ttu-id="64afd-141">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="64afd-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="64afd-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="64afd-142">-SecurityStyle</span></span>
<span data-ttu-id="64afd-143">Der Sicherheitsstil des Volumens.</span><span class="sxs-lookup"><span data-stu-id="64afd-143">The security style of volume.</span></span> <span data-ttu-id="64afd-144">Mögliche Werte sind: 'ntfs', 'unix'</span><span class="sxs-lookup"><span data-stu-id="64afd-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="64afd-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="64afd-145">-ServiceLevel</span></span>
<span data-ttu-id="64afd-146">Der Servicelevel des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="64afd-146">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="64afd-147">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="64afd-147">-Snapshot</span></span>
<span data-ttu-id="64afd-148">Hashtablearray, das das Momentaufnahmeobjekt darstellt</span><span class="sxs-lookup"><span data-stu-id="64afd-148">A hashtable array which represents the snapshot object</span></span>

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

### <span data-ttu-id="64afd-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="64afd-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="64afd-150">Wenn die Option (true) aktiviert ist, enthält das Volume ein schreibgeschütztes Snapshotverzeichnis, das Zugriff auf die Momentaufnahmen des Volumes bietet (Standardeinstellung "true").</span><span class="sxs-lookup"><span data-stu-id="64afd-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

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

### <span data-ttu-id="64afd-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="64afd-151">-SnapshotId</span></span>
<span data-ttu-id="64afd-152">Erstellen Sie Volumen aus einer Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="64afd-152">Create volume from a snapshot.</span></span> <span data-ttu-id="64afd-153">UUID v4 oder Ressourcenbezeichner zum Identifizieren der Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="64afd-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="64afd-154">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="64afd-154">-SubnetId</span></span>
<span data-ttu-id="64afd-155">Der Azure-Ressourcen-URI für ein delegiertes Subnetz</span><span class="sxs-lookup"><span data-stu-id="64afd-155">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="64afd-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="64afd-156">-Tag</span></span>
<span data-ttu-id="64afd-157">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="64afd-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="64afd-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="64afd-158">-ThroughputMibps</span></span>
<span data-ttu-id="64afd-159">Maximaler Durchsatz in Mibps, der mit diesem Volume erzielt werden kann</span><span class="sxs-lookup"><span data-stu-id="64afd-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="64afd-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="64afd-160">-UsageThreshold</span></span>
<span data-ttu-id="64afd-161">Das für ein Dateisystem zulässige maximale Speicherkontingent in Byte</span><span class="sxs-lookup"><span data-stu-id="64afd-161">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="64afd-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="64afd-162">-VolumeType</span></span>
<span data-ttu-id="64afd-163">Der Typ der ANF-Lautstärke</span><span class="sxs-lookup"><span data-stu-id="64afd-163">The type of the ANF volume</span></span>

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

### <span data-ttu-id="64afd-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64afd-164">-Confirm</span></span>
<span data-ttu-id="64afd-165">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64afd-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64afd-166">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="64afd-166">-WhatIf</span></span>
<span data-ttu-id="64afd-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64afd-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64afd-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64afd-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64afd-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64afd-169">CommonParameters</span></span>
<span data-ttu-id="64afd-170">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64afd-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64afd-171">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64afd-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64afd-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64afd-172">INPUTS</span></span>

### <span data-ttu-id="64afd-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="64afd-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="64afd-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64afd-174">OUTPUTS</span></span>

### <span data-ttu-id="64afd-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="64afd-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="64afd-176">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="64afd-176">NOTES</span></span>

## <span data-ttu-id="64afd-177">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="64afd-177">RELATED LINKS</span></span>
