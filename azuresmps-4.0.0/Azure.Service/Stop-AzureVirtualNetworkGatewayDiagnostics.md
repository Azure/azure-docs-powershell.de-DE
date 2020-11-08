---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005946"
---
# <span data-ttu-id="38669-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="38669-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="38669-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38669-102">SYNOPSIS</span></span>
<span data-ttu-id="38669-103">Unterbricht die Ausführung einer virtuellen Netzwerkgateway-Diagnosesitzung.</span><span class="sxs-lookup"><span data-stu-id="38669-103">Stops a running virtual network gateway diagnostics session.</span></span>

## <span data-ttu-id="38669-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38669-104">SYNTAX</span></span>

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="38669-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38669-105">DESCRIPTION</span></span>
<span data-ttu-id="38669-106">Das Cmdlet **Stop-AzureVirtualNetworkGatewayDiagnostics** beendet die Ausführung einer virtuellen Netzwerk-Gateway-Diagnosesitzung.</span><span class="sxs-lookup"><span data-stu-id="38669-106">The **Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet stops a running virtual network gateway diagnostics session.</span></span>
<span data-ttu-id="38669-107">Dieser Befehl speichert die Ergebnisse der Diagnosesitzung in dem Speicherkonto, das vom Start-AzureVirtualNetworkGatewayDiagnostics-Cmdlet angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="38669-107">This command saves the results of the diagnostics session to the storage account that the Start-AzureVirtualNetworkGatewayDiagnostics cmdlet specifies.</span></span>

## <span data-ttu-id="38669-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38669-108">EXAMPLES</span></span>

## <span data-ttu-id="38669-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="38669-109">PARAMETERS</span></span>

### <span data-ttu-id="38669-110">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="38669-110">-GatewayId</span></span>
<span data-ttu-id="38669-111">Gibt die ID eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="38669-111">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="38669-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="38669-112">-Profile</span></span>
<span data-ttu-id="38669-113">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="38669-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="38669-114">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="38669-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="38669-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38669-115">CommonParameters</span></span>
<span data-ttu-id="38669-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38669-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38669-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38669-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38669-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38669-118">INPUTS</span></span>

## <span data-ttu-id="38669-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38669-119">OUTPUTS</span></span>

## <span data-ttu-id="38669-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="38669-120">NOTES</span></span>

## <span data-ttu-id="38669-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38669-121">RELATED LINKS</span></span>

[<span data-ttu-id="38669-122">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="38669-122">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="38669-123">Anfang-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="38669-123">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


