---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 8c977c61f332ccdc927dd3f0e070d635e6095acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934235"
---
# <span data-ttu-id="01464-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="01464-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="01464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01464-102">SYNOPSIS</span></span>
<span data-ttu-id="01464-103">Entfernt einen Benutzer auf einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="01464-103">Removes a user on a device.</span></span>

## <span data-ttu-id="01464-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01464-104">SYNTAX</span></span>

### <span data-ttu-id="01464-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="01464-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01464-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01464-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01464-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01464-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01464-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01464-108">DESCRIPTION</span></span>
<span data-ttu-id="01464-109">Das **Cmdlet Remove-AzDataBoxEdgeUser** entfernt einen Benutzer auf dem Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="01464-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="01464-110">Die Erstellung von nur Benutzern vom Typ `Share` wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01464-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="01464-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01464-111">EXAMPLES</span></span>

### <span data-ttu-id="01464-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01464-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="01464-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="01464-113">PARAMETERS</span></span>

### <span data-ttu-id="01464-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01464-114">-AsJob</span></span>
<span data-ttu-id="01464-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="01464-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01464-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01464-116">-DefaultProfile</span></span>
<span data-ttu-id="01464-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01464-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01464-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="01464-118">-DeviceName</span></span>
<span data-ttu-id="01464-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="01464-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01464-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01464-120">-InputObject</span></span>
<span data-ttu-id="01464-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="01464-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01464-122">-Name</span><span class="sxs-lookup"><span data-stu-id="01464-122">-Name</span></span>
<span data-ttu-id="01464-123">Benutzername</span><span class="sxs-lookup"><span data-stu-id="01464-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01464-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01464-124">-PassThru</span></span>
<span data-ttu-id="01464-125">gibt "true" zurück, wenn dies erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="01464-125">returns true if successful</span></span>

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

### <span data-ttu-id="01464-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01464-126">-ResourceGroupName</span></span>
<span data-ttu-id="01464-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="01464-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01464-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01464-128">-ResourceId</span></span>
<span data-ttu-id="01464-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="01464-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01464-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01464-130">-Confirm</span></span>
<span data-ttu-id="01464-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01464-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01464-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01464-132">-WhatIf</span></span>
<span data-ttu-id="01464-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01464-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01464-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01464-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01464-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01464-135">CommonParameters</span></span>
<span data-ttu-id="01464-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01464-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01464-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01464-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01464-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01464-138">INPUTS</span></span>

### <span data-ttu-id="01464-139">System.String</span><span class="sxs-lookup"><span data-stu-id="01464-139">System.String</span></span>

### <span data-ttu-id="01464-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="01464-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="01464-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01464-141">OUTPUTS</span></span>

### <span data-ttu-id="01464-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="01464-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="01464-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="01464-143">NOTES</span></span>

## <span data-ttu-id="01464-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="01464-144">RELATED LINKS</span></span>
