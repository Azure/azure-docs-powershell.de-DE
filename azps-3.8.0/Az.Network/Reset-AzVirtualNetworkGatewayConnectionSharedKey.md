---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004143"
---
# <span data-ttu-id="b14de-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b14de-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="b14de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b14de-102">SYNOPSIS</span></span>
<span data-ttu-id="b14de-103">Setzt den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="b14de-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b14de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b14de-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b14de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b14de-105">DESCRIPTION</span></span>
<span data-ttu-id="b14de-106">Setzt den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="b14de-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b14de-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b14de-107">EXAMPLES</span></span>

### <span data-ttu-id="b14de-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="b14de-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="b14de-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b14de-109">PARAMETERS</span></span>

### <span data-ttu-id="b14de-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b14de-110">-DefaultProfile</span></span>
<span data-ttu-id="b14de-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b14de-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b14de-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b14de-112">-Force</span></span>
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

### <span data-ttu-id="b14de-113">-Keylength</span><span class="sxs-lookup"><span data-stu-id="b14de-113">-KeyLength</span></span>
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

### <span data-ttu-id="b14de-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b14de-114">-Name</span></span>
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

### <span data-ttu-id="b14de-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b14de-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b14de-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b14de-116">-Confirm</span></span>
<span data-ttu-id="b14de-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b14de-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b14de-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b14de-118">-WhatIf</span></span>
<span data-ttu-id="b14de-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b14de-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b14de-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b14de-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b14de-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b14de-121">CommonParameters</span></span>
<span data-ttu-id="b14de-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b14de-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b14de-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b14de-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b14de-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b14de-124">INPUTS</span></span>

### <span data-ttu-id="b14de-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b14de-125">System.String</span></span>

### <span data-ttu-id="b14de-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="b14de-126">System.UInt32</span></span>

## <span data-ttu-id="b14de-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b14de-127">OUTPUTS</span></span>

### <span data-ttu-id="b14de-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b14de-128">System.String</span></span>

## <span data-ttu-id="b14de-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b14de-129">NOTES</span></span>

## <span data-ttu-id="b14de-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b14de-130">RELATED LINKS</span></span>

[<span data-ttu-id="b14de-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b14de-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="b14de-132">Satz-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b14de-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
