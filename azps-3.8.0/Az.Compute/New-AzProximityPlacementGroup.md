---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: cf8c4867fcc623065cce73fa392cb78d513200fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996154"
---
# <span data-ttu-id="567e4-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="567e4-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="567e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="567e4-102">SYNOPSIS</span></span>
<span data-ttu-id="567e4-103">Erstellen einer Näherungs-Placement-Gruppenressource</span><span class="sxs-lookup"><span data-stu-id="567e4-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="567e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="567e4-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="567e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="567e4-105">DESCRIPTION</span></span>
<span data-ttu-id="567e4-106">Mit diesem Cmdlet wird die Gruppenressource für die Näherungsposition erstellt.</span><span class="sxs-lookup"><span data-stu-id="567e4-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="567e4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="567e4-107">EXAMPLES</span></span>

### <span data-ttu-id="567e4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="567e4-108">Example 1</span></span>
```
PS C:\> New-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = "val1"}

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {"key1":"val1"}
```

<span data-ttu-id="567e4-109">Mit diesem Befehl wird eine Näherungs Ortsgruppe an der angegebenen Position erstellt.</span><span class="sxs-lookup"><span data-stu-id="567e4-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="567e4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="567e4-110">PARAMETERS</span></span>

### <span data-ttu-id="567e4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="567e4-111">-AsJob</span></span>
<span data-ttu-id="567e4-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="567e4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="567e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567e4-113">-DefaultProfile</span></span>
<span data-ttu-id="567e4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="567e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="567e4-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="567e4-115">-Location</span></span>
<span data-ttu-id="567e4-116">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="567e4-116">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567e4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="567e4-117">-Name</span></span>
<span data-ttu-id="567e4-118">Der Name der Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="567e4-118">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567e4-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="567e4-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="567e4-120">Gibt den Typ der Näherungs Platzierungs Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="567e4-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="567e4-121">Mögliche Werte sind: Standard oder Ultra</span><span class="sxs-lookup"><span data-stu-id="567e4-121">Possible values are: Standard or Ultra</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567e4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="567e4-122">-ResourceGroupName</span></span>
<span data-ttu-id="567e4-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="567e4-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567e4-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="567e4-124">-Tag</span></span>
<span data-ttu-id="567e4-125">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="567e4-125">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567e4-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="567e4-126">-Confirm</span></span>
<span data-ttu-id="567e4-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="567e4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="567e4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="567e4-128">-WhatIf</span></span>
<span data-ttu-id="567e4-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="567e4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="567e4-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="567e4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="567e4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567e4-131">CommonParameters</span></span>
<span data-ttu-id="567e4-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="567e4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567e4-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="567e4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567e4-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="567e4-134">INPUTS</span></span>

### <span data-ttu-id="567e4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="567e4-135">System.String</span></span>

## <span data-ttu-id="567e4-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="567e4-136">OUTPUTS</span></span>

### <span data-ttu-id="567e4-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="567e4-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="567e4-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="567e4-138">NOTES</span></span>

## <span data-ttu-id="567e4-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="567e4-139">RELATED LINKS</span></span>
