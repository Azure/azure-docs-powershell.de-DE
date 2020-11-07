---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 11ac1df9032f86d5265b78efcfc02c08b441cdd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841351"
---
# <span data-ttu-id="b579a-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b579a-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b579a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b579a-102">SYNOPSIS</span></span>
<span data-ttu-id="b579a-103">Erstellt eine Konfiguration des Back-End-Adresspools für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="b579a-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="b579a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b579a-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b579a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b579a-105">DESCRIPTION</span></span>
<span data-ttu-id="b579a-106">Das Cmdlet **New-AzLoadBalancerBackendAddressPoolConfig** erstellt eine Konfiguration des Back-End-Adresspools für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="b579a-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="b579a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b579a-107">EXAMPLES</span></span>

### <span data-ttu-id="b579a-108">Beispiel 1: Erstellen einer Konfiguration des Back-End-Adresspools für ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="b579a-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="b579a-109">Dieser Befehl erstellt eine Konfiguration des Back-End-Adresspools mit dem Namen BackendAddressPool02 für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="b579a-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="b579a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b579a-110">PARAMETERS</span></span>

### <span data-ttu-id="b579a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b579a-111">-DefaultProfile</span></span>
<span data-ttu-id="b579a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b579a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b579a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b579a-113">-Name</span></span>
<span data-ttu-id="b579a-114">Gibt den Namen der zu erstellende Adresspool Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b579a-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="b579a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b579a-115">CommonParameters</span></span>
<span data-ttu-id="b579a-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b579a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b579a-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b579a-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b579a-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b579a-118">INPUTS</span></span>

## <span data-ttu-id="b579a-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b579a-119">OUTPUTS</span></span>

### <span data-ttu-id="b579a-120">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b579a-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b579a-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="b579a-121">NOTES</span></span>

## <span data-ttu-id="b579a-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b579a-122">RELATED LINKS</span></span>

[<span data-ttu-id="b579a-123">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b579a-123">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b579a-124">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b579a-124">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b579a-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b579a-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


