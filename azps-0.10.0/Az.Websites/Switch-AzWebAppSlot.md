---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/switch-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: e30179ce2e9198729771d406d1963ff0048e05b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842644"
---
# <span data-ttu-id="de017-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de017-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="de017-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de017-102">SYNOPSIS</span></span>
<span data-ttu-id="de017-103">Austauschen von zwei Slots mit einer Web-App</span><span class="sxs-lookup"><span data-stu-id="de017-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="de017-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de017-104">SYNTAX</span></span>

### <span data-ttu-id="de017-105">S1</span><span class="sxs-lookup"><span data-stu-id="de017-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de017-106">S2</span><span class="sxs-lookup"><span data-stu-id="de017-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de017-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de017-107">DESCRIPTION</span></span>
<span data-ttu-id="de017-108">Die **Switch-AzWebAppSlot** wechselt zwei Slots, die einer Azure Web-App zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="de017-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="de017-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de017-109">EXAMPLES</span></span>

### <span data-ttu-id="de017-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="de017-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="de017-111">Dieser Befehl wechselt den Steckplatz "sourceslot" mit "destinationslot" für für Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="de017-111">This command will switch slot "sourceslot" slot with "destinationslot" for for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="de017-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="de017-112">PARAMETERS</span></span>

### <span data-ttu-id="de017-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de017-113">-DefaultProfile</span></span>
<span data-ttu-id="de017-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de017-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de017-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="de017-115">-DestinationSlotName</span></span>
<span data-ttu-id="de017-116">Name des Ziel Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="de017-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="de017-117">-Name</span><span class="sxs-lookup"><span data-stu-id="de017-117">-Name</span></span>
<span data-ttu-id="de017-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="de017-118">WebApp Name</span></span>

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

### <span data-ttu-id="de017-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="de017-119">-PreserveVnet</span></span>
<span data-ttu-id="de017-120">Preserve vnet boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="de017-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="de017-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de017-121">-ResourceGroupName</span></span>
<span data-ttu-id="de017-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="de017-122">Resource Group Name</span></span>

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

### <span data-ttu-id="de017-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="de017-123">-SourceSlotName</span></span>
<span data-ttu-id="de017-124">Name des Quell Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="de017-124">Source Slot Name</span></span>

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

### <span data-ttu-id="de017-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="de017-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="de017-126">Mit Vorschau Aktion austauschen</span><span class="sxs-lookup"><span data-stu-id="de017-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="de017-127">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="de017-127">-WebApp</span></span>
<span data-ttu-id="de017-128">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="de017-128">WebApp Object</span></span>

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

### <span data-ttu-id="de017-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de017-129">-Confirm</span></span>
<span data-ttu-id="de017-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de017-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de017-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de017-131">-WhatIf</span></span>
<span data-ttu-id="de017-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de017-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de017-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de017-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de017-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de017-134">CommonParameters</span></span>
<span data-ttu-id="de017-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de017-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de017-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de017-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de017-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de017-137">INPUTS</span></span>

### <span data-ttu-id="de017-138">Website</span><span class="sxs-lookup"><span data-stu-id="de017-138">Site</span></span>
<span data-ttu-id="de017-139">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="de017-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="de017-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de017-140">OUTPUTS</span></span>

## <span data-ttu-id="de017-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="de017-141">NOTES</span></span>

## <span data-ttu-id="de017-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de017-142">RELATED LINKS</span></span>

