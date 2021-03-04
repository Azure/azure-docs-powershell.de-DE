---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 6b2121c581d3d7da990813884cf0097064b73f44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932387"
---
# <span data-ttu-id="95587-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="95587-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="95587-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95587-102">SYNOPSIS</span></span>
<span data-ttu-id="95587-103">Setzt den freigegebenen Schlüssel der Verbindung des virtuellen Netzwerkgateways zurück.</span><span class="sxs-lookup"><span data-stu-id="95587-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="95587-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95587-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95587-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95587-105">DESCRIPTION</span></span>
<span data-ttu-id="95587-106">Setzt den freigegebenen Schlüssel der Verbindung des virtuellen Netzwerkgateways zurück.</span><span class="sxs-lookup"><span data-stu-id="95587-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="95587-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95587-107">EXAMPLES</span></span>

### <span data-ttu-id="95587-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="95587-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="95587-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="95587-109">PARAMETERS</span></span>

### <span data-ttu-id="95587-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95587-110">-DefaultProfile</span></span>
<span data-ttu-id="95587-111">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95587-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95587-112">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="95587-112">-Force</span></span>
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

### <span data-ttu-id="95587-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="95587-113">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95587-114">-Name</span><span class="sxs-lookup"><span data-stu-id="95587-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95587-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95587-115">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95587-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95587-116">-Confirm</span></span>
<span data-ttu-id="95587-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95587-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95587-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95587-118">-WhatIf</span></span>
<span data-ttu-id="95587-119">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95587-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95587-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95587-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95587-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95587-121">CommonParameters</span></span>
<span data-ttu-id="95587-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95587-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95587-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95587-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95587-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95587-124">INPUTS</span></span>

### <span data-ttu-id="95587-125">System.String</span><span class="sxs-lookup"><span data-stu-id="95587-125">System.String</span></span>

### <span data-ttu-id="95587-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="95587-126">System.UInt32</span></span>

## <span data-ttu-id="95587-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95587-127">OUTPUTS</span></span>

### <span data-ttu-id="95587-128">System.String</span><span class="sxs-lookup"><span data-stu-id="95587-128">System.String</span></span>

## <span data-ttu-id="95587-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="95587-129">NOTES</span></span>

## <span data-ttu-id="95587-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="95587-130">RELATED LINKS</span></span>

[<span data-ttu-id="95587-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="95587-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="95587-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="95587-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
