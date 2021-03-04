---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: c5ceef5ec70ac337180c8e2fcf6bb567c68391a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918720"
---
# <span data-ttu-id="01cef-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="01cef-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="01cef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01cef-102">SYNOPSIS</span></span>
<span data-ttu-id="01cef-103">Ruft Informationen zu VPN-Clientsperrzertifikaten ab.</span><span class="sxs-lookup"><span data-stu-id="01cef-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="01cef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01cef-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01cef-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01cef-105">DESCRIPTION</span></span>
<span data-ttu-id="01cef-106">Das **Cmdlet Get-AzVpnClientRevokedCertificate** gibt Informationen zu den Clientsperrzertifikaten zurück, die einem Gateway für virtuelle Netzwerke zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="01cef-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="01cef-107">Clientperrzertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="01cef-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="01cef-108">**Mit Get-AzVpnClientRevokedCertificate** können Sie Informationen zu allen Clientperrzertifikaten im Gateway zurückgeben oder mithilfe des *VpnClientRevokedCertificateName-Parameters* Informationen zu einem einzelnen Zertifikat erhalten.</span><span class="sxs-lookup"><span data-stu-id="01cef-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="01cef-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01cef-109">EXAMPLES</span></span>

### <span data-ttu-id="01cef-110">Beispiel 1: Informationen zu allen Clientsperrzertifikaten</span><span class="sxs-lookup"><span data-stu-id="01cef-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="01cef-111">Dieser Befehl ruft Informationen zu allen Clientperrzertifikaten ab, die dem virtuellen Netzwerkgateway "ContosoVirtualNetworkGateway" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="01cef-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="01cef-112">Beispiel 2: Informationen zu bestimmten Clientsperrzertifikaten</span><span class="sxs-lookup"><span data-stu-id="01cef-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="01cef-113">Dieser Befehl ist eine Variation des Befehls in Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="01cef-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="01cef-114">In diesem Fall wird jedoch der *Parameter VpnClientRevokedCertificateName* verwendet, um die zurückgegebenen Daten auf ein bestimmtes vom Client widerrufenes Zertifikat zu beschränken: das Zertifikat mit dem Namen ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="01cef-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="01cef-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="01cef-115">PARAMETERS</span></span>

### <span data-ttu-id="01cef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01cef-116">-DefaultProfile</span></span>
<span data-ttu-id="01cef-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01cef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01cef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01cef-118">-ResourceGroupName</span></span>
<span data-ttu-id="01cef-119">Gibt den Namen der Ressourcengruppe an, der das Virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="01cef-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="01cef-120">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="01cef-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="01cef-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="01cef-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="01cef-122">Gibt den Namen des Virtuellen Netzwerkgateways an, dem die widerrufenen Zertifikatinformationen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="01cef-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="01cef-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="01cef-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="01cef-124">Gibt den Namen des VPN-Clientzertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="01cef-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="01cef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01cef-125">CommonParameters</span></span>
<span data-ttu-id="01cef-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01cef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01cef-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01cef-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01cef-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01cef-128">INPUTS</span></span>

### <span data-ttu-id="01cef-129">System.String</span><span class="sxs-lookup"><span data-stu-id="01cef-129">System.String</span></span>

## <span data-ttu-id="01cef-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01cef-130">OUTPUTS</span></span>

### <span data-ttu-id="01cef-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="01cef-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="01cef-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="01cef-132">NOTES</span></span>

## <span data-ttu-id="01cef-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="01cef-133">RELATED LINKS</span></span>

[<span data-ttu-id="01cef-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="01cef-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="01cef-135">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="01cef-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="01cef-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="01cef-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


