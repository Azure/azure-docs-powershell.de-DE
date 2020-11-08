---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176382"
---
# <span data-ttu-id="8b3e3-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="8b3e3-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="8b3e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="8b3e3-103">Entfernt eine Freigabe vom Gerät.</span><span class="sxs-lookup"><span data-stu-id="8b3e3-103">Removes a share from the device.</span></span>

## <span data-ttu-id="8b3e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b3e3-104">SYNTAX</span></span>

### <span data-ttu-id="8b3e3-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b3e3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b3e3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b3e3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b3e3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b3e3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b3e3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b3e3-108">DESCRIPTION</span></span>
<span data-ttu-id="8b3e3-109">Das Cmdlet **Remove-AzStackEdgeEdgeShare** entfernt die zugehörigen Edge-Freigaben für ein Stack-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="8b3e3-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="8b3e3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b3e3-110">EXAMPLES</span></span>

### <span data-ttu-id="8b3e3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b3e3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="8b3e3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b3e3-112">PARAMETERS</span></span>

### <span data-ttu-id="8b3e3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b3e3-113">-AsJob</span></span>
<span data-ttu-id="8b3e3-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8b3e3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b3e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b3e3-115">-DefaultProfile</span></span>
<span data-ttu-id="8b3e3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b3e3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b3e3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8b3e3-117">-DeviceName</span></span>
<span data-ttu-id="8b3e3-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="8b3e3-118">Device Name</span></span>

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

### <span data-ttu-id="8b3e3-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8b3e3-119">-InputObject</span></span>
<span data-ttu-id="8b3e3-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="8b3e3-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b3e3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8b3e3-121">-Name</span></span>
<span data-ttu-id="8b3e3-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="8b3e3-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b3e3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b3e3-123">-PassThru</span></span>
<span data-ttu-id="8b3e3-124">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="8b3e3-124">returns true if successful</span></span>

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

### <span data-ttu-id="8b3e3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b3e3-125">-ResourceGroupName</span></span>
<span data-ttu-id="8b3e3-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8b3e3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8b3e3-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8b3e3-127">-ResourceId</span></span>
<span data-ttu-id="8b3e3-128">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="8b3e3-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="8b3e3-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b3e3-129">-Confirm</span></span>
<span data-ttu-id="8b3e3-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b3e3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b3e3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b3e3-131">-WhatIf</span></span>
<span data-ttu-id="8b3e3-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b3e3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b3e3-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b3e3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b3e3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b3e3-134">CommonParameters</span></span>
<span data-ttu-id="8b3e3-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b3e3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b3e3-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b3e3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b3e3-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b3e3-137">INPUTS</span></span>

### <span data-ttu-id="8b3e3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8b3e3-138">System.String</span></span>

### <span data-ttu-id="8b3e3-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="8b3e3-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="8b3e3-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b3e3-140">OUTPUTS</span></span>

### <span data-ttu-id="8b3e3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b3e3-141">System.Boolean</span></span>

## <span data-ttu-id="8b3e3-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b3e3-142">NOTES</span></span>

## <span data-ttu-id="8b3e3-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b3e3-143">RELATED LINKS</span></span>
