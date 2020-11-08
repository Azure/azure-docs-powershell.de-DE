---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e7c2b8d4e26e45fff0c81f5bf3fecd10e40cd7a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173249"
---
# <span data-ttu-id="d00f6-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d00f6-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="d00f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d00f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d00f6-103">Fügt ein VPN-Client Sperrungs Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="d00f6-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="d00f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d00f6-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d00f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d00f6-105">DESCRIPTION</span></span>
<span data-ttu-id="d00f6-106">Das Cmdlet **Add-AzVpnClientRevokedCertificate** weist einem virtuellen Netzwerkgateway ein Client Sperr Zertifikat zu.</span><span class="sxs-lookup"><span data-stu-id="d00f6-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="d00f6-107">Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="d00f6-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="d00f6-108">Sie müssen sowohl den Zertifikatnamen als auch den Fingerabdruck des Zertifikats angeben, um dieses Cmdlet verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="d00f6-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="d00f6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d00f6-109">EXAMPLES</span></span>

### <span data-ttu-id="d00f6-110">Beispiel 1: Hinzufügen eines neuen Client Sperr Zertifikats zu einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="d00f6-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="d00f6-111">Mit diesem Befehl wird dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetwork ein neues Client Sperr Zertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d00f6-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="d00f6-112">Um das Zertifikat hinzuzufügen, müssen Sie sowohl den Zertifikatnamen als auch den Fingerabdruck des Zertifikats angeben.</span><span class="sxs-lookup"><span data-stu-id="d00f6-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="d00f6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d00f6-113">PARAMETERS</span></span>

### <span data-ttu-id="d00f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d00f6-114">-DefaultProfile</span></span>
<span data-ttu-id="d00f6-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d00f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d00f6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d00f6-116">-ResourceGroupName</span></span>
<span data-ttu-id="d00f6-117">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d00f6-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="d00f6-118">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="d00f6-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="d00f6-119">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="d00f6-119">-Thumbprint</span></span>
<span data-ttu-id="d00f6-120">Gibt den eindeutigen Bezeichner des hinzuzufügenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="d00f6-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="d00f6-121">Beispiel:-Fingerabdruck "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" Sie können Fingerabdruckinformationen für Ihre Zertifikate abrufen, indem Sie einen Windows PowerShell-Befehl wie den folgenden verwenden: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="d00f6-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="d00f6-122">Der vorhergehende Befehl ruft Informationen für alle lokalen Computerzertifikate ab, die im Stammzertifikatspeicher gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="d00f6-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d00f6-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d00f6-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d00f6-124">Gibt den Namen des virtuellen Netzwerkgateways an, in dem das Zertifikat hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d00f6-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="d00f6-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="d00f6-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="d00f6-126">Gibt den Namen des VPN-Clientzertifikats an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d00f6-126">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d00f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d00f6-127">CommonParameters</span></span>
<span data-ttu-id="d00f6-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d00f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d00f6-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d00f6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d00f6-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d00f6-130">INPUTS</span></span>

### <span data-ttu-id="d00f6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d00f6-131">System.String</span></span>

## <span data-ttu-id="d00f6-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d00f6-132">OUTPUTS</span></span>

### <span data-ttu-id="d00f6-133">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d00f6-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="d00f6-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d00f6-134">NOTES</span></span>

## <span data-ttu-id="d00f6-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d00f6-135">RELATED LINKS</span></span>

[<span data-ttu-id="d00f6-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d00f6-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="d00f6-137">Neu – AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d00f6-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="d00f6-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d00f6-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


