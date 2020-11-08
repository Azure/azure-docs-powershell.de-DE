---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1AB168AA-F466-4C7C-9AD7-0BC7AEEBC932
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8daca2a335f063264fb2e6734948cc1353946e8a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006016"
---
# <span data-ttu-id="7cfe3-101">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="7cfe3-101">Set-AzureVNetGatewayKey</span></span>

## <span data-ttu-id="7cfe3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7cfe3-102">SYNOPSIS</span></span>
<span data-ttu-id="7cfe3-103">Legt den vor-freigegebenen Schlüssel für die Verbindung zwischen einem Azure VPN-Gateway und einer lokalen Netzwerk Website fest.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-103">Sets the pre-shared key for the connection between an Azure VPN gateway and a local network site.</span></span>

## <span data-ttu-id="7cfe3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cfe3-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayKey -VNetName <String> -LocalNetworkSiteName <String> -SharedKey <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7cfe3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7cfe3-105">DESCRIPTION</span></span>
<span data-ttu-id="7cfe3-106">Mit dem Cmdlet **Set-AzureVNetGatewayKey** wird der vorinstallierte Schlüssel für die Verbindung zwischen einem Azure Virtual Private Network (VPN)-Gateway und einer lokalen lokalen Netzwerk Website festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-106">The **Set-AzureVNetGatewayKey** cmdlet sets the pre-shared key for the connection between an Azure virtual private network (VPN) gateway and an on-premises local network site.</span></span>
<span data-ttu-id="7cfe3-107">Der Schlüssel muss mit dem auf dem Gateway der lokalen Netzwerk Website konfigurierten Schlüssel identisch sein.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-107">The key must be equal to the key configured on the gateway of the local network site.</span></span>
<span data-ttu-id="7cfe3-108">Wenn die Schlüssel nicht übereinstimmen, kann eine Verbindung nicht hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-108">If the keys do not match, a connection cannot establish.</span></span>

## <span data-ttu-id="7cfe3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7cfe3-109">EXAMPLES</span></span>

## <span data-ttu-id="7cfe3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cfe3-110">PARAMETERS</span></span>

### <span data-ttu-id="7cfe3-111">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="7cfe3-111">-LocalNetworkSiteName</span></span>
<span data-ttu-id="7cfe3-112">Gibt den Namen der lokalen Netzwerk Website an, die eine Verbindung mit dem virtuellen Netzwerkgateway herstellt.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-112">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="7cfe3-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="7cfe3-113">-Profile</span></span>
<span data-ttu-id="7cfe3-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7cfe3-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7cfe3-116">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7cfe3-116">-SharedKey</span></span>
<span data-ttu-id="7cfe3-117">Gibt den freigegebenen Schlüssel an, der dem VPN-Gateway zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-117">Specifies the shared key to assign to the VPN gateway.</span></span>
<span data-ttu-id="7cfe3-118">Der Wert muss eine alphanumerische Zeichenfolge nicht mehr als 128 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-118">The value must be an alpha-numerical string no longer than 128 characters.</span></span>

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

### <span data-ttu-id="7cfe3-119">-VNetName</span><span class="sxs-lookup"><span data-stu-id="7cfe3-119">-VNetName</span></span>
<span data-ttu-id="7cfe3-120">Gibt das virtuelle Netzwerk an, für das dieses Cmdlet den freigegebenen Schlüssel für die Verbindung festlegt.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-120">Specifies the virtual network for which this cmdlet sets the shared key for the connection.</span></span>

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

### <span data-ttu-id="7cfe3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cfe3-121">CommonParameters</span></span>
<span data-ttu-id="7cfe3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cfe3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cfe3-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cfe3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cfe3-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7cfe3-124">INPUTS</span></span>

## <span data-ttu-id="7cfe3-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7cfe3-125">OUTPUTS</span></span>

## <span data-ttu-id="7cfe3-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="7cfe3-126">NOTES</span></span>

## <span data-ttu-id="7cfe3-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7cfe3-127">RELATED LINKS</span></span>

[<span data-ttu-id="7cfe3-128">Get-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="7cfe3-128">Get-AzureVNetGatewayKey</span></span>](./Get-AzureVNetGatewayKey.md)


