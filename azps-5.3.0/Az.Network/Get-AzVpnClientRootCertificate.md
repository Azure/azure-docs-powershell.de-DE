---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3cf1bea87824320b659def722d0d0f0166fa177d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379643"
---
# <span data-ttu-id="3a230-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3a230-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="3a230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a230-102">SYNOPSIS</span></span>
<span data-ttu-id="3a230-103">Ruft Informationen zu DEN VPN-Stammzertifikaten ab.</span><span class="sxs-lookup"><span data-stu-id="3a230-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="3a230-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a230-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a230-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a230-105">DESCRIPTION</span></span>
<span data-ttu-id="3a230-106">Das **Cmdlet "Get-AzVpnClientRootCertificate"** gibt Informationen zu den Stammzertifikaten zurück, die einem virtuellen Netzwerkgateway zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="3a230-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="3a230-107">Stammzertifikate sind X.509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: Alle anderen auf dem Gateway verwendeten Zertifikate vertrauen dem Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="3a230-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="3a230-108">Standardmäßig gibt **"Get-AzVpnClientRootCertificate"** Informationen zu allen Stammzertifikaten zurück, die einem Gateway zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="3a230-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="3a230-109">(Gateways können über mehrere Stammzertifikate verfügen.) Durch Einbeziehung des Parameters **"VpnClientRootCertificateName"** können Sie die zurückgegebenen Daten jedoch auf ein bestimmtes Zertifikat beschränken.</span><span class="sxs-lookup"><span data-stu-id="3a230-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="3a230-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a230-110">EXAMPLES</span></span>

### <span data-ttu-id="3a230-111">Beispiel 1: Informationen zu allen Stammzertifikaten</span><span class="sxs-lookup"><span data-stu-id="3a230-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="3a230-112">Dieser Befehl ruft Informationen zu allen Stammzertifikaten ab, die einem virtuellen Netzwerkgateway namens "ContosoVirtualNetwork" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="3a230-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="3a230-113">Beispiel 2: Informationen zu bestimmten Stammzertifikaten</span><span class="sxs-lookup"><span data-stu-id="3a230-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="3a230-114">Dieser Befehl ist eine Variation des Befehls aus Beispiel 1.</span><span class="sxs-lookup"><span data-stu-id="3a230-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="3a230-115">In diesem Fall ist jedoch der Parameter *"VpnClientRootCertificateName"* enthalten, um die zurückgegebenen Daten auf ein bestimmtes Stammzertifikat zu beschränken: "ContosoRootClientCertificate".</span><span class="sxs-lookup"><span data-stu-id="3a230-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="3a230-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a230-116">PARAMETERS</span></span>

### <span data-ttu-id="3a230-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a230-117">-DefaultProfile</span></span>
<span data-ttu-id="3a230-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a230-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a230-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a230-119">-ResourceGroupName</span></span>
<span data-ttu-id="3a230-120">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3a230-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="3a230-121">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Verwaltung von Azure zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="3a230-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="3a230-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3a230-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3a230-123">Gibt den Namen des virtuellen Netzwerkgateways an, dem das Stammzertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3a230-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="3a230-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="3a230-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="3a230-125">Gibt den Namen des Clientstammzertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3a230-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3a230-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a230-126">CommonParameters</span></span>
<span data-ttu-id="3a230-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a230-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a230-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a230-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a230-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a230-129">INPUTS</span></span>

### <span data-ttu-id="3a230-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3a230-130">System.String</span></span>

## <span data-ttu-id="3a230-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a230-131">OUTPUTS</span></span>

### <span data-ttu-id="3a230-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3a230-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="3a230-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a230-133">NOTES</span></span>

## <span data-ttu-id="3a230-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a230-134">RELATED LINKS</span></span>

[<span data-ttu-id="3a230-135">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3a230-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="3a230-136">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3a230-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="3a230-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3a230-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


