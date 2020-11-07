---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 5dc2b6a9650cdf4110858edf1b061f69adac48f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663124"
---
# <span data-ttu-id="a3756-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a3756-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="a3756-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3756-102">SYNOPSIS</span></span>
<span data-ttu-id="a3756-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="a3756-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3756-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3756-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3756-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3756-105">DESCRIPTION</span></span>
<span data-ttu-id="a3756-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="a3756-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="a3756-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3756-107">EXAMPLES</span></span>

### <span data-ttu-id="a3756-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3756-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a3756-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="a3756-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="a3756-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3756-110">PARAMETERS</span></span>

### <span data-ttu-id="a3756-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3756-111">-AsJob</span></span>
<span data-ttu-id="a3756-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a3756-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3756-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3756-113">-DefaultProfile</span></span>
<span data-ttu-id="a3756-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3756-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3756-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a3756-115">-Force</span></span>
<span data-ttu-id="a3756-116">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="a3756-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="a3756-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a3756-117">-RouteFilter</span></span>
<span data-ttu-id="a3756-118">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="a3756-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3756-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3756-119">-Confirm</span></span>
<span data-ttu-id="a3756-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3756-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3756-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3756-121">-WhatIf</span></span>
<span data-ttu-id="a3756-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3756-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3756-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3756-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3756-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3756-124">CommonParameters</span></span>
<span data-ttu-id="a3756-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3756-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3756-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3756-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3756-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3756-127">INPUTS</span></span>

### <span data-ttu-id="a3756-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a3756-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="a3756-129">Parameter: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3756-129">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="a3756-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3756-130">OUTPUTS</span></span>

### <span data-ttu-id="a3756-131">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a3756-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="a3756-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3756-132">NOTES</span></span>

## <span data-ttu-id="a3756-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3756-133">RELATED LINKS</span></span>
