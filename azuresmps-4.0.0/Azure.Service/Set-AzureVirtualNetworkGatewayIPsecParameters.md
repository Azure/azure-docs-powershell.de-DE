---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 150EE0DC-07CD-4E24-AF70-0C1A7BB61433
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b663ced66318335afb1fe4c3bf0e6a1520ede7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006618"
---
# <span data-ttu-id="124e8-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="124e8-101">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="124e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="124e8-102">SYNOPSIS</span></span>
<span data-ttu-id="124e8-103">Legt IPSec-Parameter für ein virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="124e8-103">Sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="124e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="124e8-104">SYNTAX</span></span>

```
Set-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="124e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="124e8-105">DESCRIPTION</span></span>
<span data-ttu-id="124e8-106">Das Cmdlet " **Set-AzureVirtualNetworkGatewayIPsecParameters** " legt IPSec-Parameter für ein virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="124e8-106">The **Set-AzureVirtualNetworkGatewayIPsecParameters** cmdlet sets IPsec parameters for a virtual network gateway.</span></span>

## <span data-ttu-id="124e8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="124e8-107">EXAMPLES</span></span>

## <span data-ttu-id="124e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="124e8-108">PARAMETERS</span></span>

### <span data-ttu-id="124e8-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="124e8-109">-ConnectedEntityId</span></span>
<span data-ttu-id="124e8-110">Gibt die ID einer verbundenen Entität an.</span><span class="sxs-lookup"><span data-stu-id="124e8-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="124e8-111">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="124e8-111">-EncryptionType</span></span>
<span data-ttu-id="124e8-112">Gibt den Verschlüsselungstyp für das virtuelle Netzwerkgateway an.</span><span class="sxs-lookup"><span data-stu-id="124e8-112">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="124e8-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="124e8-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="124e8-114">NoEncryption</span><span class="sxs-lookup"><span data-stu-id="124e8-114">NoEncryption</span></span>
- <span data-ttu-id="124e8-115">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="124e8-115">RequireEncryption</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e8-116">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="124e8-116">-GatewayId</span></span>
<span data-ttu-id="124e8-117">Gibt die ID eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="124e8-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="124e8-118">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="124e8-118">-PfsGroup</span></span>
<span data-ttu-id="124e8-119">Gibt die Gruppe "Perfect Forward Heimlichkeit (PFS)" an.</span><span class="sxs-lookup"><span data-stu-id="124e8-119">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="124e8-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="124e8-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="124e8-121">PFS1</span><span class="sxs-lookup"><span data-stu-id="124e8-121">PFS1</span></span>
- <span data-ttu-id="124e8-122">Keine</span><span class="sxs-lookup"><span data-stu-id="124e8-122">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e8-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="124e8-123">-Profile</span></span>
<span data-ttu-id="124e8-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="124e8-124">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="124e8-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="124e8-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e8-126">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="124e8-126">-SADataSizeKilobytes</span></span>
<span data-ttu-id="124e8-127">Gibt die Größe der Sicherheitszuordnung (SA) in Kilobyte an.</span><span class="sxs-lookup"><span data-stu-id="124e8-127">Specifies the size, in kilobytes, of the security association (SA).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e8-128">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="124e8-128">-SALifetimeSeconds</span></span>
<span data-ttu-id="124e8-129">Gibt den Zeitraum (in Sekunden) der Sicherheitszuordnung an.</span><span class="sxs-lookup"><span data-stu-id="124e8-129">Specifies the period, in seconds, of the security association.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="124e8-130">CommonParameters</span></span>
<span data-ttu-id="124e8-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="124e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="124e8-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="124e8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="124e8-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="124e8-133">INPUTS</span></span>

## <span data-ttu-id="124e8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="124e8-134">OUTPUTS</span></span>

## <span data-ttu-id="124e8-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="124e8-135">NOTES</span></span>

## <span data-ttu-id="124e8-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="124e8-136">RELATED LINKS</span></span>

[<span data-ttu-id="124e8-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="124e8-137">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Get-AzureVirtualNetworkGatewayIPsecParameters.md)


