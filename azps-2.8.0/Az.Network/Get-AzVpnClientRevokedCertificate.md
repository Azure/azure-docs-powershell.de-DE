---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 42b8b0baa223c72642ad27e5ea823ba0dfa9e2df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822228"
---
# <span data-ttu-id="ce002-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ce002-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="ce002-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce002-102">SYNOPSIS</span></span>
<span data-ttu-id="ce002-103">Ruft Informationen zu VPN-Client Sperrungs Zertifikaten ab.</span><span class="sxs-lookup"><span data-stu-id="ce002-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="ce002-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce002-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce002-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce002-105">DESCRIPTION</span></span>
<span data-ttu-id="ce002-106">Das Cmdlet " **Get-AzVpnClientRevokedCertificate** " gibt Informationen zu den Client Sperr Zertifikaten zurück, die einem virtuellen Netzwerkgateway zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="ce002-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="ce002-107">Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="ce002-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="ce002-108">Mit **Get-AzVpnClientRevokedCertificate** können Sie Informationen zu allen Client Sperr Zertifikaten auf dem Gateway zurückgeben oder mithilfe des *VpnClientRevokedCertificateName* -Parameters Informationen zu einem einzelnen Zertifikat abrufen.</span><span class="sxs-lookup"><span data-stu-id="ce002-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="ce002-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce002-109">EXAMPLES</span></span>

### <span data-ttu-id="ce002-110">Beispiel 1: Abrufen von Informationen zu allen Client Sperr Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="ce002-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="ce002-111">Dieser Befehl ruft Informationen zu allen Client Sperr Zertifikaten ab, die dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetworkGateway zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ce002-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="ce002-112">Beispiel 2: Abrufen von Informationen zu bestimmten Client Sperr Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="ce002-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="ce002-113">Dieser Befehl ist eine Variation des Befehls, der in Beispiel 1 gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ce002-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="ce002-114">In diesem Fall wird jedoch der *VpnClientRevokedCertificateName* -Parameter verwendet, um die zurückgegebenen Daten auf ein bestimmtes vom Client gesperrtes Zertifikat zu begrenzen: das Zertifikat mit dem Namen ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="ce002-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="ce002-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce002-115">PARAMETERS</span></span>

### <span data-ttu-id="ce002-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce002-116">-DefaultProfile</span></span>
<span data-ttu-id="ce002-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce002-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce002-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce002-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce002-119">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ce002-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="ce002-120">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="ce002-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="ce002-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ce002-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ce002-122">Gibt den Namen des virtuellen Netzwerkgateways an, in dem die gesperrten Zertifikatinformationen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="ce002-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="ce002-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="ce002-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="ce002-124">Gibt den Namen des VPN-Clientzertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ce002-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ce002-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce002-125">CommonParameters</span></span>
<span data-ttu-id="ce002-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce002-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce002-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce002-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce002-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce002-128">INPUTS</span></span>

### <span data-ttu-id="ce002-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ce002-129">System.String</span></span>

## <span data-ttu-id="ce002-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce002-130">OUTPUTS</span></span>

### <span data-ttu-id="ce002-131">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ce002-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="ce002-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce002-132">NOTES</span></span>

## <span data-ttu-id="ce002-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce002-133">RELATED LINKS</span></span>

[<span data-ttu-id="ce002-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ce002-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="ce002-135">Neu – AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ce002-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="ce002-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ce002-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


