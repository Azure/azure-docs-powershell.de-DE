---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: a9b0d3565e2266373d3ba553be94ffd8a24707d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174389"
---
# <span data-ttu-id="f219c-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f219c-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="f219c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f219c-102">SYNOPSIS</span></span>
<span data-ttu-id="f219c-103">Entfernt einen vorhandenen Trigger auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="f219c-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="f219c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f219c-104">SYNTAX</span></span>

### <span data-ttu-id="f219c-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f219c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f219c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f219c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f219c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f219c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f219c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f219c-108">DESCRIPTION</span></span>
<span data-ttu-id="f219c-109">Das Cmdlet " **Remove-AzDataBoxEdgeTrigger** " entfernt einen vorhandenen Trigger auf dem Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="f219c-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="f219c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f219c-110">EXAMPLES</span></span>

### <span data-ttu-id="f219c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f219c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="f219c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f219c-112">PARAMETERS</span></span>

### <span data-ttu-id="f219c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f219c-113">-AsJob</span></span>
<span data-ttu-id="f219c-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f219c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f219c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f219c-115">-DefaultProfile</span></span>
<span data-ttu-id="f219c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f219c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f219c-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f219c-117">-DeviceName</span></span>
<span data-ttu-id="f219c-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="f219c-118">Device Name</span></span>

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

### <span data-ttu-id="f219c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f219c-119">-InputObject</span></span>
<span data-ttu-id="f219c-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f219c-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f219c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f219c-121">-Name</span></span>
<span data-ttu-id="f219c-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="f219c-122">Resource Name</span></span>

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

### <span data-ttu-id="f219c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f219c-123">-PassThru</span></span>
<span data-ttu-id="f219c-124">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="f219c-124">returns true if successful</span></span>

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

### <span data-ttu-id="f219c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f219c-125">-ResourceGroupName</span></span>
<span data-ttu-id="f219c-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f219c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f219c-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f219c-127">-ResourceId</span></span>
<span data-ttu-id="f219c-128">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="f219c-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="f219c-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f219c-129">-Confirm</span></span>
<span data-ttu-id="f219c-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f219c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f219c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f219c-131">-WhatIf</span></span>
<span data-ttu-id="f219c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f219c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f219c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f219c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f219c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f219c-134">CommonParameters</span></span>
<span data-ttu-id="f219c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f219c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f219c-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f219c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f219c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f219c-137">INPUTS</span></span>

### <span data-ttu-id="f219c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f219c-138">System.String</span></span>

### <span data-ttu-id="f219c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f219c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="f219c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f219c-140">OUTPUTS</span></span>

### <span data-ttu-id="f219c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f219c-141">System.Boolean</span></span>

## <span data-ttu-id="f219c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="f219c-142">NOTES</span></span>

## <span data-ttu-id="f219c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f219c-143">RELATED LINKS</span></span>
