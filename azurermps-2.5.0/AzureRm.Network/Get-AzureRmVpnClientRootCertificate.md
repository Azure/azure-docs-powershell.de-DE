---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 7c3ee4e2c640417a7ba3d6cd78c2c8ea0691fff3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849172"
---
# <span data-ttu-id="de1e9-101">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de1e9-101">Get-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="de1e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="de1e9-103">Ruft Informationen zu VPN-Stammzertifikaten ab.</span><span class="sxs-lookup"><span data-stu-id="de1e9-103">Gets information about VPN root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de1e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de1e9-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de1e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de1e9-105">DESCRIPTION</span></span>
<span data-ttu-id="de1e9-106">Das Cmdlet " **Get-AzureRmVpnClientRootCertificate** " gibt Informationen zu den Stammzertifikaten zurück, die einem virtuellen Netzwerkgateway zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="de1e9-106">The **Get-AzureRmVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="de1e9-107">Stammzertifikate sind X. 509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: alle anderen auf dem Gateway verwendeten Zertifikate vertrauen dem Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="de1e9-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="de1e9-108">Standardmäßig gibt **Get-AzureRmVpnClientRootCertificate** Informationen zu allen Stammzertifikaten zurück, die einem Gateway zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="de1e9-108">By default, **Get-AzureRmVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="de1e9-109">(Gateways können mehr als ein Stammzertifikat aufweisen.) Durch Einschließen des **VpnClientRootCertificateName** -Parameters können Sie die zurückgegebenen Daten jedoch auf ein bestimmtes Zertifikat einschränken.</span><span class="sxs-lookup"><span data-stu-id="de1e9-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="de1e9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de1e9-110">EXAMPLES</span></span>

### <span data-ttu-id="de1e9-111">Beispiel 1: Abrufen von Informationen zu allen Stammzertifikaten</span><span class="sxs-lookup"><span data-stu-id="de1e9-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="de1e9-112">Dieser Befehl ruft Informationen zu allen Stammzertifikaten ab, die einem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetwork zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="de1e9-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="de1e9-113">Beispiel 2: Abrufen von Informationen zu bestimmten Stammzertifikaten</span><span class="sxs-lookup"><span data-stu-id="de1e9-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="de1e9-114">Dieser Befehl ist eine Variation des Befehls, der in Beispiel 1 gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="de1e9-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="de1e9-115">In diesem Fall ist der *VpnClientRootCertificateName* -Parameter jedoch enthalten, um die zurückgegebenen Daten auf ein bestimmtes Stammzertifikat zu begrenzen: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="de1e9-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="de1e9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="de1e9-116">PARAMETERS</span></span>

### <span data-ttu-id="de1e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de1e9-117">-DefaultProfile</span></span>
<span data-ttu-id="de1e9-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de1e9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de1e9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de1e9-119">-ResourceGroupName</span></span>
<span data-ttu-id="de1e9-120">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="de1e9-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="de1e9-121">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="de1e9-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="de1e9-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="de1e9-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="de1e9-123">Gibt den Namen des virtuellen Netzwerkgateways an, dem das Stammzertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="de1e9-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="de1e9-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="de1e9-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="de1e9-125">Gibt den Namen des Client-Stammzertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="de1e9-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="de1e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1e9-126">CommonParameters</span></span>
<span data-ttu-id="de1e9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de1e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1e9-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de1e9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1e9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de1e9-129">INPUTS</span></span>

## <span data-ttu-id="de1e9-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de1e9-130">OUTPUTS</span></span>

###  
<span data-ttu-id="de1e9-131">**Get-AzureRmVpnClientRootCertificate** Ruft Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="de1e9-131">**Get-AzureRmVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="de1e9-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="de1e9-132">NOTES</span></span>

## <span data-ttu-id="de1e9-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de1e9-133">RELATED LINKS</span></span>

[<span data-ttu-id="de1e9-134">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de1e9-134">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="de1e9-135">Neu – AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de1e9-135">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="de1e9-136">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de1e9-136">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


