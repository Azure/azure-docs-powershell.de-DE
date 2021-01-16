---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 2d3b212ea24c9dda665d2e2ec2516f25a59318b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295385"
---
# <span data-ttu-id="fd335-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="fd335-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="fd335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd335-102">SYNOPSIS</span></span>
<span data-ttu-id="fd335-103">Aktualisiert ein Azure NetApp Files (ANF)-Volume entsprechend den bereitgestellten optionalen Modifizierern.</span><span class="sxs-lookup"><span data-stu-id="fd335-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="fd335-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd335-104">SYNTAX</span></span>

### <span data-ttu-id="fd335-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd335-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd335-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd335-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd335-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd335-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd335-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd335-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd335-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd335-109">DESCRIPTION</span></span>
<span data-ttu-id="fd335-110">Das **Cmdlet "Update-AzNetAppFilesVolume"** aktualisiert ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="fd335-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="fd335-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd335-111">EXAMPLES</span></span>

### <span data-ttu-id="fd335-112">Beispiel 1: Aktualisieren eines ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="fd335-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="fd335-113">Mit diesem Befehl wird das ANF-Volume "MyAnfVolume" mit der neuen Größe "UsageThreshold" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fd335-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="fd335-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd335-114">PARAMETERS</span></span>

### <span data-ttu-id="fd335-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd335-115">-AccountName</span></span>
<span data-ttu-id="fd335-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="fd335-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="fd335-117">-Sicherung</span><span class="sxs-lookup"><span data-stu-id="fd335-117">-Backup</span></span>
<span data-ttu-id="fd335-118">Hashtablearray, das das Sicherungsobjekt darstellt</span><span class="sxs-lookup"><span data-stu-id="fd335-118">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="fd335-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd335-119">-DefaultProfile</span></span>
<span data-ttu-id="fd335-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd335-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd335-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="fd335-121">-ExportPolicy</span></span>
<span data-ttu-id="fd335-122">Hashtablearray, das die Exportrichtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="fd335-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="fd335-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd335-123">-InputObject</span></span>
<span data-ttu-id="fd335-124">Das zu aktualisierende Volumenobjekt</span><span class="sxs-lookup"><span data-stu-id="fd335-124">The volume object to update</span></span>

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

### <span data-ttu-id="fd335-125">-Location</span><span class="sxs-lookup"><span data-stu-id="fd335-125">-Location</span></span>
<span data-ttu-id="fd335-126">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="fd335-126">The location of the resource</span></span>

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

### <span data-ttu-id="fd335-127">-Name</span><span class="sxs-lookup"><span data-stu-id="fd335-127">-Name</span></span>
<span data-ttu-id="fd335-128">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="fd335-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="fd335-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="fd335-129">-PoolName</span></span>
<span data-ttu-id="fd335-130">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="fd335-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="fd335-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="fd335-131">-PoolObject</span></span>
<span data-ttu-id="fd335-132">Das Poolobjekt mit dem zu aktualisierenden Volume</span><span class="sxs-lookup"><span data-stu-id="fd335-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="fd335-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd335-133">-ResourceGroupName</span></span>
<span data-ttu-id="fd335-134">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="fd335-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="fd335-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd335-135">-ResourceId</span></span>
<span data-ttu-id="fd335-136">Die Ressourcen-ID des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="fd335-136">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="fd335-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="fd335-137">-ServiceLevel</span></span>
<span data-ttu-id="fd335-138">Der Servicelevel des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="fd335-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="fd335-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd335-139">-Tag</span></span>
<span data-ttu-id="fd335-140">Eine Hashtable, die Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="fd335-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="fd335-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="fd335-141">-ThroughputMibps</span></span>
<span data-ttu-id="fd335-142">Maximaler Durchsatz in Mibps, der mit diesem Volume erzielt werden kann</span><span class="sxs-lookup"><span data-stu-id="fd335-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="fd335-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="fd335-143">-UsageThreshold</span></span>
<span data-ttu-id="fd335-144">Das für ein Dateisystem zulässige maximale Speicherkontingent in Byte</span><span class="sxs-lookup"><span data-stu-id="fd335-144">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="fd335-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd335-145">-Confirm</span></span>
<span data-ttu-id="fd335-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd335-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd335-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fd335-147">-WhatIf</span></span>
<span data-ttu-id="fd335-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd335-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd335-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd335-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd335-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd335-150">CommonParameters</span></span>
<span data-ttu-id="fd335-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd335-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd335-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd335-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd335-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd335-153">INPUTS</span></span>

### <span data-ttu-id="fd335-154">System.String</span><span class="sxs-lookup"><span data-stu-id="fd335-154">System.String</span></span>

### <span data-ttu-id="fd335-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="fd335-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="fd335-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="fd335-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="fd335-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd335-157">OUTPUTS</span></span>

### <span data-ttu-id="fd335-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="fd335-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="fd335-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd335-159">NOTES</span></span>

## <span data-ttu-id="fd335-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd335-160">RELATED LINKS</span></span>
