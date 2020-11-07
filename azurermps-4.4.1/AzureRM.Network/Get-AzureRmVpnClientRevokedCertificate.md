---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8171a87ea744eb708e65c71a1d25b13190b6f0fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665361"
---
# <span data-ttu-id="0481e-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="0481e-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="0481e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0481e-102">SYNOPSIS</span></span>
<span data-ttu-id="0481e-103">Ruft Informationen zu VPN-Client Sperrungs Zertifikaten ab.</span><span class="sxs-lookup"><span data-stu-id="0481e-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0481e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0481e-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0481e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0481e-105">DESCRIPTION</span></span>
<span data-ttu-id="0481e-106">Das Cmdlet " **Get-AzureRmVpnClientRevokedCertificate** " gibt Informationen zu den Client Sperr Zertifikaten zurück, die einem virtuellen Netzwerkgateway zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="0481e-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="0481e-107">Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0481e-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="0481e-108">Mit **Get-AzureRmVpnClientRevokedCertificate** können Sie Informationen zu allen Client Sperr Zertifikaten auf dem Gateway zurückgeben oder mithilfe des *VpnClientRevokedCertificateName* -Parameters Informationen zu einem einzelnen Zertifikat abrufen.</span><span class="sxs-lookup"><span data-stu-id="0481e-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="0481e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0481e-109">EXAMPLES</span></span>

### <span data-ttu-id="0481e-110">Beispiel 1: Abrufen von Informationen zu allen Client Sperr Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="0481e-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="0481e-111">Dieser Befehl ruft Informationen zu allen Client Sperr Zertifikaten ab, die dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetworkGateway zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0481e-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="0481e-112">Beispiel 2: Abrufen von Informationen zu bestimmten Client Sperr Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="0481e-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="0481e-113">Dieser Befehl ist eine Variation des Befehls, der in Beispiel 1 gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0481e-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="0481e-114">In diesem Fall wird jedoch der *VpnClientRevokedCertificateName* -Parameter verwendet, um die zurückgegebenen Daten auf ein bestimmtes vom Client gesperrtes Zertifikat zu begrenzen: das Zertifikat mit dem Namen ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="0481e-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="0481e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0481e-115">PARAMETERS</span></span>

### <span data-ttu-id="0481e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0481e-116">-ResourceGroupName</span></span>
<span data-ttu-id="0481e-117">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0481e-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="0481e-118">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="0481e-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0481e-119">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="0481e-119">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="0481e-120">Gibt den Namen des virtuellen Netzwerkgateways an, in dem die gesperrten Zertifikatinformationen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="0481e-120">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0481e-121">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="0481e-121">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="0481e-122">Gibt den Namen des VPN-Clientzertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0481e-122">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0481e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0481e-123">-DefaultProfile</span></span>
<span data-ttu-id="0481e-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0481e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0481e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0481e-125">CommonParameters</span></span>
<span data-ttu-id="0481e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0481e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0481e-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0481e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0481e-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0481e-128">INPUTS</span></span>

## <span data-ttu-id="0481e-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0481e-129">OUTPUTS</span></span>

###  
<span data-ttu-id="0481e-130">**Get-AzureRmVpnClientRevokedCertificate** gibt Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="0481e-130">**Get-AzureRmVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="0481e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0481e-131">NOTES</span></span>

## <span data-ttu-id="0481e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0481e-132">RELATED LINKS</span></span>

[<span data-ttu-id="0481e-133">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="0481e-133">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="0481e-134">Neu – AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="0481e-134">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="0481e-135">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="0481e-135">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


