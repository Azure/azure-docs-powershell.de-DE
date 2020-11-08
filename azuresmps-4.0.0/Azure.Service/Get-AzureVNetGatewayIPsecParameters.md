---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006482"
---
# <span data-ttu-id="06670-101">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="06670-101">Get-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="06670-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06670-102">SYNOPSIS</span></span>
<span data-ttu-id="06670-103">Ruft IPSec-Parameter für die Verbindung zwischen einem virtuellen Netzwerkgateway und einer lokalen Netzwerk Website ab.</span><span class="sxs-lookup"><span data-stu-id="06670-103">Gets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="06670-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06670-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="06670-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06670-105">DESCRIPTION</span></span>
<span data-ttu-id="06670-106">Das Cmdlet " **Get-AzureVNetGatewayIPsecParameters** " Ruft aktuelle IPSec-Parameter (Internet Protocol Security) und IKE-Parameter für die Verbindung zwischen einem virtuellen Netzwerkgateway und einer lokalen Netzwerk Website ab.</span><span class="sxs-lookup"><span data-stu-id="06670-106">The **Get-AzureVNetGatewayIPsecParameters** cmdlet gets current Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="06670-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06670-107">EXAMPLES</span></span>

## <span data-ttu-id="06670-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="06670-108">PARAMETERS</span></span>

### <span data-ttu-id="06670-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="06670-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="06670-110">Gibt den Namen der lokalen Netzwerk Website an, die eine Verbindung mit dem virtuellen Netzwerkgateway herstellt.</span><span class="sxs-lookup"><span data-stu-id="06670-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="06670-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="06670-111">-Profile</span></span>
<span data-ttu-id="06670-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="06670-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="06670-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="06670-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06670-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="06670-114">-VNetName</span></span>
<span data-ttu-id="06670-115">Gibt das virtuelle Netzwerk an, für das dieses Cmdlet IPSec-Parameter für die Verbindung erhält.</span><span class="sxs-lookup"><span data-stu-id="06670-115">Specifies the virtual network for which this cmdlet gets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="06670-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06670-116">CommonParameters</span></span>
<span data-ttu-id="06670-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06670-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06670-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06670-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06670-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06670-119">INPUTS</span></span>

## <span data-ttu-id="06670-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06670-120">OUTPUTS</span></span>

## <span data-ttu-id="06670-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="06670-121">NOTES</span></span>

## <span data-ttu-id="06670-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06670-122">RELATED LINKS</span></span>

[<span data-ttu-id="06670-123">Satz-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="06670-123">Set-AzureVNetGatewayIPsecParameters</span></span>](./Set-AzureVNetGatewayIPsecParameters.md)


