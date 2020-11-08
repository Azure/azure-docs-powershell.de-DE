---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174295"
---
# <span data-ttu-id="9cec4-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="9cec4-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="9cec4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9cec4-102">SYNOPSIS</span></span>
<span data-ttu-id="9cec4-103">Entfernt eine Identität aus einem ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="9cec4-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="9cec4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cec4-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cec4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cec4-105">DESCRIPTION</span></span>
<span data-ttu-id="9cec4-106">Das Cmdlet **Remove-AzExpressRoutePortIdentity** entfernt die Identität aus einem lokalen Azure ExpressRoutePort-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9cec4-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="9cec4-107">Verwenden Sie **Remove-AzExpressRoutePort** , um Sie aus ExpressRoutePort zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9cec4-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="9cec4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cec4-108">EXAMPLES</span></span>

### <span data-ttu-id="9cec4-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9cec4-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="9cec4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cec4-110">PARAMETERS</span></span>

### <span data-ttu-id="9cec4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cec4-111">-DefaultProfile</span></span>
<span data-ttu-id="9cec4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9cec4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cec4-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9cec4-113">-ExpressRoutePort</span></span>
<span data-ttu-id="9cec4-114">Die ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9cec4-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cec4-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9cec4-115">-Confirm</span></span>
<span data-ttu-id="9cec4-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9cec4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cec4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cec4-117">-WhatIf</span></span>
<span data-ttu-id="9cec4-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9cec4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cec4-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9cec4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cec4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cec4-120">CommonParameters</span></span>
<span data-ttu-id="9cec4-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cec4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cec4-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cec4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="9cec4-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9cec4-123">INPUTS</span></span>

### <span data-ttu-id="9cec4-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9cec4-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="9cec4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9cec4-125">OUTPUTS</span></span>

### <span data-ttu-id="9cec4-126">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9cec4-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="9cec4-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="9cec4-127">NOTES</span></span>

## <span data-ttu-id="9cec4-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9cec4-128">RELATED LINKS</span></span>
[<span data-ttu-id="9cec4-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="9cec4-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="9cec4-130">Neu – AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="9cec4-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="9cec4-131">Satz-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="9cec4-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
