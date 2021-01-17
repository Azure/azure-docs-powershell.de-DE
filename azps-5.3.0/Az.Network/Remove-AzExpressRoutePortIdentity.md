---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468940"
---
# <span data-ttu-id="4aa75-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4aa75-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="4aa75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aa75-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa75-103">Entfernt eine Identität aus einem ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="4aa75-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="4aa75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aa75-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aa75-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aa75-105">DESCRIPTION</span></span>
<span data-ttu-id="4aa75-106">Das **Cmdlet "Remove-AzExpressRoutePortIdentity"** entfernt die Identität eines lokalen Azure ExpressRoutePort-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4aa75-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="4aa75-107">Verwenden **Sie "Remove-AzExpressRoutePort",** um ihn aus ExpressRoutePort zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4aa75-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="4aa75-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4aa75-108">EXAMPLES</span></span>

### <span data-ttu-id="4aa75-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4aa75-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="4aa75-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aa75-110">PARAMETERS</span></span>

### <span data-ttu-id="4aa75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa75-111">-DefaultProfile</span></span>
<span data-ttu-id="4aa75-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4aa75-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aa75-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4aa75-113">-ExpressRoutePort</span></span>
<span data-ttu-id="4aa75-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4aa75-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="4aa75-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4aa75-115">-Confirm</span></span>
<span data-ttu-id="4aa75-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4aa75-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aa75-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4aa75-117">-WhatIf</span></span>
<span data-ttu-id="4aa75-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4aa75-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa75-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4aa75-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aa75-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa75-120">CommonParameters</span></span>
<span data-ttu-id="4aa75-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aa75-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa75-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aa75-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="4aa75-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4aa75-123">INPUTS</span></span>

### <span data-ttu-id="4aa75-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4aa75-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="4aa75-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4aa75-125">OUTPUTS</span></span>

### <span data-ttu-id="4aa75-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4aa75-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="4aa75-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4aa75-127">NOTES</span></span>

## <span data-ttu-id="4aa75-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4aa75-128">RELATED LINKS</span></span>
[<span data-ttu-id="4aa75-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4aa75-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="4aa75-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4aa75-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="4aa75-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4aa75-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
