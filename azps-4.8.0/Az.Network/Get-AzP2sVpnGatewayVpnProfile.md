---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165260"
---
# <span data-ttu-id="c3e6c-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="c3e6c-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="c3e6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e6c-103">Generiert eine SAS-URL für den Kunden zum Herunterladen des VPN-Profils für den Point-to-Site-Client-Setup, um auf eine Standort Konnektivität mit P2SVpnGateway zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="c3e6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3e6c-104">SYNTAX</span></span>

### <span data-ttu-id="c3e6c-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3e6c-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e6c-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c3e6c-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e6c-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c3e6c-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e6c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3e6c-108">DESCRIPTION</span></span>
<span data-ttu-id="c3e6c-109">Das Cmdlet " **Get-AzP2sVpnGatewayVpnProfile** " ermöglicht es Ihnen, eine SAS-URL für den Kunden zum Herunterladen des VPN-Profils für einen Point-to-Site-Client-Setup zu generieren, um auf eine Standort Konnektivität mit P2SVpnGateway zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="c3e6c-110">Zeigen Sie auf das Setup des Website Clients mit diesem VPN-Profil kann nur eine Verbindung mit diesem bestimmten P2SVpnGateway hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="c3e6c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3e6c-111">EXAMPLES</span></span>

### <span data-ttu-id="c3e6c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3e6c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="c3e6c-113">Das Cmdlet " **Get-AzP2sVpnGatewayVpnProfile** " ermöglicht es Ihnen, eine SAS-URL für den Kunden zum Herunterladen des VPN-Profils für einen Point-to-Site-Client-Setup zu generieren, um auf eine Standort Konnektivität mit P2SVpnGateway zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="c3e6c-114">ProfileUrl zeigt die SAS-URL an, aus der der Kunde das VPN-Profil für die Einrichtung eines Point-to-Site-Clients herunterladen kann</span><span class="sxs-lookup"><span data-stu-id="c3e6c-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="c3e6c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3e6c-115">PARAMETERS</span></span>

### <span data-ttu-id="c3e6c-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="c3e6c-116">-AuthenticationMethod</span></span>
<span data-ttu-id="c3e6c-117">Authentifizierungsmethode</span><span class="sxs-lookup"><span data-stu-id="c3e6c-117">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e6c-118">-DefaultProfile</span></span>
<span data-ttu-id="c3e6c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3e6c-120">-InputObject</span></span>
<span data-ttu-id="c3e6c-121">Das zu ändernde P2S-VPN-Gateway-Objekt</span><span class="sxs-lookup"><span data-stu-id="c3e6c-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c3e6c-122">-Name</span></span>
<span data-ttu-id="c3e6c-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e6c-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3e6c-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6c-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c3e6c-126">-ResourceId</span></span>
<span data-ttu-id="c3e6c-127">Die Azure-Ressourcen-ID des zu ändernden P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e6c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e6c-128">CommonParameters</span></span>
<span data-ttu-id="c3e6c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e6c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e6c-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e6c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e6c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3e6c-131">INPUTS</span></span>

### <span data-ttu-id="c3e6c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c3e6c-132">System.String</span></span>
<span data-ttu-id="c3e6c-133">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c3e6c-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="c3e6c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3e6c-134">OUTPUTS</span></span>

### <span data-ttu-id="c3e6c-135">Microsoft. Azure. Commands. Network. Models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="c3e6c-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="c3e6c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3e6c-136">NOTES</span></span>

## <span data-ttu-id="c3e6c-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3e6c-137">RELATED LINKS</span></span>
