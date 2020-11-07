---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: e2a2153ca9d75447603ce87c896720ece0f83a18
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850775"
---
# <span data-ttu-id="fe30c-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fe30c-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="fe30c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe30c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe30c-103">Fügt ein VPN-Client Sperrungs Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="fe30c-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe30c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe30c-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe30c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe30c-105">DESCRIPTION</span></span>
<span data-ttu-id="fe30c-106">Das Cmdlet **Add-AzureRmVpnClientRevokedCertificate** weist einem virtuellen Netzwerkgateway ein Client Sperr Zertifikat zu.</span><span class="sxs-lookup"><span data-stu-id="fe30c-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="fe30c-107">Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe30c-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="fe30c-108">Sie müssen sowohl den Zertifikatnamen als auch den Fingerabdruck des Zertifikats angeben, um dieses Cmdlet verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="fe30c-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="fe30c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe30c-109">EXAMPLES</span></span>

### <span data-ttu-id="fe30c-110">Beispiel 1: Hinzufügen eines neuen Client Sperr Zertifikats zu einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="fe30c-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="fe30c-111">Mit diesem Befehl wird dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetwork ein neues Client Sperr Zertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fe30c-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="fe30c-112">Um das Zertifikat hinzuzufügen, müssen Sie sowohl den Zertifikatnamen als auch den Fingerabdruck des Zertifikats angeben.</span><span class="sxs-lookup"><span data-stu-id="fe30c-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="fe30c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe30c-113">PARAMETERS</span></span>

### <span data-ttu-id="fe30c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe30c-114">-DefaultProfile</span></span>
<span data-ttu-id="fe30c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe30c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe30c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe30c-116">-ResourceGroupName</span></span>
<span data-ttu-id="fe30c-117">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="fe30c-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="fe30c-118">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="fe30c-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="fe30c-119">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="fe30c-119">-Thumbprint</span></span>
<span data-ttu-id="fe30c-120">Gibt den eindeutigen Bezeichner des hinzuzufügenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="fe30c-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="fe30c-121">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fe30c-121">For example:</span></span>

<span data-ttu-id="fe30c-122">-Daumenabdruck "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="fe30c-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="fe30c-123">Sie können Fingerabdruckinformationen für Ihre Zertifikate abrufen, indem Sie einen Windows PowerShell-Befehl wie den folgenden verwenden: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="fe30c-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="fe30c-124">Der vorhergehende Befehl ruft Informationen für alle lokalen Computerzertifikate ab, die im Stammzertifikatspeicher gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="fe30c-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="fe30c-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="fe30c-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="fe30c-126">Gibt den Namen des virtuellen Netzwerkgateways an, in dem das Zertifikat hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe30c-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="fe30c-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="fe30c-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="fe30c-128">Gibt den Namen des VPN-Clientzertifikats an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fe30c-128">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe30c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe30c-129">CommonParameters</span></span>
<span data-ttu-id="fe30c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe30c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe30c-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe30c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe30c-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe30c-132">INPUTS</span></span>

## <span data-ttu-id="fe30c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe30c-133">OUTPUTS</span></span>

### <span data-ttu-id="fe30c-134">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fe30c-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="fe30c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe30c-135">NOTES</span></span>

## <span data-ttu-id="fe30c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe30c-136">RELATED LINKS</span></span>

[<span data-ttu-id="fe30c-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fe30c-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="fe30c-138">Neu – AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fe30c-138">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="fe30c-139">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="fe30c-139">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


