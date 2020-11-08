---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac3282d8249eecbb6e8c7bd1fb23a5ab0f55ed95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004779"
---
# <span data-ttu-id="4d0a8-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="4d0a8-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="4d0a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="4d0a8-103">Entfernt eine Freigabe vom Gerät.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-103">Removes a share from the device.</span></span>

## <span data-ttu-id="4d0a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d0a8-104">SYNTAX</span></span>

### <span data-ttu-id="4d0a8-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d0a8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d0a8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d0a8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d0a8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d0a8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d0a8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d0a8-108">DESCRIPTION</span></span>
<span data-ttu-id="4d0a8-109">Das Cmdlet **Remove-AzDataBoxEdgeEdgeShare** entfernt die zugehörigen Edge-Freigaben für ein Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="4d0a8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d0a8-110">EXAMPLES</span></span>

### <span data-ttu-id="4d0a8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d0a8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="4d0a8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d0a8-112">PARAMETERS</span></span>

### <span data-ttu-id="4d0a8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d0a8-113">-AsJob</span></span>
<span data-ttu-id="4d0a8-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4d0a8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d0a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d0a8-115">-DefaultProfile</span></span>
<span data-ttu-id="4d0a8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d0a8-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4d0a8-117">-DeviceName</span></span>
<span data-ttu-id="4d0a8-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="4d0a8-118">Device Name</span></span>

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

### <span data-ttu-id="4d0a8-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4d0a8-119">-InputObject</span></span>
<span data-ttu-id="4d0a8-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="4d0a8-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d0a8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4d0a8-121">-Name</span></span>
<span data-ttu-id="4d0a8-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="4d0a8-122">Resource Name</span></span>

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

### <span data-ttu-id="4d0a8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d0a8-123">-PassThru</span></span>
<span data-ttu-id="4d0a8-124">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="4d0a8-124">returns true if successful</span></span>

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

### <span data-ttu-id="4d0a8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d0a8-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d0a8-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="4d0a8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4d0a8-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4d0a8-127">-ResourceId</span></span>
<span data-ttu-id="4d0a8-128">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="4d0a8-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="4d0a8-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d0a8-129">-Confirm</span></span>
<span data-ttu-id="4d0a8-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d0a8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d0a8-131">-WhatIf</span></span>
<span data-ttu-id="4d0a8-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d0a8-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d0a8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d0a8-134">CommonParameters</span></span>
<span data-ttu-id="4d0a8-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d0a8-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d0a8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d0a8-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d0a8-137">INPUTS</span></span>

### <span data-ttu-id="4d0a8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4d0a8-138">System.String</span></span>

### <span data-ttu-id="4d0a8-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="4d0a8-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="4d0a8-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d0a8-140">OUTPUTS</span></span>

### <span data-ttu-id="4d0a8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d0a8-141">System.Boolean</span></span>

## <span data-ttu-id="4d0a8-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d0a8-142">NOTES</span></span>

## <span data-ttu-id="4d0a8-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d0a8-143">RELATED LINKS</span></span>
