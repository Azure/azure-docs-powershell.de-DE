---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 496ABC97-A493-4E42-B998-28A907DFBC19
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0641fd7bc8dcfa5048ac3e9d922bade199af2bab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006145"
---
# <span data-ttu-id="4bd78-101">Switch-AzureWebsiteSlot</span><span class="sxs-lookup"><span data-stu-id="4bd78-101">Switch-AzureWebsiteSlot</span></span>

## <span data-ttu-id="4bd78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bd78-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd78-103">Tauscht den Produktions Steckplatz für eine Website mit einem anderen Steckplatz aus.</span><span class="sxs-lookup"><span data-stu-id="4bd78-103">Swaps the production slot for a website with another slot.</span></span>

## <span data-ttu-id="4bd78-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bd78-104">SYNTAX</span></span>

```
Switch-AzureWebsiteSlot [-Name <String>] [-Slot1 <String>] [-Slot2 <String>] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bd78-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bd78-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd78-106">Mit dem Cmdlet " **Switch-AzureWebsiteSlot** " wird der Produktions Steckplatz für eine Website durch einen anderen Steckplatz ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4bd78-106">The **Switch-AzureWebsiteSlot** cmdlet swaps the production slot for a website with another slot.</span></span>
<span data-ttu-id="4bd78-107">Dies funktioniert nur auf Websites mit zwei Slots.</span><span class="sxs-lookup"><span data-stu-id="4bd78-107">This works on websites with two slots only.</span></span>

## <span data-ttu-id="4bd78-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bd78-108">EXAMPLES</span></span>

### <span data-ttu-id="4bd78-109">Beispiel 1: Wechseln des Website Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="4bd78-109">Example 1: Switch Website Slot</span></span>
```
PS C:\> Switch-AzureWebsiteSlot -Name MyWebsite
```

<span data-ttu-id="4bd78-110">Wechseln Sie zum Sicherungs Steckplatz der Azure-Website mywebsite mit dem Produktions Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="4bd78-110">Switch the azure website MyWebsite backup slot with production slot.</span></span>

## <span data-ttu-id="4bd78-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bd78-111">PARAMETERS</span></span>

### <span data-ttu-id="4bd78-112">-Force</span><span class="sxs-lookup"><span data-stu-id="4bd78-112">-Force</span></span>
<span data-ttu-id="4bd78-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4bd78-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd78-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4bd78-114">-Name</span></span>
<span data-ttu-id="4bd78-115">Der Name der Website.</span><span class="sxs-lookup"><span data-stu-id="4bd78-115">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd78-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="4bd78-116">-Profile</span></span>
<span data-ttu-id="4bd78-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4bd78-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4bd78-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4bd78-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd78-119">-Slot1</span><span class="sxs-lookup"><span data-stu-id="4bd78-119">-Slot1</span></span>
<span data-ttu-id="4bd78-120">Gibt den ersten Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="4bd78-120">Specifies the first slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd78-121">-SLOT2</span><span class="sxs-lookup"><span data-stu-id="4bd78-121">-Slot2</span></span>
<span data-ttu-id="4bd78-122">Gibt den zweiten Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="4bd78-122">Specifies the second slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd78-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4bd78-123">-Confirm</span></span>
<span data-ttu-id="4bd78-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4bd78-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd78-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bd78-125">-WhatIf</span></span>
<span data-ttu-id="4bd78-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bd78-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bd78-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bd78-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd78-128">CommonParameters</span></span>
<span data-ttu-id="4bd78-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd78-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd78-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd78-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bd78-131">INPUTS</span></span>

## <span data-ttu-id="4bd78-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bd78-132">OUTPUTS</span></span>

## <span data-ttu-id="4bd78-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bd78-133">NOTES</span></span>

## <span data-ttu-id="4bd78-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bd78-134">RELATED LINKS</span></span>

[<span data-ttu-id="4bd78-135">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4bd78-135">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="4bd78-136">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4bd78-136">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="4bd78-137">Anfang-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4bd78-137">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="4bd78-138">Stopp-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4bd78-138">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


