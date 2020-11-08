---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177477"
---
# <span data-ttu-id="90093-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="90093-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="90093-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90093-102">SYNOPSIS</span></span>
<span data-ttu-id="90093-103">Erstellt eine IPSec-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="90093-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="90093-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90093-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90093-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90093-105">DESCRIPTION</span></span>
<span data-ttu-id="90093-106">Das New-AzIpsecPolicy-Cmdlet erstellt einen IPSec-Richtlinienvorschlag zur Verwendung in einer virtuellen Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="90093-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="90093-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90093-107">EXAMPLES</span></span>

### <span data-ttu-id="90093-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90093-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="90093-109">Erstellen einer IPSec-Richtlinie, die für eine neue virtuelle Netzwerkgateway-Verbindung verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="90093-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="90093-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90093-110">PARAMETERS</span></span>

### <span data-ttu-id="90093-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90093-111">-DefaultProfile</span></span>
<span data-ttu-id="90093-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90093-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90093-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="90093-113">-DhGroup</span></span>
<span data-ttu-id="90093-114">Die in IKE Phase 1 für Initial SA verwendeten DH-Gruppen</span><span class="sxs-lookup"><span data-stu-id="90093-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90093-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="90093-115">-IkeEncryption</span></span>
<span data-ttu-id="90093-116">Der IKE-Verschlüsselungsalgorithmus (IKE-Phase 1)</span><span class="sxs-lookup"><span data-stu-id="90093-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90093-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="90093-117">-IkeIntegrity</span></span>
<span data-ttu-id="90093-118">Der IKE-Integritätsalgorithmus (IKE-Phase 1)</span><span class="sxs-lookup"><span data-stu-id="90093-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90093-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="90093-119">-IpsecEncryption</span></span>
<span data-ttu-id="90093-120">Der IPSec-Verschlüsselungsalgorithmus (IKE-Phase 2)</span><span class="sxs-lookup"><span data-stu-id="90093-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90093-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="90093-121">-IpsecIntegrity</span></span>
<span data-ttu-id="90093-122">Der IPSec-Integritätsalgorithmus (IKE-Phase 2)</span><span class="sxs-lookup"><span data-stu-id="90093-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90093-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="90093-123">-PfsGroup</span></span>
<span data-ttu-id="90093-124">Die in IKE Phase 2 für neue untergeordnete SA verwendeten DH-Gruppen</span><span class="sxs-lookup"><span data-stu-id="90093-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90093-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="90093-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="90093-126">Die IPSec-Sicherheitszuordnung (auch als Schnellmodus oder Phase 2 SA bezeichnet) Nutzlast-Größe in KB</span><span class="sxs-lookup"><span data-stu-id="90093-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90093-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="90093-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="90093-128">Die IPSec-Sicherheitszuordnung (auch als Schnellmodus oder Phase 2 SA bezeichnet) Lebensdauer in Sekunden</span><span class="sxs-lookup"><span data-stu-id="90093-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90093-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90093-129">CommonParameters</span></span>
<span data-ttu-id="90093-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90093-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90093-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90093-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90093-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90093-132">INPUTS</span></span>

### <span data-ttu-id="90093-133">Keine</span><span class="sxs-lookup"><span data-stu-id="90093-133">None</span></span>

## <span data-ttu-id="90093-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90093-134">OUTPUTS</span></span>

### <span data-ttu-id="90093-135">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="90093-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="90093-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="90093-136">NOTES</span></span>

## <span data-ttu-id="90093-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90093-137">RELATED LINKS</span></span>
