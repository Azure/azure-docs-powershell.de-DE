---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 7cb74e6eec27df299206ee62264588a37dee3a2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948112"
---
# <span data-ttu-id="5e685-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5e685-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="5e685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e685-102">SYNOPSIS</span></span>
<span data-ttu-id="5e685-103">Tauschen von zwei Steckplätzen mit einer Web App</span><span class="sxs-lookup"><span data-stu-id="5e685-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="5e685-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e685-104">SYNTAX</span></span>

### <span data-ttu-id="5e685-105">S1</span><span class="sxs-lookup"><span data-stu-id="5e685-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e685-106">S2</span><span class="sxs-lookup"><span data-stu-id="5e685-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e685-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e685-107">DESCRIPTION</span></span>
<span data-ttu-id="5e685-108">Der **Switch-AzWebAppSlot** wechselt zwei Steckplätze, die einer Azure Web App zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5e685-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="5e685-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e685-109">EXAMPLES</span></span>

### <span data-ttu-id="5e685-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e685-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="5e685-111">Dieser Befehl wechselt den Slot "sourceslot" mit "destinationslot" der Web App ContosoWebApp, die der Ressourcengruppe Default-Web-WestUS zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5e685-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="5e685-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5e685-112">PARAMETERS</span></span>

### <span data-ttu-id="5e685-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e685-113">-DefaultProfile</span></span>
<span data-ttu-id="5e685-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e685-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e685-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="5e685-115">-DestinationSlotName</span></span>
<span data-ttu-id="5e685-116">Zielplatzname</span><span class="sxs-lookup"><span data-stu-id="5e685-116">Destination Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e685-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5e685-117">-Name</span></span>
<span data-ttu-id="5e685-118">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="5e685-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e685-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="5e685-119">-PreserveVnet</span></span>
<span data-ttu-id="5e685-120">Beibehalten von Vnet Boolean</span><span class="sxs-lookup"><span data-stu-id="5e685-120">Preserve Vnet Boolean</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e685-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e685-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e685-122">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5e685-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e685-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="5e685-123">-SourceSlotName</span></span>
<span data-ttu-id="5e685-124">Name des Quellplatzes</span><span class="sxs-lookup"><span data-stu-id="5e685-124">Source Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e685-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="5e685-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="5e685-126">Tauschen mit Vorschauaktion</span><span class="sxs-lookup"><span data-stu-id="5e685-126">Swap With Preview Action</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.WebApps.Utilities.SwapWithPreviewAction]
Parameter Sets: (All)
Aliases:
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e685-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5e685-127">-WebApp</span></span>
<span data-ttu-id="5e685-128">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="5e685-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e685-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e685-129">-Confirm</span></span>
<span data-ttu-id="5e685-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e685-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e685-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e685-131">-WhatIf</span></span>
<span data-ttu-id="5e685-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e685-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e685-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e685-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e685-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e685-134">CommonParameters</span></span>
<span data-ttu-id="5e685-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e685-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e685-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e685-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e685-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e685-137">INPUTS</span></span>

### <span data-ttu-id="5e685-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5e685-138">System.String</span></span>

### <span data-ttu-id="5e685-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5e685-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5e685-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e685-140">OUTPUTS</span></span>

### <span data-ttu-id="5e685-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="5e685-141">System.Void</span></span>

## <span data-ttu-id="5e685-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5e685-142">NOTES</span></span>

## <span data-ttu-id="5e685-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5e685-143">RELATED LINKS</span></span>
