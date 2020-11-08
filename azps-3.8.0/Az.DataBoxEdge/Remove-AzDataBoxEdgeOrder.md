---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004778"
---
# <span data-ttu-id="ea6f4-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="ea6f4-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="ea6f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ea6f4-103">Entfernt die Reihenfolge für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-103">Removes the order for a device.</span></span>

## <span data-ttu-id="ea6f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea6f4-104">SYNTAX</span></span>

### <span data-ttu-id="ea6f4-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea6f4-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea6f4-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea6f4-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea6f4-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea6f4-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea6f4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea6f4-108">DESCRIPTION</span></span>
<span data-ttu-id="ea6f4-109">Das Cmdlet **Remove-AzDataBoxEdgeOrder** löscht eine vorhandene Reihenfolge für ein Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="ea6f4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea6f4-110">EXAMPLES</span></span>

### <span data-ttu-id="ea6f4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea6f4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="ea6f4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea6f4-112">PARAMETERS</span></span>

### <span data-ttu-id="ea6f4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea6f4-113">-AsJob</span></span>
<span data-ttu-id="ea6f4-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ea6f4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea6f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea6f4-115">-DefaultProfile</span></span>
<span data-ttu-id="ea6f4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea6f4-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ea6f4-117">-DeviceName</span></span>
<span data-ttu-id="ea6f4-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="ea6f4-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f4-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea6f4-119">-InputObject</span></span>
<span data-ttu-id="ea6f4-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="ea6f4-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea6f4-121">-PassThru</span></span>
<span data-ttu-id="ea6f4-122">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="ea6f4-122">returns true if successful</span></span>

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

### <span data-ttu-id="ea6f4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea6f4-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea6f4-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ea6f4-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f4-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ea6f4-125">-ResourceId</span></span>
<span data-ttu-id="ea6f4-126">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="ea6f4-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f4-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea6f4-127">-Confirm</span></span>
<span data-ttu-id="ea6f4-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea6f4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea6f4-129">-WhatIf</span></span>
<span data-ttu-id="ea6f4-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea6f4-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea6f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea6f4-132">CommonParameters</span></span>
<span data-ttu-id="ea6f4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea6f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea6f4-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea6f4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea6f4-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea6f4-135">INPUTS</span></span>

### <span data-ttu-id="ea6f4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ea6f4-136">System.String</span></span>

### <span data-ttu-id="ea6f4-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="ea6f4-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="ea6f4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea6f4-138">OUTPUTS</span></span>

### <span data-ttu-id="ea6f4-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="ea6f4-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="ea6f4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea6f4-140">NOTES</span></span>

## <span data-ttu-id="ea6f4-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea6f4-141">RELATED LINKS</span></span>
