---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: dce91ee25cac4a716dc604e38f1ac38e5a3f3f1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178595"
---
# <span data-ttu-id="91573-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="91573-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="91573-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91573-102">SYNOPSIS</span></span>
<span data-ttu-id="91573-103">Erstellt ein neues Azure NetApp-Dateien (ANF)-Volume.</span><span class="sxs-lookup"><span data-stu-id="91573-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="91573-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91573-104">SYNTAX</span></span>

### <span data-ttu-id="91573-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="91573-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91573-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91573-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91573-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91573-107">DESCRIPTION</span></span>
<span data-ttu-id="91573-108">Das Cmdlet **New-AzNetAppFilesVolume** erstellt ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="91573-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="91573-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91573-109">EXAMPLES</span></span>

### <span data-ttu-id="91573-110">Beispiel 1: Erstellen eines ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="91573-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="91573-111">Dieser Befehl erstellt das neue ANF-Volumen "MyAnfVolume" innerhalb des Pools "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="91573-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="91573-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="91573-112">PARAMETERS</span></span>

### <span data-ttu-id="91573-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="91573-113">-AccountName</span></span>
<span data-ttu-id="91573-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="91573-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="91573-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="91573-115">-CreationToken</span></span>
<span data-ttu-id="91573-116">Ein eindeutiger Dateipfad für das Volume</span><span class="sxs-lookup"><span data-stu-id="91573-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="91573-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91573-117">-DefaultProfile</span></span>
<span data-ttu-id="91573-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91573-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91573-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="91573-119">-ExportPolicy</span></span>
<span data-ttu-id="91573-120">Ein Hashtable-Array, das die Export Richtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="91573-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="91573-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="91573-121">-Location</span></span>
<span data-ttu-id="91573-122">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="91573-122">The location of the resource</span></span>

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

### <span data-ttu-id="91573-123">-Name</span><span class="sxs-lookup"><span data-stu-id="91573-123">-Name</span></span>
<span data-ttu-id="91573-124">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="91573-124">The name of the ANF volume</span></span>

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

### <span data-ttu-id="91573-125">-Poolname</span><span class="sxs-lookup"><span data-stu-id="91573-125">-PoolName</span></span>
<span data-ttu-id="91573-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="91573-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="91573-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="91573-127">-PoolObject</span></span>
<span data-ttu-id="91573-128">Der Pool für das neue Volumen Objekt</span><span class="sxs-lookup"><span data-stu-id="91573-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="91573-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="91573-129">-ProtocolType</span></span>
<span data-ttu-id="91573-130">Ein Hashtable-Array, das die Export Richtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="91573-130">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="91573-131">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="91573-131">-ReplicationObject</span></span>
<span data-ttu-id="91573-132">Ein Hashtable-Array, das das Replication-Objekt darstellt</span><span class="sxs-lookup"><span data-stu-id="91573-132">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="91573-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91573-133">-ResourceGroupName</span></span>
<span data-ttu-id="91573-134">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="91573-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="91573-135">-Service Level</span><span class="sxs-lookup"><span data-stu-id="91573-135">-ServiceLevel</span></span>
<span data-ttu-id="91573-136">Die Dienstebene des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="91573-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="91573-137">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="91573-137">-SnapshotId</span></span>
<span data-ttu-id="91573-138">Erstellen eines Volumes aus einer Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="91573-138">Create volume from a snapshot.</span></span> <span data-ttu-id="91573-139">UUID v4 oder Ressourcen-ID, mit der der Snapshot identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="91573-139">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="91573-140">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="91573-140">-SubnetId</span></span>
<span data-ttu-id="91573-141">Der Azure-Ressourcen-URI für ein delegiertes Subnetz</span><span class="sxs-lookup"><span data-stu-id="91573-141">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="91573-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="91573-142">-Tag</span></span>
<span data-ttu-id="91573-143">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="91573-143">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="91573-144">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="91573-144">-UsageThreshold</span></span>
<span data-ttu-id="91573-145">Das maximal zulässige Speicherkontingent für ein Dateisystem in Byte</span><span class="sxs-lookup"><span data-stu-id="91573-145">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="91573-146">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="91573-146">-VolumeType</span></span>
<span data-ttu-id="91573-147">Der Typ des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="91573-147">The type of the ANF volume</span></span>

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

### <span data-ttu-id="91573-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91573-148">-Confirm</span></span>
<span data-ttu-id="91573-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91573-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91573-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91573-150">-WhatIf</span></span>
<span data-ttu-id="91573-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91573-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91573-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91573-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91573-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91573-153">CommonParameters</span></span>
<span data-ttu-id="91573-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91573-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91573-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91573-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91573-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91573-156">INPUTS</span></span>

### <span data-ttu-id="91573-157">System. String</span><span class="sxs-lookup"><span data-stu-id="91573-157">System.String</span></span>

### <span data-ttu-id="91573-158">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="91573-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="91573-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91573-159">OUTPUTS</span></span>

### <span data-ttu-id="91573-160">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="91573-160">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="91573-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="91573-161">NOTES</span></span>

## <span data-ttu-id="91573-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91573-162">RELATED LINKS</span></span>
