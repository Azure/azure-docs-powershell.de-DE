---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b4503c94b750763fa7371f1c5297b0c181e32054
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843744"
---
# <span data-ttu-id="573c2-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="573c2-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="573c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="573c2-102">SYNOPSIS</span></span>

## <span data-ttu-id="573c2-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="573c2-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="573c2-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="573c2-104">DESCRIPTION</span></span>

## <span data-ttu-id="573c2-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="573c2-105">EXAMPLES</span></span>

### <span data-ttu-id="573c2-106">1:</span><span class="sxs-lookup"><span data-stu-id="573c2-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="573c2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="573c2-107">PARAMETERS</span></span>

### <span data-ttu-id="573c2-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573c2-108">-DefaultProfile</span></span>
<span data-ttu-id="573c2-109">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="573c2-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="573c2-110">-Name</span><span class="sxs-lookup"><span data-stu-id="573c2-110">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573c2-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="573c2-111">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="573c2-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="573c2-112">-Confirm</span></span>
<span data-ttu-id="573c2-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="573c2-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573c2-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="573c2-114">-WhatIf</span></span>
<span data-ttu-id="573c2-115">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="573c2-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="573c2-116">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="573c2-116">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573c2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573c2-117">CommonParameters</span></span>
<span data-ttu-id="573c2-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="573c2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573c2-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="573c2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573c2-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="573c2-120">INPUTS</span></span>

### <span data-ttu-id="573c2-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="573c2-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="573c2-122">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="573c2-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="573c2-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="573c2-123">OUTPUTS</span></span>

### <span data-ttu-id="573c2-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="573c2-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="573c2-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="573c2-125">NOTES</span></span>

## <span data-ttu-id="573c2-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="573c2-126">RELATED LINKS</span></span>

