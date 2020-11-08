---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 1f1bcd7b0eb7318746f2f5a48ce5ccd58941196c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167138"
---
# <span data-ttu-id="a520a-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a520a-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="a520a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a520a-102">SYNOPSIS</span></span>
<span data-ttu-id="a520a-103">Austauschen von zwei Slots mit einer Web-App</span><span class="sxs-lookup"><span data-stu-id="a520a-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="a520a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a520a-104">SYNTAX</span></span>

### <span data-ttu-id="a520a-105">S1</span><span class="sxs-lookup"><span data-stu-id="a520a-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a520a-106">S2</span><span class="sxs-lookup"><span data-stu-id="a520a-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a520a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a520a-107">DESCRIPTION</span></span>
<span data-ttu-id="a520a-108">Die **Switch-AzWebAppSlot** wechselt zwei Slots, die einer Azure Web-App zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a520a-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="a520a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a520a-109">EXAMPLES</span></span>

### <span data-ttu-id="a520a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a520a-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a520a-111">Dieser Befehl wechselt in den Steckplatz "sourceslot" mit "destinationslot" die Web-App-ContosoWebApp, die der Ressourcengruppe Standard zugeordnet ist-Web-westus</span><span class="sxs-lookup"><span data-stu-id="a520a-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="a520a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a520a-112">PARAMETERS</span></span>

### <span data-ttu-id="a520a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a520a-113">-DefaultProfile</span></span>
<span data-ttu-id="a520a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a520a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a520a-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="a520a-115">-DestinationSlotName</span></span>
<span data-ttu-id="a520a-116">Name des Ziel Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="a520a-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="a520a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a520a-117">-Name</span></span>
<span data-ttu-id="a520a-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="a520a-118">WebApp Name</span></span>

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

### <span data-ttu-id="a520a-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="a520a-119">-PreserveVnet</span></span>
<span data-ttu-id="a520a-120">Preserve vnet boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="a520a-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="a520a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a520a-121">-ResourceGroupName</span></span>
<span data-ttu-id="a520a-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a520a-122">Resource Group Name</span></span>

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

### <span data-ttu-id="a520a-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="a520a-123">-SourceSlotName</span></span>
<span data-ttu-id="a520a-124">Name des Quell Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="a520a-124">Source Slot Name</span></span>

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

### <span data-ttu-id="a520a-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="a520a-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="a520a-126">Mit Vorschau Aktion austauschen</span><span class="sxs-lookup"><span data-stu-id="a520a-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="a520a-127">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="a520a-127">-WebApp</span></span>
<span data-ttu-id="a520a-128">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="a520a-128">WebApp Object</span></span>

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

### <span data-ttu-id="a520a-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a520a-129">-Confirm</span></span>
<span data-ttu-id="a520a-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a520a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a520a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a520a-131">-WhatIf</span></span>
<span data-ttu-id="a520a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a520a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a520a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a520a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a520a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a520a-134">CommonParameters</span></span>
<span data-ttu-id="a520a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a520a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a520a-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a520a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a520a-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a520a-137">INPUTS</span></span>

### <span data-ttu-id="a520a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a520a-138">System.String</span></span>

### <span data-ttu-id="a520a-139">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a520a-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a520a-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a520a-140">OUTPUTS</span></span>

### <span data-ttu-id="a520a-141">System. void</span><span class="sxs-lookup"><span data-stu-id="a520a-141">System.Void</span></span>

## <span data-ttu-id="a520a-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a520a-142">NOTES</span></span>

## <span data-ttu-id="a520a-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a520a-143">RELATED LINKS</span></span>
