---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: d721feb80598e343fc5757eceee90136bbc51ae9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505601"
---
# <span data-ttu-id="778d1-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="778d1-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="778d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="778d1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="778d1-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="778d1-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="778d1-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="778d1-104">DESCRIPTION</span></span>

## <span data-ttu-id="778d1-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="778d1-105">EXAMPLES</span></span>

### <span data-ttu-id="778d1-106">1:</span><span class="sxs-lookup"><span data-stu-id="778d1-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="778d1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="778d1-107">PARAMETERS</span></span>

### <span data-ttu-id="778d1-108">-Name</span><span class="sxs-lookup"><span data-stu-id="778d1-108">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="778d1-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="778d1-109">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="778d1-110">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="778d1-110">-Confirm</span></span>
<span data-ttu-id="778d1-111">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="778d1-111">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="778d1-112">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="778d1-112">-WhatIf</span></span>
<span data-ttu-id="778d1-113">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="778d1-113">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="778d1-114">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="778d1-114">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="778d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778d1-115">-DefaultProfile</span></span>
<span data-ttu-id="778d1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="778d1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="778d1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778d1-117">CommonParameters</span></span>
<span data-ttu-id="778d1-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="778d1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778d1-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="778d1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778d1-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="778d1-120">INPUTS</span></span>

### <span data-ttu-id="778d1-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="778d1-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="778d1-122">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="778d1-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="778d1-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="778d1-123">OUTPUTS</span></span>

### <span data-ttu-id="778d1-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="778d1-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="778d1-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="778d1-125">NOTES</span></span>

## <span data-ttu-id="778d1-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="778d1-126">RELATED LINKS</span></span>

