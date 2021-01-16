---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 6606de1a5d4de6df6ecafa700ac1b93d31399b43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289343"
---
# <span data-ttu-id="7a3f4-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7a3f4-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="7a3f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="7a3f4-103">Wiederherstellen/Zurücksetzen eines Volumes auf einen seiner Momentaufnahmen</span><span class="sxs-lookup"><span data-stu-id="7a3f4-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="7a3f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a3f4-104">SYNTAX</span></span>

### <span data-ttu-id="7a3f4-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a3f4-105">ByFieldsParameterSet (Default)</span></span>
```
Restore-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a3f4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a3f4-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a3f4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a3f4-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a3f4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a3f4-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a3f4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a3f4-109">DESCRIPTION</span></span>
<span data-ttu-id="7a3f4-110">Wiederherstellen/Zurücksetzen eines Volumens auf die Momentaufnahme, die im Absatz "SnapshotId" angegeben ist</span><span class="sxs-lookup"><span data-stu-id="7a3f4-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="7a3f4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a3f4-111">EXAMPLES</span></span>

### <span data-ttu-id="7a3f4-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a3f4-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="7a3f4-113">Mit diesem Befehl wird das Volumen von MyVolume mit der snapshotId von 7d6e4069-6c78-6c61-7bf6-c60968e45fbf wiederhergestellt/zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7a3f4-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="7a3f4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a3f4-114">PARAMETERS</span></span>

### <span data-ttu-id="7a3f4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a3f4-115">-AccountName</span></span>
<span data-ttu-id="7a3f4-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="7a3f4-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="7a3f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a3f4-117">-DefaultProfile</span></span>
<span data-ttu-id="7a3f4-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a3f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a3f4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a3f4-119">-InputObject</span></span>
<span data-ttu-id="7a3f4-120">Das zu entfernende Volumenobjekt</span><span class="sxs-lookup"><span data-stu-id="7a3f4-120">The volume object to remove</span></span>

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

### <span data-ttu-id="7a3f4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7a3f4-121">-Name</span></span>
<span data-ttu-id="7a3f4-122">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="7a3f4-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="7a3f4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a3f4-123">-PassThru</span></span>
<span data-ttu-id="7a3f4-124">Zurückgeben, ob das angegebene Volume erfolgreich wiederhergestellt/wiederhergestellt wurde</span><span class="sxs-lookup"><span data-stu-id="7a3f4-124">Return whether the specified volume was successfully restored/reverted</span></span>

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

### <span data-ttu-id="7a3f4-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7a3f4-125">-PoolName</span></span>
<span data-ttu-id="7a3f4-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="7a3f4-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="7a3f4-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="7a3f4-127">-PoolObject</span></span>
<span data-ttu-id="7a3f4-128">Das Poolobjekt mit dem zu entfernenden Volume</span><span class="sxs-lookup"><span data-stu-id="7a3f4-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="7a3f4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a3f4-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a3f4-130">Die Ressourcengruppe des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="7a3f4-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="7a3f4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a3f4-131">-ResourceId</span></span>
<span data-ttu-id="7a3f4-132">Die Ressourcen-ID des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="7a3f4-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="7a3f4-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="7a3f4-133">-SnapshotId</span></span>
<span data-ttu-id="7a3f4-134">SnapshotId der Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="7a3f4-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="7a3f4-135">UUID v4 zum Identifizieren der Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="7a3f4-135">UUID v4 used to identify the Snapshot</span></span>

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

### <span data-ttu-id="7a3f4-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a3f4-136">-Confirm</span></span>
<span data-ttu-id="7a3f4-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a3f4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a3f4-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7a3f4-138">-WhatIf</span></span>
<span data-ttu-id="7a3f4-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a3f4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a3f4-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a3f4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a3f4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a3f4-141">CommonParameters</span></span>
<span data-ttu-id="7a3f4-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a3f4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a3f4-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a3f4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a3f4-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a3f4-144">INPUTS</span></span>

### <span data-ttu-id="7a3f4-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7a3f4-145">System.String</span></span>

### <span data-ttu-id="7a3f4-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7a3f4-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="7a3f4-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7a3f4-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7a3f4-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a3f4-148">OUTPUTS</span></span>

### <span data-ttu-id="7a3f4-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a3f4-149">System.Boolean</span></span>

## <span data-ttu-id="7a3f4-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a3f4-150">NOTES</span></span>

## <span data-ttu-id="7a3f4-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a3f4-151">RELATED LINKS</span></span>
