---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 942669106e70bbb8c5b5b6f059fe934effe9b7fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843579"
---
# <span data-ttu-id="cf8b9-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cf8b9-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="cf8b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8b9-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="cf8b9-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="cf8b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf8b9-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf8b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf8b9-105">DESCRIPTION</span></span>
<span data-ttu-id="cf8b9-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="cf8b9-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="cf8b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf8b9-107">EXAMPLES</span></span>

### <span data-ttu-id="cf8b9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cf8b9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="cf8b9-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="cf8b9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="cf8b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf8b9-110">PARAMETERS</span></span>

### <span data-ttu-id="cf8b9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf8b9-111">-AsJob</span></span>
<span data-ttu-id="cf8b9-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cf8b9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf8b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8b9-113">-DefaultProfile</span></span>
<span data-ttu-id="cf8b9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf8b9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf8b9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cf8b9-115">-Force</span></span>
<span data-ttu-id="cf8b9-116">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="cf8b9-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="cf8b9-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="cf8b9-117">-RouteFilter</span></span>
<span data-ttu-id="cf8b9-118">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="cf8b9-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8b9-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf8b9-119">-Confirm</span></span>
<span data-ttu-id="cf8b9-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf8b9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf8b9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf8b9-121">-WhatIf</span></span>
<span data-ttu-id="cf8b9-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf8b9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf8b9-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf8b9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf8b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8b9-124">CommonParameters</span></span>
<span data-ttu-id="cf8b9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf8b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8b9-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf8b9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8b9-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf8b9-127">INPUTS</span></span>

### <span data-ttu-id="cf8b9-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cf8b9-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="cf8b9-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf8b9-129">OUTPUTS</span></span>

### <span data-ttu-id="cf8b9-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cf8b9-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="cf8b9-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf8b9-131">NOTES</span></span>

## <span data-ttu-id="cf8b9-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf8b9-132">RELATED LINKS</span></span>

