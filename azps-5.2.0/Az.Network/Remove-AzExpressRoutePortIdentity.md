---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366819"
---
# <span data-ttu-id="2a154-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="2a154-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="2a154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a154-102">SYNOPSIS</span></span>
<span data-ttu-id="2a154-103">Entfernt eine Identität aus einem ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="2a154-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="2a154-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a154-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a154-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a154-105">DESCRIPTION</span></span>
<span data-ttu-id="2a154-106">Das **Cmdlet "Remove-AzExpressRoutePortIdentity"** entfernt die Identität eines lokalen Azure ExpressRoutePort-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2a154-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="2a154-107">Verwenden **Sie "Remove-AzExpressRoutePort",** um ihn aus ExpressRoutePort zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2a154-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="2a154-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a154-108">EXAMPLES</span></span>

### <span data-ttu-id="2a154-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2a154-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="2a154-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a154-110">PARAMETERS</span></span>

### <span data-ttu-id="2a154-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a154-111">-DefaultProfile</span></span>
<span data-ttu-id="2a154-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a154-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a154-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2a154-113">-ExpressRoutePort</span></span>
<span data-ttu-id="2a154-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2a154-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="2a154-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a154-115">-Confirm</span></span>
<span data-ttu-id="2a154-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a154-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a154-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2a154-117">-WhatIf</span></span>
<span data-ttu-id="2a154-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a154-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a154-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a154-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a154-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a154-120">CommonParameters</span></span>
<span data-ttu-id="2a154-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a154-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a154-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a154-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="2a154-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a154-123">INPUTS</span></span>

### <span data-ttu-id="2a154-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2a154-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="2a154-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a154-125">OUTPUTS</span></span>

### <span data-ttu-id="2a154-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="2a154-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="2a154-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2a154-127">NOTES</span></span>

## <span data-ttu-id="2a154-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2a154-128">RELATED LINKS</span></span>
[<span data-ttu-id="2a154-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="2a154-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="2a154-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="2a154-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="2a154-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="2a154-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
