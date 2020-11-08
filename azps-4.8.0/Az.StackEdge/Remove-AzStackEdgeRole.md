---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174024"
---
# <span data-ttu-id="1c257-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1c257-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="1c257-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c257-102">SYNOPSIS</span></span>
<span data-ttu-id="1c257-103">Entfernt die zugeordnete Rolle für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="1c257-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="1c257-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c257-104">SYNTAX</span></span>

### <span data-ttu-id="1c257-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c257-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c257-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c257-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c257-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c257-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c257-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c257-108">DESCRIPTION</span></span>
<span data-ttu-id="1c257-109">Das Cmdlet **Remove-AzStackEdgeRole** entfernt die zugeordnete Rolle für ein Stack-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="1c257-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="1c257-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c257-110">EXAMPLES</span></span>

### <span data-ttu-id="1c257-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c257-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="1c257-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c257-112">PARAMETERS</span></span>

### <span data-ttu-id="1c257-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c257-113">-AsJob</span></span>
<span data-ttu-id="1c257-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1c257-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c257-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c257-115">-DefaultProfile</span></span>
<span data-ttu-id="1c257-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c257-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c257-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1c257-117">-DeviceName</span></span>
<span data-ttu-id="1c257-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="1c257-118">Device Name</span></span>

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

### <span data-ttu-id="1c257-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1c257-119">-InputObject</span></span>
<span data-ttu-id="1c257-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="1c257-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c257-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1c257-121">-Name</span></span>
<span data-ttu-id="1c257-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="1c257-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c257-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c257-123">-PassThru</span></span>
<span data-ttu-id="1c257-124">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="1c257-124">returns true if successful</span></span>

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

### <span data-ttu-id="1c257-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c257-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c257-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="1c257-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1c257-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1c257-127">-ResourceId</span></span>
<span data-ttu-id="1c257-128">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="1c257-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1c257-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c257-129">-Confirm</span></span>
<span data-ttu-id="1c257-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c257-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c257-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c257-131">-WhatIf</span></span>
<span data-ttu-id="1c257-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c257-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c257-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c257-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c257-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c257-134">CommonParameters</span></span>
<span data-ttu-id="1c257-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c257-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c257-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c257-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c257-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c257-137">INPUTS</span></span>

### <span data-ttu-id="1c257-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1c257-138">System.String</span></span>

### <span data-ttu-id="1c257-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1c257-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="1c257-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c257-140">OUTPUTS</span></span>

### <span data-ttu-id="1c257-141">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1c257-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="1c257-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c257-142">NOTES</span></span>

## <span data-ttu-id="1c257-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c257-143">RELATED LINKS</span></span>
