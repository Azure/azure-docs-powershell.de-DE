---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: cbac48c8f9f79dc74453222c162fee105cce2fdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499745"
---
# <span data-ttu-id="8a3c9-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8a3c9-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="8a3c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="8a3c9-103">Erstellt eine Konfiguration des Back-End-Adresspools für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="8a3c9-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a3c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a3c9-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a3c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a3c9-105">DESCRIPTION</span></span>
<span data-ttu-id="8a3c9-106">Das Cmdlet **New-AzureRmLoadBalancerBackendAddressPoolConfig** erstellt eine Konfiguration des Back-End-Adresspools für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="8a3c9-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8a3c9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a3c9-107">EXAMPLES</span></span>

### <span data-ttu-id="8a3c9-108">Beispiel 1: Erstellen einer Konfiguration des Back-End-Adresspools für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="8a3c9-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="8a3c9-109">Dieser Befehl erstellt eine Konfiguration des Back-End-Adresspools mit dem Namen BackendAddressPool02 für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="8a3c9-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="8a3c9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a3c9-110">PARAMETERS</span></span>

### <span data-ttu-id="8a3c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a3c9-111">-DefaultProfile</span></span>
<span data-ttu-id="8a3c9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a3c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a3c9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8a3c9-113">-Name</span></span>
<span data-ttu-id="8a3c9-114">Gibt den Namen der zu erstellende Adresspool Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="8a3c9-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="8a3c9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a3c9-115">CommonParameters</span></span>
<span data-ttu-id="8a3c9-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a3c9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a3c9-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a3c9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a3c9-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a3c9-118">INPUTS</span></span>

### <span data-ttu-id="8a3c9-119">Keine</span><span class="sxs-lookup"><span data-stu-id="8a3c9-119">None</span></span>
<span data-ttu-id="8a3c9-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8a3c9-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a3c9-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a3c9-121">OUTPUTS</span></span>

### <span data-ttu-id="8a3c9-122">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8a3c9-122">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="8a3c9-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a3c9-123">NOTES</span></span>

## <span data-ttu-id="8a3c9-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a3c9-124">RELATED LINKS</span></span>

[<span data-ttu-id="8a3c9-125">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8a3c9-125">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8a3c9-126">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8a3c9-126">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8a3c9-127">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8a3c9-127">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


