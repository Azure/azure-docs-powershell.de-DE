---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 04bc51a7040cae1310fd3c4fe51fd45c425fad8e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379656"
---
# <span data-ttu-id="5f812-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f812-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="5f812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f812-102">SYNOPSIS</span></span>
<span data-ttu-id="5f812-103">Ruft Informationen über VPN-Client-Sperrzertifikate ab.</span><span class="sxs-lookup"><span data-stu-id="5f812-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="5f812-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f812-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f812-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f812-105">DESCRIPTION</span></span>
<span data-ttu-id="5f812-106">Das **Cmdlet "Get-AzVpnClientRevokedCertificate"** gibt Informationen zu den Zertifikaten zur Clientsperrung zurück, die einem virtuellen Netzwerkgateway zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="5f812-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="5f812-107">Clientsperrzertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f812-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="5f812-108">**Mit Get-AzVpnClientRevokedCertificate** können Sie Informationen zu allen Zertifikaten für die Clientsperrung auf dem Gateway zurückgeben oder mithilfe des Parameters *"VpnClientRevokedCertificateName"* Informationen zu einem einzelnen Zertifikat erhalten.</span><span class="sxs-lookup"><span data-stu-id="5f812-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="5f812-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f812-109">EXAMPLES</span></span>

### <span data-ttu-id="5f812-110">Beispiel 1: Informationen zu allen Zertifikaten für die Clientsperrung</span><span class="sxs-lookup"><span data-stu-id="5f812-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="5f812-111">Dieser Befehl ruft Informationen zu allen Zertifikaten für die Clientsperrung ab, die dem virtuellen Netzwerkgateway "ContosoVirtualNetworkGateway" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5f812-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="5f812-112">Beispiel 2: Erhalten von Informationen zu bestimmten Zertifikaten für die Clientsperrung</span><span class="sxs-lookup"><span data-stu-id="5f812-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="5f812-113">Dieser Befehl ist eine Variation des Befehls, der in Beispiel 1 gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5f812-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="5f812-114">In diesem Fall wird jedoch der Parameter *"VpnClientRevokedCertificateName"* verwendet, um die zurückgegebenen Daten auf ein bestimmtes Zertifikat mit Client widerrufen zu beschränken: das Zertifikat mit dem Namen "ContosoRevokedClientCertificate".</span><span class="sxs-lookup"><span data-stu-id="5f812-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="5f812-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f812-115">PARAMETERS</span></span>

### <span data-ttu-id="5f812-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f812-116">-DefaultProfile</span></span>
<span data-ttu-id="5f812-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f812-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f812-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f812-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f812-119">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5f812-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="5f812-120">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Verwaltung von Azure zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="5f812-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="5f812-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5f812-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5f812-122">Gibt den Namen des virtuellen Netzwerkgateways an, dem die Widerrufenzertifikatinformationen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="5f812-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="5f812-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="5f812-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="5f812-124">Gibt den Namen des VPN-Clientzertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5f812-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f812-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f812-125">CommonParameters</span></span>
<span data-ttu-id="5f812-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f812-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f812-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f812-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f812-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f812-128">INPUTS</span></span>

### <span data-ttu-id="5f812-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5f812-129">System.String</span></span>

## <span data-ttu-id="5f812-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f812-130">OUTPUTS</span></span>

### <span data-ttu-id="5f812-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f812-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="5f812-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5f812-132">NOTES</span></span>

## <span data-ttu-id="5f812-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5f812-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f812-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f812-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="5f812-135">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f812-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="5f812-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5f812-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


