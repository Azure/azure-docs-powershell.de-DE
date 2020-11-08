---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006469"
---
# <span data-ttu-id="6843a-101">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="6843a-101">Get-WAPackVNet</span></span>

## <span data-ttu-id="6843a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6843a-102">SYNOPSIS</span></span>
<span data-ttu-id="6843a-103">Ruft virtuelle Netzwerke ab.</span><span class="sxs-lookup"><span data-stu-id="6843a-103">Gets virtual networks.</span></span>

## <span data-ttu-id="6843a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6843a-104">SYNTAX</span></span>

### <span data-ttu-id="6843a-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="6843a-105">Empty (Default)</span></span>
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6843a-106">FromId</span><span class="sxs-lookup"><span data-stu-id="6843a-106">FromId</span></span>
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6843a-107">FromName</span><span class="sxs-lookup"><span data-stu-id="6843a-107">FromName</span></span>
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6843a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6843a-108">DESCRIPTION</span></span>
<span data-ttu-id="6843a-109">Das Cmdlet " **Get-WAPackVNet** " ruft virtuelle Netzwerke ab.</span><span class="sxs-lookup"><span data-stu-id="6843a-109">The **Get-WAPackVNet** cmdlet gets virtual networks.</span></span>

## <span data-ttu-id="6843a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6843a-110">EXAMPLES</span></span>

### <span data-ttu-id="6843a-111">Beispiel 1: Abrufen aller virtuellen Netzwerke</span><span class="sxs-lookup"><span data-stu-id="6843a-111">Example 1: Get all virtual networks</span></span>
```
PS C:\> Get-WAPackVNet
```

<span data-ttu-id="6843a-112">Dieser Befehl ruft alle virtuellen Netzwerke ab.</span><span class="sxs-lookup"><span data-stu-id="6843a-112">This command gets all virtual networks.</span></span>

### <span data-ttu-id="6843a-113">Beispiel 2: Abrufen eines virtuellen Netzwerks mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="6843a-113">Example 2: Get a virtual network by using an ID</span></span>
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="6843a-114">Dieser Befehl ruft das virtuelle Netzwerk ab, das die angegebene ID hat.</span><span class="sxs-lookup"><span data-stu-id="6843a-114">This command gets the virtual network that has the specified ID.</span></span>

### <span data-ttu-id="6843a-115">Beispiel 3: Abrufen eines virtuellen Netzwerks mithilfe eines Namens</span><span class="sxs-lookup"><span data-stu-id="6843a-115">Example 3: Get a virtual network by using a name</span></span>
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

<span data-ttu-id="6843a-116">Dieser Befehl ruft das virtuelle Netzwerk mit dem Namen ContosoVNet08 ab.</span><span class="sxs-lookup"><span data-stu-id="6843a-116">This command gets the virtual network named ContosoVNet08.</span></span>

## <span data-ttu-id="6843a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6843a-117">PARAMETERS</span></span>

### <span data-ttu-id="6843a-118">-ID</span><span class="sxs-lookup"><span data-stu-id="6843a-118">-ID</span></span>
<span data-ttu-id="6843a-119">Gibt die eindeutige ID eines virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="6843a-119">Specifies the unique ID of a virtual network.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6843a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6843a-120">-Name</span></span>
<span data-ttu-id="6843a-121">Gibt den Namen eines virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="6843a-121">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6843a-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="6843a-122">-Profile</span></span>
<span data-ttu-id="6843a-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6843a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6843a-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6843a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6843a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6843a-125">CommonParameters</span></span>
<span data-ttu-id="6843a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6843a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6843a-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6843a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6843a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6843a-128">INPUTS</span></span>

## <span data-ttu-id="6843a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6843a-129">OUTPUTS</span></span>

## <span data-ttu-id="6843a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="6843a-130">NOTES</span></span>

## <span data-ttu-id="6843a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6843a-131">RELATED LINKS</span></span>

