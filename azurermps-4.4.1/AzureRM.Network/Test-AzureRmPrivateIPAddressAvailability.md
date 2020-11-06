---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 880e079d5facec2edc20f38d7d1e1d4c9ba41e41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497033"
---
# <span data-ttu-id="2cc63-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="2cc63-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="2cc63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cc63-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc63-103">Testen der Verfügbarkeit einer privaten IP-Adresse in einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2cc63-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cc63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cc63-104">SYNTAX</span></span>

### <span data-ttu-id="2cc63-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="2cc63-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc63-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="2cc63-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cc63-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cc63-107">DESCRIPTION</span></span>
<span data-ttu-id="2cc63-108">Das Cmdlet **Test-AzureRmPrivateIPAddressAvailability** testet, ob eine angegebene private IP-Adresse in einem virtuellen Netzwerk zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="2cc63-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="2cc63-109">Dieses Cmdlet gibt eine Liste der verfügbaren privaten IP-Adressen zurück, wenn die angeforderte private IP-Adresse übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="2cc63-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="2cc63-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cc63-110">EXAMPLES</span></span>

### <span data-ttu-id="2cc63-111">Beispiel 1: testen, ob eine IP-Adresse über die Pipeline verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="2cc63-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="2cc63-112">Dieser Befehl ruft ein virtuelles Netzwerk ab und verwendet den Pipelineoperator, um ihn an **Test-AzureRmPrivateIPAddressAvailability** zu übergeben, wodurch überprüft wird, ob die angegebene private IP-Adresse verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2cc63-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="2cc63-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cc63-113">PARAMETERS</span></span>

### <span data-ttu-id="2cc63-114">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="2cc63-114">-IPAddress</span></span>
<span data-ttu-id="2cc63-115">Gibt die zu testende IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="2cc63-115">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="2cc63-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc63-116">-ResourceGroupName</span></span>
<span data-ttu-id="2cc63-117">Gibt den Namen der Ressourcengruppe für das virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="2cc63-117">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc63-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2cc63-118">-VirtualNetwork</span></span>
<span data-ttu-id="2cc63-119">Gibt ein **PSVirtualNetwork** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2cc63-119">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc63-120">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2cc63-120">-VirtualNetworkName</span></span>
<span data-ttu-id="2cc63-121">Gibt den Namen des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="2cc63-121">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc63-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc63-122">-DefaultProfile</span></span>
<span data-ttu-id="2cc63-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2cc63-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cc63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc63-124">CommonParameters</span></span>
<span data-ttu-id="2cc63-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc63-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc63-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc63-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cc63-127">INPUTS</span></span>

### <span data-ttu-id="2cc63-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2cc63-128">PSVirtualNetwork</span></span>
<span data-ttu-id="2cc63-129">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2cc63-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="2cc63-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cc63-130">OUTPUTS</span></span>

### <span data-ttu-id="2cc63-131">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="2cc63-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="2cc63-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cc63-132">NOTES</span></span>

## <span data-ttu-id="2cc63-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cc63-133">RELATED LINKS</span></span>

[<span data-ttu-id="2cc63-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2cc63-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


