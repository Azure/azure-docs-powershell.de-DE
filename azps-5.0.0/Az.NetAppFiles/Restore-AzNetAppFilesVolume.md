---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 486bd44d3f48213fde6fb9b6c1d15a5683c1fd82
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178590"
---
# <span data-ttu-id="55145-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="55145-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="55145-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55145-102">SYNOPSIS</span></span>
<span data-ttu-id="55145-103">Wiederherstellen/Zurücksetzen eines Volumes auf einen seiner Snapshots</span><span class="sxs-lookup"><span data-stu-id="55145-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="55145-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55145-104">SYNTAX</span></span>

### <span data-ttu-id="55145-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="55145-105">ByFieldsParameterSet (Default)</span></span>
```
Revert-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55145-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55145-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55145-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55145-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55145-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55145-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55145-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55145-109">DESCRIPTION</span></span>
<span data-ttu-id="55145-110">Wiederherstellen/Zurücksetzen eines Volumes auf die im Snapshot-Parameter angegebene Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="55145-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="55145-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55145-111">EXAMPLES</span></span>

### <span data-ttu-id="55145-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55145-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="55145-113">Mit diesem Befehl wird die Lautstärke "myvolume" wieder in einen der Snapshots des 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="55145-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="55145-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="55145-114">PARAMETERS</span></span>

### <span data-ttu-id="55145-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="55145-115">-AccountName</span></span>
<span data-ttu-id="55145-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="55145-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55145-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55145-117">-DefaultProfile</span></span>
<span data-ttu-id="55145-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55145-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55145-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="55145-119">-InputObject</span></span>
<span data-ttu-id="55145-120">Das zu entfernende Volume-Objekt</span><span class="sxs-lookup"><span data-stu-id="55145-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55145-121">-Name</span><span class="sxs-lookup"><span data-stu-id="55145-121">-Name</span></span>
<span data-ttu-id="55145-122">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="55145-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55145-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55145-123">-PassThru</span></span>
<span data-ttu-id="55145-124">Gibt zurück, ob das angegebene Volume erfolgreich wiederhergestellt/zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="55145-124">Return whether the specified volume was successfully restored/reverted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55145-125">-Poolname</span><span class="sxs-lookup"><span data-stu-id="55145-125">-PoolName</span></span>
<span data-ttu-id="55145-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="55145-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55145-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="55145-127">-PoolObject</span></span>
<span data-ttu-id="55145-128">Das Pool-Objekt, das das zu entfernende Volume enthält</span><span class="sxs-lookup"><span data-stu-id="55145-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55145-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55145-129">-ResourceGroupName</span></span>
<span data-ttu-id="55145-130">Die Ressourcengruppe des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="55145-130">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55145-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="55145-131">-ResourceId</span></span>
<span data-ttu-id="55145-132">Die Ressourcen-ID des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="55145-132">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55145-133">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="55145-133">-SnapshotId</span></span>
<span data-ttu-id="55145-134">Snapshot-Nr des Schnappschusses.</span><span class="sxs-lookup"><span data-stu-id="55145-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="55145-135">UUID V4, mit der der Snapshot identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="55145-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55145-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55145-136">-Confirm</span></span>
<span data-ttu-id="55145-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55145-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55145-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55145-138">-WhatIf</span></span>
<span data-ttu-id="55145-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55145-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55145-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55145-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55145-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55145-141">CommonParameters</span></span>
<span data-ttu-id="55145-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55145-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55145-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55145-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55145-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55145-144">INPUTS</span></span>

### <span data-ttu-id="55145-145">System. String</span><span class="sxs-lookup"><span data-stu-id="55145-145">System.String</span></span>

### <span data-ttu-id="55145-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="55145-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="55145-147">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="55145-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="55145-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55145-148">OUTPUTS</span></span>

### <span data-ttu-id="55145-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55145-149">System.Boolean</span></span>

## <span data-ttu-id="55145-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="55145-150">NOTES</span></span>

## <span data-ttu-id="55145-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55145-151">RELATED LINKS</span></span>
