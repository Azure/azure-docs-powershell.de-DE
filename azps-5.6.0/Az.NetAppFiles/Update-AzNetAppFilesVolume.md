---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: b7947f4224c667ed8332b0f3206588dda49fd1af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926651"
---
# <span data-ttu-id="d4b73-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d4b73-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="d4b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4b73-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b73-103">Aktualisiert ein Azure NetApp Files (ANF)-Volume entsprechend den optionalen bereitgestellten Modifizierern.</span><span class="sxs-lookup"><span data-stu-id="d4b73-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="d4b73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4b73-104">SYNTAX</span></span>

### <span data-ttu-id="d4b73-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4b73-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4b73-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b73-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b73-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b73-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b73-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4b73-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4b73-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4b73-109">DESCRIPTION</span></span>
<span data-ttu-id="d4b73-110">Das **Cmdlet Update-AzNetAppFilesVolume** aktualisiert ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="d4b73-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="d4b73-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4b73-111">EXAMPLES</span></span>

### <span data-ttu-id="d4b73-112">Beispiel 1: Aktualisieren eines ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="d4b73-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="d4b73-113">Mit diesem Befehl wird das ANF-Volume "MyAnfVolume" mit der neuen UsageThreshold-Größe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d4b73-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="d4b73-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d4b73-114">PARAMETERS</span></span>

### <span data-ttu-id="d4b73-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d4b73-115">-AccountName</span></span>
<span data-ttu-id="d4b73-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="d4b73-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="d4b73-117">-Sicherung</span><span class="sxs-lookup"><span data-stu-id="d4b73-117">-Backup</span></span>
<span data-ttu-id="d4b73-118">Ein Hashtablearray, das das Sicherungsobjekt darstellt</span><span class="sxs-lookup"><span data-stu-id="d4b73-118">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="d4b73-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b73-119">-DefaultProfile</span></span>
<span data-ttu-id="d4b73-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4b73-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4b73-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="d4b73-121">-ExportPolicy</span></span>
<span data-ttu-id="d4b73-122">Ein Hashtablearray, das die Exportrichtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="d4b73-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="d4b73-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4b73-123">-InputObject</span></span>
<span data-ttu-id="d4b73-124">Das zu aktualisierende Volumenobjekt</span><span class="sxs-lookup"><span data-stu-id="d4b73-124">The volume object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b73-125">-Location</span><span class="sxs-lookup"><span data-stu-id="d4b73-125">-Location</span></span>
<span data-ttu-id="d4b73-126">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="d4b73-126">The location of the resource</span></span>

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

### <span data-ttu-id="d4b73-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d4b73-127">-Name</span></span>
<span data-ttu-id="d4b73-128">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="d4b73-128">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b73-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d4b73-129">-PoolName</span></span>
<span data-ttu-id="d4b73-130">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="d4b73-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d4b73-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="d4b73-131">-PoolObject</span></span>
<span data-ttu-id="d4b73-132">Das Poolobjekt, das das zu aktualisierende Volume enthält</span><span class="sxs-lookup"><span data-stu-id="d4b73-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="d4b73-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4b73-133">-ResourceGroupName</span></span>
<span data-ttu-id="d4b73-134">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="d4b73-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d4b73-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4b73-135">-ResourceId</span></span>
<span data-ttu-id="d4b73-136">Die Ressourcen-ID des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="d4b73-136">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b73-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="d4b73-137">-ServiceLevel</span></span>
<span data-ttu-id="d4b73-138">Die Dienstebene des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="d4b73-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="d4b73-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4b73-139">-Tag</span></span>
<span data-ttu-id="d4b73-140">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="d4b73-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d4b73-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="d4b73-141">-ThroughputMibps</span></span>
<span data-ttu-id="d4b73-142">Maximaler Durchsatz in Mibps, der mit diesem Volume erzielt werden kann</span><span class="sxs-lookup"><span data-stu-id="d4b73-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="d4b73-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="d4b73-143">-UsageThreshold</span></span>
<span data-ttu-id="d4b73-144">Das maximal zulässige Speicherkontingent für ein Dateisystem in Bytes</span><span class="sxs-lookup"><span data-stu-id="d4b73-144">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b73-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4b73-145">-Confirm</span></span>
<span data-ttu-id="d4b73-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4b73-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4b73-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4b73-147">-WhatIf</span></span>
<span data-ttu-id="d4b73-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4b73-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4b73-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4b73-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4b73-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b73-150">CommonParameters</span></span>
<span data-ttu-id="d4b73-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4b73-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b73-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4b73-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b73-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4b73-153">INPUTS</span></span>

### <span data-ttu-id="d4b73-154">System.String</span><span class="sxs-lookup"><span data-stu-id="d4b73-154">System.String</span></span>

### <span data-ttu-id="d4b73-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d4b73-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="d4b73-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d4b73-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d4b73-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4b73-157">OUTPUTS</span></span>

### <span data-ttu-id="d4b73-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d4b73-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d4b73-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d4b73-159">NOTES</span></span>

## <span data-ttu-id="d4b73-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d4b73-160">RELATED LINKS</span></span>
