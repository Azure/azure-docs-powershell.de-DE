---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 861ea7bcfbfbe8a713934e2dc80a4448a2a98c48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821299"
---
# <span data-ttu-id="1769f-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1769f-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="1769f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1769f-102">SYNOPSIS</span></span>
<span data-ttu-id="1769f-103">Entfernt ein VPN-Client-Sperrungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="1769f-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="1769f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1769f-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1769f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1769f-105">DESCRIPTION</span></span>
<span data-ttu-id="1769f-106">Das Cmdlet **Remove-AzVpnClientRevokedCertificate** entfernt ein Client Sperr Zertifikat von einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="1769f-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="1769f-107">Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="1769f-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="1769f-108">Wenn Sie ein Client-Sperr Zertifikat entfernen, können Clientcomputer das zuvor gesperrte Zertifikat verwenden, um eine VPN-Verbindung (virtuelles privates Netzwerk) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1769f-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="1769f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1769f-109">EXAMPLES</span></span>

### <span data-ttu-id="1769f-110">Beispiel 1: Entfernen eines Client Sperr Zertifikats von einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="1769f-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="1769f-111">Dieser Befehl entfernt ein Client Sperr Zertifikat von einem virtuellen Netzwerkgateway namens ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="1769f-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="1769f-112">Um ein Client Sperr Zertifikat zu entfernen, müssen Sie sowohl den Zertifikatsnamen als auch den Fingerabdruck des Zertifikats angeben.</span><span class="sxs-lookup"><span data-stu-id="1769f-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="1769f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1769f-113">PARAMETERS</span></span>

### <span data-ttu-id="1769f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1769f-114">-DefaultProfile</span></span>
<span data-ttu-id="1769f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1769f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1769f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1769f-116">-ResourceGroupName</span></span>
<span data-ttu-id="1769f-117">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1769f-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="1769f-118">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="1769f-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="1769f-119">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="1769f-119">-Thumbprint</span></span>
<span data-ttu-id="1769f-120">Gibt den eindeutigen Bezeichner des Zertifikats an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1769f-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="1769f-121">Sie können Fingerabdruckinformationen für Ihre Zertifikate zurückgeben, indem Sie einen Windows PowerShell-Befehl wie den folgenden verwenden: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="1769f-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="1769f-122">Der vorhergehende Befehl gibt Informationen für alle lokalen Computer Zertifikate zurück, die im Stammzertifikatspeicher gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="1769f-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="1769f-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="1769f-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="1769f-124">Gibt den Namen des virtuellen Netzwerkgateways an, dem das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1769f-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="1769f-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="1769f-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="1769f-126">Gibt den Namen des zu entfernendes VPN-Clientzertifikats an.</span><span class="sxs-lookup"><span data-stu-id="1769f-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="1769f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1769f-127">CommonParameters</span></span>
<span data-ttu-id="1769f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1769f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1769f-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1769f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1769f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1769f-130">INPUTS</span></span>

### <span data-ttu-id="1769f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1769f-131">System.String</span></span>

## <span data-ttu-id="1769f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1769f-132">OUTPUTS</span></span>

### <span data-ttu-id="1769f-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1769f-133">System.Boolean</span></span>

## <span data-ttu-id="1769f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="1769f-134">NOTES</span></span>

## <span data-ttu-id="1769f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1769f-135">RELATED LINKS</span></span>

[<span data-ttu-id="1769f-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1769f-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="1769f-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1769f-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="1769f-138">Neu – AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="1769f-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


