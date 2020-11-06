---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 56f0c3ec3a69819ad7faa28b10d33a3cf751c48f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481818"
---
# <span data-ttu-id="ea5c8-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ea5c8-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="ea5c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5c8-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="ea5c8-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea5c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea5c8-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea5c8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="ea5c8-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="ea5c8-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ea5c8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea5c8-107">EXAMPLES</span></span>

### <span data-ttu-id="ea5c8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea5c8-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ea5c8-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="ea5c8-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ea5c8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea5c8-110">PARAMETERS</span></span>

### <span data-ttu-id="ea5c8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ea5c8-111">-Force</span></span>
<span data-ttu-id="ea5c8-112">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="ea5c8-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="ea5c8-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ea5c8-113">-RouteFilter</span></span>
<span data-ttu-id="ea5c8-114">Die RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ea5c8-114">The RouteFilter</span></span>

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

### <span data-ttu-id="ea5c8-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea5c8-115">-Confirm</span></span>
<span data-ttu-id="ea5c8-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea5c8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea5c8-117">-WhatIf</span></span>
<span data-ttu-id="ea5c8-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea5c8-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea5c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5c8-120">-DefaultProfile</span></span>
<span data-ttu-id="ea5c8-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea5c8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5c8-122">CommonParameters</span></span>
<span data-ttu-id="ea5c8-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5c8-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea5c8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5c8-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea5c8-125">INPUTS</span></span>

### <span data-ttu-id="ea5c8-126">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ea5c8-126">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ea5c8-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea5c8-127">OUTPUTS</span></span>

### <span data-ttu-id="ea5c8-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ea5c8-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ea5c8-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea5c8-129">NOTES</span></span>

## <span data-ttu-id="ea5c8-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea5c8-130">RELATED LINKS</span></span>

