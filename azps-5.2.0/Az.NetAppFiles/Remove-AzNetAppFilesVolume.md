---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361106"
---
# <span data-ttu-id="cfa30-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="cfa30-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="cfa30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfa30-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa30-103">Löscht ein Azure NetApp Files (ANF)-Volume.</span><span class="sxs-lookup"><span data-stu-id="cfa30-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="cfa30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfa30-104">SYNTAX</span></span>

### <span data-ttu-id="cfa30-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cfa30-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa30-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa30-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa30-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa30-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa30-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfa30-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfa30-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfa30-109">DESCRIPTION</span></span>
<span data-ttu-id="cfa30-110">Das **Cmdlet "Remove-AzNetAppFilesVolume"** löscht ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="cfa30-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="cfa30-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cfa30-111">EXAMPLES</span></span>

### <span data-ttu-id="cfa30-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfa30-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="cfa30-113">Mit diesem Befehl wird das ANF-Volume "MyAnfVolume" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cfa30-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="cfa30-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfa30-114">PARAMETERS</span></span>

### <span data-ttu-id="cfa30-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cfa30-115">-AccountName</span></span>
<span data-ttu-id="cfa30-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="cfa30-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="cfa30-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa30-117">-DefaultProfile</span></span>
<span data-ttu-id="cfa30-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cfa30-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfa30-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfa30-119">-InputObject</span></span>
<span data-ttu-id="cfa30-120">Das zu entfernende Volumenobjekt</span><span class="sxs-lookup"><span data-stu-id="cfa30-120">The volume object to remove</span></span>

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

### <span data-ttu-id="cfa30-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cfa30-121">-Name</span></span>
<span data-ttu-id="cfa30-122">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="cfa30-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="cfa30-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfa30-123">-PassThru</span></span>
<span data-ttu-id="cfa30-124">Rückgabe, ob das angegebene Volume erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="cfa30-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="cfa30-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="cfa30-125">-PoolName</span></span>
<span data-ttu-id="cfa30-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="cfa30-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="cfa30-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="cfa30-127">-PoolObject</span></span>
<span data-ttu-id="cfa30-128">Das Poolobjekt mit dem zu entfernenden Volume</span><span class="sxs-lookup"><span data-stu-id="cfa30-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="cfa30-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfa30-129">-ResourceGroupName</span></span>
<span data-ttu-id="cfa30-130">Die Ressourcengruppe des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="cfa30-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="cfa30-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa30-131">-ResourceId</span></span>
<span data-ttu-id="cfa30-132">Die Ressourcen-ID des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="cfa30-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="cfa30-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfa30-133">-Confirm</span></span>
<span data-ttu-id="cfa30-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cfa30-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfa30-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cfa30-135">-WhatIf</span></span>
<span data-ttu-id="cfa30-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cfa30-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfa30-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfa30-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfa30-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa30-138">CommonParameters</span></span>
<span data-ttu-id="cfa30-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa30-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa30-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfa30-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa30-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cfa30-141">INPUTS</span></span>

### <span data-ttu-id="cfa30-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cfa30-142">System.String</span></span>

### <span data-ttu-id="cfa30-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="cfa30-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="cfa30-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="cfa30-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="cfa30-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cfa30-145">OUTPUTS</span></span>

### <span data-ttu-id="cfa30-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cfa30-146">System.Boolean</span></span>

## <span data-ttu-id="cfa30-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cfa30-147">NOTES</span></span>

## <span data-ttu-id="cfa30-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cfa30-148">RELATED LINKS</span></span>
