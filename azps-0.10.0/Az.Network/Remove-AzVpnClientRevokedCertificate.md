---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 3ea5a6ba20b02fd7289e597683d97c1513aa9873
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843731"
---
# <span data-ttu-id="62959-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="62959-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="62959-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62959-102">SYNOPSIS</span></span>
<span data-ttu-id="62959-103">Entfernt ein VPN-Client-Sperrungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="62959-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="62959-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62959-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62959-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62959-105">DESCRIPTION</span></span>
<span data-ttu-id="62959-106">Das Cmdlet **Remove-AzVpnClientRevokedCertificate** entfernt ein Client Sperr Zertifikat von einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="62959-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="62959-107">Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="62959-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="62959-108">Wenn Sie ein Client-Sperr Zertifikat entfernen, können Clientcomputer das zuvor gesperrte Zertifikat verwenden, um eine VPN-Verbindung (virtuelles privates Netzwerk) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="62959-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="62959-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62959-109">EXAMPLES</span></span>

### <span data-ttu-id="62959-110">Beispiel 1: Entfernen eines Client Sperr Zertifikats von einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="62959-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="62959-111">Dieser Befehl entfernt ein Client Sperr Zertifikat von einem virtuellen Netzwerkgateway namens ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="62959-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="62959-112">Um ein Client Sperr Zertifikat zu entfernen, müssen Sie sowohl den Zertifikatsnamen als auch den Fingerabdruck des Zertifikats angeben.</span><span class="sxs-lookup"><span data-stu-id="62959-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="62959-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="62959-113">PARAMETERS</span></span>

### <span data-ttu-id="62959-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62959-114">-DefaultProfile</span></span>
<span data-ttu-id="62959-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="62959-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62959-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62959-116">-ResourceGroupName</span></span>
<span data-ttu-id="62959-117">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="62959-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="62959-118">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="62959-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="62959-119">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="62959-119">-Thumbprint</span></span>
<span data-ttu-id="62959-120">Gibt den eindeutigen Bezeichner des Zertifikats an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="62959-120">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="62959-121">Sie können Fingerabdruckinformationen für Ihre Zertifikate zurückgeben, indem Sie einen Windows PowerShell-Befehl wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="62959-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="62959-122">Der vorhergehende Befehl gibt Informationen für alle lokalen Computer Zertifikate zurück, die im Stammzertifikatspeicher gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="62959-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="62959-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="62959-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="62959-124">Gibt den Namen des virtuellen Netzwerkgateways an, dem das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="62959-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="62959-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="62959-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="62959-126">Gibt den Namen des zu entfernendes VPN-Clientzertifikats an.</span><span class="sxs-lookup"><span data-stu-id="62959-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="62959-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62959-127">CommonParameters</span></span>
<span data-ttu-id="62959-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62959-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62959-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62959-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62959-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62959-130">INPUTS</span></span>

## <span data-ttu-id="62959-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62959-131">OUTPUTS</span></span>

## <span data-ttu-id="62959-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="62959-132">NOTES</span></span>

## <span data-ttu-id="62959-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62959-133">RELATED LINKS</span></span>

[<span data-ttu-id="62959-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="62959-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="62959-135">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="62959-135">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="62959-136">Neu – AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="62959-136">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


