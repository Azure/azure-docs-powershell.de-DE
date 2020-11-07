---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e97e8f3ed5769e4f81175b29f097aa4946d28881
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841835"
---
# <span data-ttu-id="ec718-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ec718-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="ec718-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec718-102">SYNOPSIS</span></span>
<span data-ttu-id="ec718-103">Fügt eine Konfiguration des Back-End-Adresspools zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec718-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="ec718-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec718-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec718-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec718-105">DESCRIPTION</span></span>
<span data-ttu-id="ec718-106">Das Cmdlet **Add-AzLoadBalancerBackend** fügt einem Azure Load Balancer einen Back-End-Adresspool hinzu.</span><span class="sxs-lookup"><span data-stu-id="ec718-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="ec718-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec718-107">EXAMPLES</span></span>

### <span data-ttu-id="ec718-108">Beispiel 1 Hinzufügen einer Konfiguration des Back-End-Adresspools zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="ec718-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="ec718-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab, fügt den Back-End-Adresspool mit dem Namen BackendAddressPool02 zu MyLoadBalancer hinzu und verwendet dann das Cmdlet " **Satz-AzLoadBalancer** ", um MyLoadBalancer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ec718-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="ec718-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec718-110">PARAMETERS</span></span>

### <span data-ttu-id="ec718-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec718-111">-DefaultProfile</span></span>
<span data-ttu-id="ec718-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec718-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec718-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ec718-113">-LoadBalancer</span></span>
<span data-ttu-id="ec718-114">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ec718-114">Specifies a **LoadBalancer** object.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec718-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ec718-115">-Name</span></span>
<span data-ttu-id="ec718-116">Gibt den Namen der hinzuzufügenden Konfiguration des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="ec718-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="ec718-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec718-117">CommonParameters</span></span>
<span data-ttu-id="ec718-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec718-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec718-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec718-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec718-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec718-120">INPUTS</span></span>

### <span data-ttu-id="ec718-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ec718-121">PSLoadBalancer</span></span>
<span data-ttu-id="ec718-122">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ec718-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ec718-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec718-123">OUTPUTS</span></span>

### <span data-ttu-id="ec718-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ec718-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ec718-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec718-125">NOTES</span></span>

## <span data-ttu-id="ec718-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec718-126">RELATED LINKS</span></span>

[<span data-ttu-id="ec718-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ec718-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ec718-128">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ec718-128">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="ec718-129">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ec718-129">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="ec718-130">Neu – AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ec718-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="ec718-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ec718-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


