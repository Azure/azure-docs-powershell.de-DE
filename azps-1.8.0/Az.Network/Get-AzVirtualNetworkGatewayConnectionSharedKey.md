---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 071843c47ea3a8f97125746aa80fdb90eb1cb566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660682"
---
# <span data-ttu-id="6dc4f-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6dc4f-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="6dc4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6dc4f-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc4f-103">Zeigt den freigegebenen Schlüssel an, der für die Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6dc4f-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="6dc4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dc4f-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dc4f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6dc4f-105">DESCRIPTION</span></span>
<span data-ttu-id="6dc4f-106">Zeigt den freigegebenen Schlüssel an, der für die Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6dc4f-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="6dc4f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6dc4f-107">EXAMPLES</span></span>

### <span data-ttu-id="6dc4f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6dc4f-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="6dc4f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dc4f-109">PARAMETERS</span></span>

### <span data-ttu-id="6dc4f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc4f-110">-DefaultProfile</span></span>
<span data-ttu-id="6dc4f-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6dc4f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dc4f-112">-Name</span><span class="sxs-lookup"><span data-stu-id="6dc4f-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc4f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dc4f-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6dc4f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc4f-114">CommonParameters</span></span>
<span data-ttu-id="6dc4f-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc4f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc4f-116">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dc4f-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc4f-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6dc4f-117">INPUTS</span></span>

### <span data-ttu-id="6dc4f-118">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc4f-118">System.String</span></span>

## <span data-ttu-id="6dc4f-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6dc4f-119">OUTPUTS</span></span>

### <span data-ttu-id="6dc4f-120">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc4f-120">System.String</span></span>

## <span data-ttu-id="6dc4f-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="6dc4f-121">NOTES</span></span>

## <span data-ttu-id="6dc4f-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6dc4f-122">RELATED LINKS</span></span>

[<span data-ttu-id="6dc4f-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6dc4f-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="6dc4f-124">Satz-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="6dc4f-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
