---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: 62fc89cefadc91445a64850d6a0e5ee23d6163f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849176"
---
# <span data-ttu-id="7035e-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7035e-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="7035e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7035e-102">SYNOPSIS</span></span>
<span data-ttu-id="7035e-103">Ruft Informationen zu VPN-Client Sperrungs Zertifikaten ab.</span><span class="sxs-lookup"><span data-stu-id="7035e-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7035e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7035e-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7035e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7035e-105">DESCRIPTION</span></span>
<span data-ttu-id="7035e-106">Das Cmdlet " **Get-AzureRmVpnClientRevokedCertificate** " gibt Informationen zu den Client Sperr Zertifikaten zurück, die einem virtuellen Netzwerkgateway zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="7035e-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="7035e-107">Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="7035e-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="7035e-108">Mit **Get-AzureRmVpnClientRevokedCertificate** können Sie Informationen zu allen Client Sperr Zertifikaten auf dem Gateway zurückgeben oder mithilfe des *VpnClientRevokedCertificateName* -Parameters Informationen zu einem einzelnen Zertifikat abrufen.</span><span class="sxs-lookup"><span data-stu-id="7035e-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="7035e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7035e-109">EXAMPLES</span></span>

### <span data-ttu-id="7035e-110">Beispiel 1: Abrufen von Informationen zu allen Client Sperr Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="7035e-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="7035e-111">Dieser Befehl ruft Informationen zu allen Client Sperr Zertifikaten ab, die dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetworkGateway zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7035e-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="7035e-112">Beispiel 2: Abrufen von Informationen zu bestimmten Client Sperr Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="7035e-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="7035e-113">Dieser Befehl ist eine Variation des Befehls, der in Beispiel 1 gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7035e-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="7035e-114">In diesem Fall wird jedoch der *VpnClientRevokedCertificateName* -Parameter verwendet, um die zurückgegebenen Daten auf ein bestimmtes vom Client gesperrtes Zertifikat zu begrenzen: das Zertifikat mit dem Namen ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="7035e-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="7035e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7035e-115">PARAMETERS</span></span>

### <span data-ttu-id="7035e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7035e-116">-DefaultProfile</span></span>
<span data-ttu-id="7035e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7035e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7035e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7035e-118">-ResourceGroupName</span></span>
<span data-ttu-id="7035e-119">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7035e-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="7035e-120">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="7035e-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7035e-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="7035e-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="7035e-122">Gibt den Namen des virtuellen Netzwerkgateways an, in dem die gesperrten Zertifikatinformationen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="7035e-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7035e-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="7035e-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="7035e-124">Gibt den Namen des VPN-Clientzertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7035e-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7035e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7035e-125">CommonParameters</span></span>
<span data-ttu-id="7035e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7035e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7035e-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7035e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7035e-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7035e-128">INPUTS</span></span>

## <span data-ttu-id="7035e-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7035e-129">OUTPUTS</span></span>

###  
<span data-ttu-id="7035e-130">**Get-AzureRmVpnClientRevokedCertificate** gibt Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="7035e-130">**Get-AzureRmVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="7035e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7035e-131">NOTES</span></span>

## <span data-ttu-id="7035e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7035e-132">RELATED LINKS</span></span>

[<span data-ttu-id="7035e-133">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7035e-133">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="7035e-134">Neu – AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7035e-134">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="7035e-135">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="7035e-135">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


