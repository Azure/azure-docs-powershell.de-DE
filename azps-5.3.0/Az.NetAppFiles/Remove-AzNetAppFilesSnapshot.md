---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380609"
---
# <span data-ttu-id="a6fca-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6fca-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="a6fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6fca-102">SYNOPSIS</span></span>
<span data-ttu-id="a6fca-103">Löscht eine Azure NetApp Files (ANF)-Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="a6fca-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="a6fca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6fca-104">SYNTAX</span></span>

### <span data-ttu-id="a6fca-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6fca-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6fca-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6fca-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6fca-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6fca-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6fca-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6fca-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6fca-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6fca-109">DESCRIPTION</span></span>
<span data-ttu-id="a6fca-110">Das **Cmdlet "Remove-AzNetAppFilesSnapshot"** löscht eine ANF-Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="a6fca-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="a6fca-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a6fca-111">EXAMPLES</span></span>

### <span data-ttu-id="a6fca-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6fca-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="a6fca-113">Mit diesem Befehl wird der ANF-Snapshot "MyAnfSnapshot" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a6fca-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="a6fca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6fca-114">PARAMETERS</span></span>

### <span data-ttu-id="a6fca-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6fca-115">-AccountName</span></span>
<span data-ttu-id="a6fca-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="a6fca-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="a6fca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6fca-117">-DefaultProfile</span></span>
<span data-ttu-id="a6fca-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6fca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6fca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6fca-119">-InputObject</span></span>
<span data-ttu-id="a6fca-120">Das zu entfernende Momentaufnahmeobjekt</span><span class="sxs-lookup"><span data-stu-id="a6fca-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6fca-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a6fca-121">-Name</span></span>
<span data-ttu-id="a6fca-122">Der Name der ANF-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="a6fca-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6fca-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6fca-123">-PassThru</span></span>
<span data-ttu-id="a6fca-124">Rückgabe, ob das angegebene Volume erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="a6fca-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="a6fca-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a6fca-125">-PoolName</span></span>
<span data-ttu-id="a6fca-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="a6fca-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a6fca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6fca-127">-ResourceGroupName</span></span>
<span data-ttu-id="a6fca-128">Die Ressourcengruppe der ANF-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="a6fca-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="a6fca-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6fca-129">-ResourceId</span></span>
<span data-ttu-id="a6fca-130">Die Ressourcen-ID der ANF-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="a6fca-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="a6fca-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="a6fca-131">-VolumeName</span></span>
<span data-ttu-id="a6fca-132">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="a6fca-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="a6fca-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="a6fca-133">-VolumeObject</span></span>
<span data-ttu-id="a6fca-134">Das Volumenobjekt mit der zu entfernenden Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="a6fca-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6fca-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6fca-135">-Confirm</span></span>
<span data-ttu-id="a6fca-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6fca-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6fca-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a6fca-137">-WhatIf</span></span>
<span data-ttu-id="a6fca-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6fca-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6fca-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6fca-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6fca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6fca-140">CommonParameters</span></span>
<span data-ttu-id="a6fca-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6fca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6fca-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6fca-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6fca-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a6fca-143">INPUTS</span></span>

### <span data-ttu-id="a6fca-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a6fca-144">System.String</span></span>

### <span data-ttu-id="a6fca-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a6fca-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="a6fca-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="a6fca-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="a6fca-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a6fca-147">OUTPUTS</span></span>

### <span data-ttu-id="a6fca-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6fca-148">System.Boolean</span></span>

## <span data-ttu-id="a6fca-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a6fca-149">NOTES</span></span>

## <span data-ttu-id="a6fca-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a6fca-150">RELATED LINKS</span></span>
