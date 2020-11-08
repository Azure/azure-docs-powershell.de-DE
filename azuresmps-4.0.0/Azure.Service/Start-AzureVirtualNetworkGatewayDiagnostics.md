---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005978"
---
# <span data-ttu-id="5469e-101">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5469e-101">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="5469e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5469e-102">SYNOPSIS</span></span>
<span data-ttu-id="5469e-103">Startet die Diagnose für ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="5469e-103">Starts diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="5469e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5469e-104">SYNTAX</span></span>

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5469e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5469e-105">DESCRIPTION</span></span>
<span data-ttu-id="5469e-106">Das Cmdlet **Start-AzureVirtualNetworkGatewayDiagnostics** startet eine neue Gateway-Diagnosesitzung für ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="5469e-106">The **Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual network gateway.</span></span>
<span data-ttu-id="5469e-107">Es kann immer nur eine Gateway-Diagnosesitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5469e-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="5469e-108">Wenn Sie dieses Cmdlet ausführen, während eine Gateway-Diagnosesitzung ausgeführt wird, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5469e-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="5469e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5469e-109">EXAMPLES</span></span>

## <span data-ttu-id="5469e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5469e-110">PARAMETERS</span></span>

### <span data-ttu-id="5469e-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="5469e-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="5469e-112">Gibt die Aufnahmedauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="5469e-112">Specifies the capture duration in seconds.</span></span>

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

### <span data-ttu-id="5469e-113">-Containername</span><span class="sxs-lookup"><span data-stu-id="5469e-113">-ContainerName</span></span>
<span data-ttu-id="5469e-114">Gibt den Namen eines Azure-Containers an.</span><span class="sxs-lookup"><span data-stu-id="5469e-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="5469e-115">Dieses Cmdlet speichert Ergebnisse in dem Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5469e-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="5469e-116">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="5469e-116">-GatewayId</span></span>
<span data-ttu-id="5469e-117">Gibt die ID eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="5469e-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="5469e-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="5469e-118">-Profile</span></span>
<span data-ttu-id="5469e-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5469e-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5469e-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5469e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5469e-121">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="5469e-121">-StorageContext</span></span>
<span data-ttu-id="5469e-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5469e-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5469e-123">Dieses Cmdlet speichert Ergebnisse unter Verwendung des Speicher Kontexts, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5469e-123">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5469e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5469e-124">CommonParameters</span></span>
<span data-ttu-id="5469e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5469e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5469e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5469e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5469e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5469e-127">INPUTS</span></span>

## <span data-ttu-id="5469e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5469e-128">OUTPUTS</span></span>

## <span data-ttu-id="5469e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="5469e-129">NOTES</span></span>

## <span data-ttu-id="5469e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5469e-130">RELATED LINKS</span></span>

[<span data-ttu-id="5469e-131">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5469e-131">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="5469e-132">Stopp-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5469e-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


