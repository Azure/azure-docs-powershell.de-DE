---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: 88cdb68da94f84dc1af977ba5b12b5bfb4d73914
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652070"
---
# <span data-ttu-id="28332-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="28332-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="28332-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28332-102">SYNOPSIS</span></span>
<span data-ttu-id="28332-103">Erstellen einer Näherungs-Placement-Gruppenressource</span><span class="sxs-lookup"><span data-stu-id="28332-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="28332-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28332-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28332-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28332-105">DESCRIPTION</span></span>
<span data-ttu-id="28332-106">Mit diesem Cmdlet wird die Gruppenressource für die Näherungsposition erstellt.</span><span class="sxs-lookup"><span data-stu-id="28332-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="28332-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28332-107">EXAMPLES</span></span>

### <span data-ttu-id="28332-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28332-108">Example 1</span></span>
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

<span data-ttu-id="28332-109">Mit diesem Befehl wird eine Näherungs Ortsgruppe an der angegebenen Position erstellt.</span><span class="sxs-lookup"><span data-stu-id="28332-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="28332-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="28332-110">PARAMETERS</span></span>

### <span data-ttu-id="28332-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28332-111">-AsJob</span></span>
<span data-ttu-id="28332-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="28332-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28332-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28332-113">-DefaultProfile</span></span>
<span data-ttu-id="28332-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28332-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28332-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="28332-115">-Location</span></span>
<span data-ttu-id="28332-116">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="28332-116">Resource location</span></span>

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

### <span data-ttu-id="28332-117">-Name</span><span class="sxs-lookup"><span data-stu-id="28332-117">-Name</span></span>
<span data-ttu-id="28332-118">Der Name der Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="28332-118">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="28332-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="28332-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="28332-120">Gibt den Typ der Näherungs Platzierungs Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="28332-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="28332-121">Mögliche Werte sind: Standard oder Ultra</span><span class="sxs-lookup"><span data-stu-id="28332-121">Possible values are: Standard or Ultra</span></span>

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

### <span data-ttu-id="28332-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28332-122">-ResourceGroupName</span></span>
<span data-ttu-id="28332-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="28332-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="28332-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="28332-124">-Tag</span></span>
<span data-ttu-id="28332-125">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="28332-125">Resource tags</span></span>

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

### <span data-ttu-id="28332-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28332-126">-Confirm</span></span>
<span data-ttu-id="28332-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28332-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28332-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28332-128">-WhatIf</span></span>
<span data-ttu-id="28332-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28332-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28332-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28332-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28332-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28332-131">CommonParameters</span></span>
<span data-ttu-id="28332-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28332-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28332-133">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28332-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28332-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28332-134">INPUTS</span></span>

### <span data-ttu-id="28332-135">System. String</span><span class="sxs-lookup"><span data-stu-id="28332-135">System.String</span></span>

## <span data-ttu-id="28332-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28332-136">OUTPUTS</span></span>

### <span data-ttu-id="28332-137">Microsoft. Azure. Commands. Compute. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="28332-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="28332-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="28332-138">NOTES</span></span>

## <span data-ttu-id="28332-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28332-139">RELATED LINKS</span></span>
