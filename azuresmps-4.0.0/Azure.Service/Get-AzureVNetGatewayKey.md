---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8AD101BA-9275-4B2B-BB31-99FC34B8D1E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ac1d91bc084c9e1b17debf154b2a44c144ce312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006481"
---
# <span data-ttu-id="882c3-101">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="882c3-101">Get-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="882c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="882c3-102">SYNOPSIS</span></span>
<span data-ttu-id="882c3-103">Ruft den vor-freigegebenen Schlüssel für die Verbindung zwischen einem virtuellen Netzwerkgateway und einer lokalen Netzwerk Website ab.</span><span class="sxs-lookup"><span data-stu-id="882c3-103">Gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="882c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="882c3-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="882c3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="882c3-105">DESCRIPTION</span></span>
<span data-ttu-id="882c3-106">Das Cmdlet " **Get-AzureVNetGatewayKey** " Ruft den vor-freigegebenen Schlüssel für die Verbindung zwischen einem virtuellen Netzwerkgateway und einer lokalen Netzwerk Website ab.</span><span class="sxs-lookup"><span data-stu-id="882c3-106">The **Get-AzureVNetGatewayKey** cmdlet gets the pre-shared key for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="882c3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="882c3-107">EXAMPLES</span></span>

## <span data-ttu-id="882c3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="882c3-108">PARAMETERS</span></span>

### <span data-ttu-id="882c3-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="882c3-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="882c3-110">Gibt den Namen der lokalen Netzwerk Website an, die eine Verbindung mit dem virtuellen Netzwerkgateway herstellt.</span><span class="sxs-lookup"><span data-stu-id="882c3-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="882c3-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="882c3-111">-Profile</span></span>
<span data-ttu-id="882c3-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="882c3-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="882c3-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="882c3-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="882c3-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="882c3-114">-VNetName</span></span>
<span data-ttu-id="882c3-115">Gibt das virtuelle Netzwerk an, für das dieses Cmdlet den freigegebenen Schlüssel für Verbindungen erhält.</span><span class="sxs-lookup"><span data-stu-id="882c3-115">Specifies the virtual network for which this cmdlet gets the shared key for connections.</span></span>

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

### <span data-ttu-id="882c3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882c3-116">CommonParameters</span></span>
<span data-ttu-id="882c3-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="882c3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882c3-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="882c3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882c3-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="882c3-119">INPUTS</span></span>

## <span data-ttu-id="882c3-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="882c3-120">OUTPUTS</span></span>

## <span data-ttu-id="882c3-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="882c3-121">NOTES</span></span>

## <span data-ttu-id="882c3-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="882c3-122">RELATED LINKS</span></span>

[<span data-ttu-id="882c3-123">Satz-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="882c3-123">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


