---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380580"
---
# <span data-ttu-id="d78a5-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d78a5-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="d78a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d78a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d78a5-103">Löscht ein Azure NetApp Files (ANF)-Volume.</span><span class="sxs-lookup"><span data-stu-id="d78a5-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="d78a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d78a5-104">SYNTAX</span></span>

### <span data-ttu-id="d78a5-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d78a5-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d78a5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d78a5-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d78a5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d78a5-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d78a5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d78a5-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d78a5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d78a5-109">DESCRIPTION</span></span>
<span data-ttu-id="d78a5-110">Das **Cmdlet "Remove-AzNetAppFilesVolume"** löscht ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="d78a5-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="d78a5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d78a5-111">EXAMPLES</span></span>

### <span data-ttu-id="d78a5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d78a5-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="d78a5-113">Mit diesem Befehl wird das ANF-Volume "MyAnfVolume" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d78a5-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="d78a5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d78a5-114">PARAMETERS</span></span>

### <span data-ttu-id="d78a5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d78a5-115">-AccountName</span></span>
<span data-ttu-id="d78a5-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="d78a5-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="d78a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d78a5-117">-DefaultProfile</span></span>
<span data-ttu-id="d78a5-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d78a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d78a5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d78a5-119">-InputObject</span></span>
<span data-ttu-id="d78a5-120">Das zu entfernende Volumenobjekt</span><span class="sxs-lookup"><span data-stu-id="d78a5-120">The volume object to remove</span></span>

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

### <span data-ttu-id="d78a5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d78a5-121">-Name</span></span>
<span data-ttu-id="d78a5-122">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="d78a5-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="d78a5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d78a5-123">-PassThru</span></span>
<span data-ttu-id="d78a5-124">Rückgabe, ob das angegebene Volume erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="d78a5-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="d78a5-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d78a5-125">-PoolName</span></span>
<span data-ttu-id="d78a5-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="d78a5-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d78a5-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="d78a5-127">-PoolObject</span></span>
<span data-ttu-id="d78a5-128">Das Poolobjekt mit dem zu entfernenden Volume</span><span class="sxs-lookup"><span data-stu-id="d78a5-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="d78a5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d78a5-129">-ResourceGroupName</span></span>
<span data-ttu-id="d78a5-130">Die Ressourcengruppe des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="d78a5-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="d78a5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d78a5-131">-ResourceId</span></span>
<span data-ttu-id="d78a5-132">Die Ressourcen-ID des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="d78a5-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="d78a5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d78a5-133">-Confirm</span></span>
<span data-ttu-id="d78a5-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d78a5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d78a5-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d78a5-135">-WhatIf</span></span>
<span data-ttu-id="d78a5-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d78a5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d78a5-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d78a5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d78a5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78a5-138">CommonParameters</span></span>
<span data-ttu-id="d78a5-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d78a5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78a5-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d78a5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d78a5-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d78a5-141">INPUTS</span></span>

### <span data-ttu-id="d78a5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d78a5-142">System.String</span></span>

### <span data-ttu-id="d78a5-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d78a5-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="d78a5-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d78a5-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d78a5-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d78a5-145">OUTPUTS</span></span>

### <span data-ttu-id="d78a5-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d78a5-146">System.Boolean</span></span>

## <span data-ttu-id="d78a5-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d78a5-147">NOTES</span></span>

## <span data-ttu-id="d78a5-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d78a5-148">RELATED LINKS</span></span>
