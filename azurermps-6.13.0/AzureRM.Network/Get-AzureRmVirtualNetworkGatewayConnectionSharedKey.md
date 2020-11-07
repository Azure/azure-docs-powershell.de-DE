---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: c2a1a63abb18f5f47ed155f24e8ac73a7bae83ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663131"
---
# <span data-ttu-id="7d83c-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="7d83c-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="7d83c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d83c-102">SYNOPSIS</span></span>
<span data-ttu-id="7d83c-103">Zeigt den freigegebenen Schlüssel an, der für die Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d83c-103">Displays the shared key used for the connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d83c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d83c-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d83c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d83c-105">DESCRIPTION</span></span>
<span data-ttu-id="7d83c-106">Zeigt den freigegebenen Schlüssel an, der für die Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d83c-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="7d83c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d83c-107">EXAMPLES</span></span>

### <span data-ttu-id="7d83c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d83c-108">Example 1</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="7d83c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d83c-109">PARAMETERS</span></span>

### <span data-ttu-id="7d83c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d83c-110">-DefaultProfile</span></span>
<span data-ttu-id="7d83c-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d83c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d83c-112">-Name</span><span class="sxs-lookup"><span data-stu-id="7d83c-112">-Name</span></span>
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

### <span data-ttu-id="7d83c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d83c-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7d83c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d83c-114">CommonParameters</span></span>
<span data-ttu-id="7d83c-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d83c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d83c-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d83c-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d83c-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d83c-117">INPUTS</span></span>

### <span data-ttu-id="7d83c-118">System. String</span><span class="sxs-lookup"><span data-stu-id="7d83c-118">System.String</span></span>

## <span data-ttu-id="7d83c-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d83c-119">OUTPUTS</span></span>

### <span data-ttu-id="7d83c-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7d83c-120">System.String</span></span>

## <span data-ttu-id="7d83c-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d83c-121">NOTES</span></span>

## <span data-ttu-id="7d83c-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d83c-122">RELATED LINKS</span></span>
