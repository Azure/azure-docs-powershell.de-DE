---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: f68709cad84adb6904e509472b1c960d6134144c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848700"
---
# <span data-ttu-id="73fcd-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="73fcd-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="73fcd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73fcd-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73fcd-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="73fcd-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73fcd-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73fcd-104">DESCRIPTION</span></span>

## <span data-ttu-id="73fcd-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73fcd-105">EXAMPLES</span></span>

### <span data-ttu-id="73fcd-106">1:</span><span class="sxs-lookup"><span data-stu-id="73fcd-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="73fcd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="73fcd-107">PARAMETERS</span></span>

### <span data-ttu-id="73fcd-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73fcd-108">-DefaultProfile</span></span>
<span data-ttu-id="73fcd-109">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73fcd-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73fcd-110">-Name</span><span class="sxs-lookup"><span data-stu-id="73fcd-110">-Name</span></span>
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

### <span data-ttu-id="73fcd-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73fcd-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="73fcd-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73fcd-112">-Confirm</span></span>
<span data-ttu-id="73fcd-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73fcd-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73fcd-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73fcd-114">-WhatIf</span></span>
<span data-ttu-id="73fcd-115">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73fcd-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73fcd-116">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73fcd-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73fcd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73fcd-117">CommonParameters</span></span>
<span data-ttu-id="73fcd-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73fcd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73fcd-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73fcd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73fcd-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73fcd-120">INPUTS</span></span>

### <span data-ttu-id="73fcd-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73fcd-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="73fcd-122">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="73fcd-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="73fcd-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73fcd-123">OUTPUTS</span></span>

### <span data-ttu-id="73fcd-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73fcd-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="73fcd-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="73fcd-125">NOTES</span></span>

## <span data-ttu-id="73fcd-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73fcd-126">RELATED LINKS</span></span>

