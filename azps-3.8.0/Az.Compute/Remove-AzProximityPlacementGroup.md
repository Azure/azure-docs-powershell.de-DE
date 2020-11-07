---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 07adbff46713136ec412d10bd428765230e1838c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847620"
---
# <span data-ttu-id="ed28a-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ed28a-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="ed28a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed28a-102">SYNOPSIS</span></span>
<span data-ttu-id="ed28a-103">Löschen Sie die Ressource für die Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ed28a-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="ed28a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed28a-104">SYNTAX</span></span>

### <span data-ttu-id="ed28a-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed28a-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed28a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ed28a-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed28a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ed28a-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed28a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed28a-108">DESCRIPTION</span></span>
<span data-ttu-id="ed28a-109">Mit diesem Cmdlet wird die Ressource für die Näherungs Platzierungs Gruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ed28a-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="ed28a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed28a-110">EXAMPLES</span></span>

### <span data-ttu-id="ed28a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed28a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="ed28a-112">Dieser Befehl entfernt die angegebene Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ed28a-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="ed28a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed28a-113">PARAMETERS</span></span>

### <span data-ttu-id="ed28a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed28a-114">-AsJob</span></span>
<span data-ttu-id="ed28a-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ed28a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed28a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed28a-116">-DefaultProfile</span></span>
<span data-ttu-id="ed28a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed28a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed28a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ed28a-118">-Force</span></span>
<span data-ttu-id="ed28a-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ed28a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed28a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ed28a-120">-InputObject</span></span>
<span data-ttu-id="ed28a-121">Das Gruppenobjekt "PS-Näherungs Platzierung"</span><span class="sxs-lookup"><span data-stu-id="ed28a-121">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed28a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ed28a-122">-Name</span></span>
<span data-ttu-id="ed28a-123">Der Name der Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ed28a-123">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed28a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed28a-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed28a-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ed28a-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed28a-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ed28a-126">-ResourceId</span></span>
<span data-ttu-id="ed28a-127">Die Ressourcen-ID für die Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ed28a-127">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed28a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed28a-128">-Confirm</span></span>
<span data-ttu-id="ed28a-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed28a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed28a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed28a-130">-WhatIf</span></span>
<span data-ttu-id="ed28a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed28a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed28a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed28a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed28a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed28a-133">CommonParameters</span></span>
<span data-ttu-id="ed28a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed28a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed28a-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed28a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed28a-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed28a-136">INPUTS</span></span>

### <span data-ttu-id="ed28a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ed28a-137">System.String</span></span>

### <span data-ttu-id="ed28a-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ed28a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="ed28a-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed28a-139">OUTPUTS</span></span>

### <span data-ttu-id="ed28a-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ed28a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ed28a-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed28a-141">NOTES</span></span>

## <span data-ttu-id="ed28a-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed28a-142">RELATED LINKS</span></span>
