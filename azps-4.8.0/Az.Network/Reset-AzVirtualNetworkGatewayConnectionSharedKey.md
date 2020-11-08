---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166223"
---
# <span data-ttu-id="4d785-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4d785-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="4d785-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d785-102">SYNOPSIS</span></span>
<span data-ttu-id="4d785-103">Setzt den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="4d785-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="4d785-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d785-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d785-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d785-105">DESCRIPTION</span></span>
<span data-ttu-id="4d785-106">Setzt den freigegebenen Schlüssel der virtuellen Netzwerkgateway-Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="4d785-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="4d785-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d785-107">EXAMPLES</span></span>

### <span data-ttu-id="4d785-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="4d785-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="4d785-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d785-109">PARAMETERS</span></span>

### <span data-ttu-id="4d785-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d785-110">-DefaultProfile</span></span>
<span data-ttu-id="4d785-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d785-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d785-112">-Force</span><span class="sxs-lookup"><span data-stu-id="4d785-112">-Force</span></span>
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

### <span data-ttu-id="4d785-113">-Keylength</span><span class="sxs-lookup"><span data-stu-id="4d785-113">-KeyLength</span></span>
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

### <span data-ttu-id="4d785-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4d785-114">-Name</span></span>
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

### <span data-ttu-id="4d785-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d785-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="4d785-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d785-116">-Confirm</span></span>
<span data-ttu-id="4d785-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d785-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d785-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d785-118">-WhatIf</span></span>
<span data-ttu-id="4d785-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d785-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d785-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d785-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d785-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d785-121">CommonParameters</span></span>
<span data-ttu-id="4d785-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d785-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d785-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d785-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d785-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d785-124">INPUTS</span></span>

### <span data-ttu-id="4d785-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4d785-125">System.String</span></span>

### <span data-ttu-id="4d785-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="4d785-126">System.UInt32</span></span>

## <span data-ttu-id="4d785-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d785-127">OUTPUTS</span></span>

### <span data-ttu-id="4d785-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4d785-128">System.String</span></span>

## <span data-ttu-id="4d785-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d785-129">NOTES</span></span>

## <span data-ttu-id="4d785-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d785-130">RELATED LINKS</span></span>

[<span data-ttu-id="4d785-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4d785-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="4d785-132">Satz-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4d785-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
