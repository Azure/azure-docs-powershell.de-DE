---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 9671c2041f767df5066353988eb633318289de47
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848595"
---
# <span data-ttu-id="9135c-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9135c-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="9135c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9135c-102">SYNOPSIS</span></span>
<span data-ttu-id="9135c-103">Austauschen von zwei Slots mit einer Web-App</span><span class="sxs-lookup"><span data-stu-id="9135c-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9135c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9135c-104">SYNTAX</span></span>

### <span data-ttu-id="9135c-105">S1</span><span class="sxs-lookup"><span data-stu-id="9135c-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9135c-106">S2</span><span class="sxs-lookup"><span data-stu-id="9135c-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9135c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9135c-107">DESCRIPTION</span></span>
<span data-ttu-id="9135c-108">Die **Switch-AzureRmWebAppSlot** wechselt zwei Slots, die einer Azure Web-App zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9135c-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="9135c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9135c-109">EXAMPLES</span></span>

### <span data-ttu-id="9135c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9135c-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="9135c-111">Dieser Befehl wechselt den Steckplatz "sourceslot" mit "destinationslot" für Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="9135c-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="9135c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9135c-112">PARAMETERS</span></span>

### <span data-ttu-id="9135c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9135c-113">-DefaultProfile</span></span>
<span data-ttu-id="9135c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9135c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9135c-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="9135c-115">-DestinationSlotName</span></span>
<span data-ttu-id="9135c-116">Name des Ziel Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="9135c-116">Destination Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9135c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9135c-117">-Name</span></span>
<span data-ttu-id="9135c-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9135c-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9135c-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="9135c-119">-PreserveVnet</span></span>
<span data-ttu-id="9135c-120">Preserve vnet boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="9135c-120">Preserve Vnet Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9135c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9135c-121">-ResourceGroupName</span></span>
<span data-ttu-id="9135c-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9135c-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9135c-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="9135c-123">-SourceSlotName</span></span>
<span data-ttu-id="9135c-124">Name des Quell Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="9135c-124">Source Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9135c-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="9135c-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="9135c-126">Mit Vorschau Aktion austauschen</span><span class="sxs-lookup"><span data-stu-id="9135c-126">Swap With Preview Action</span></span>

```yaml
Type: SwapWithPreviewAction
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9135c-127">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="9135c-127">-WebApp</span></span>
<span data-ttu-id="9135c-128">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="9135c-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9135c-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9135c-129">-Confirm</span></span>
<span data-ttu-id="9135c-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9135c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9135c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9135c-131">-WhatIf</span></span>
<span data-ttu-id="9135c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9135c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9135c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9135c-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9135c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9135c-134">CommonParameters</span></span>
<span data-ttu-id="9135c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9135c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9135c-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9135c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9135c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9135c-137">INPUTS</span></span>

### <span data-ttu-id="9135c-138">Website</span><span class="sxs-lookup"><span data-stu-id="9135c-138">Site</span></span>
<span data-ttu-id="9135c-139">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9135c-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9135c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9135c-140">OUTPUTS</span></span>

## <span data-ttu-id="9135c-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9135c-141">NOTES</span></span>

## <span data-ttu-id="9135c-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9135c-142">RELATED LINKS</span></span>

