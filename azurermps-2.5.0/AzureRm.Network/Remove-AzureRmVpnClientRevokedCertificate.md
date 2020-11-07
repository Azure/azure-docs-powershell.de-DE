---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: ce4d2c61feb20c750d908b6f235d89dafa713e62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850608"
---
# <span data-ttu-id="8ac28-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="8ac28-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="8ac28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ac28-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac28-103">Entfernt ein VPN-Client-Sperrungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="8ac28-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ac28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ac28-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ac28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ac28-105">DESCRIPTION</span></span>
<span data-ttu-id="8ac28-106">Das Cmdlet **Remove-AzureRmVpnClientRevokedCertificate** entfernt ein Client Sperr Zertifikat von einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="8ac28-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="8ac28-107">Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ac28-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="8ac28-108">Wenn Sie ein Client-Sperr Zertifikat entfernen, können Clientcomputer das zuvor gesperrte Zertifikat verwenden, um eine VPN-Verbindung (virtuelles privates Netzwerk) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8ac28-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="8ac28-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ac28-109">EXAMPLES</span></span>

### <span data-ttu-id="8ac28-110">Beispiel 1: Entfernen eines Client Sperr Zertifikats von einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="8ac28-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="8ac28-111">Dieser Befehl entfernt ein Client Sperr Zertifikat von einem virtuellen Netzwerkgateway namens ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="8ac28-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="8ac28-112">Um ein Client Sperr Zertifikat zu entfernen, müssen Sie sowohl den Zertifikatsnamen als auch den Fingerabdruck des Zertifikats angeben.</span><span class="sxs-lookup"><span data-stu-id="8ac28-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="8ac28-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ac28-113">PARAMETERS</span></span>

### <span data-ttu-id="8ac28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac28-114">-DefaultProfile</span></span>
<span data-ttu-id="8ac28-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ac28-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ac28-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac28-116">-ResourceGroupName</span></span>
<span data-ttu-id="8ac28-117">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8ac28-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="8ac28-118">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="8ac28-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="8ac28-119">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="8ac28-119">-Thumbprint</span></span>
<span data-ttu-id="8ac28-120">Gibt den eindeutigen Bezeichner des Zertifikats an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ac28-120">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="8ac28-121">Sie können Fingerabdruckinformationen für Ihre Zertifikate zurückgeben, indem Sie einen Windows PowerShell-Befehl wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="8ac28-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="8ac28-122">Der vorhergehende Befehl gibt Informationen für alle lokalen Computer Zertifikate zurück, die im Stammzertifikatspeicher gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="8ac28-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="8ac28-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8ac28-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8ac28-124">Gibt den Namen des virtuellen Netzwerkgateways an, dem das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8ac28-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="8ac28-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="8ac28-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="8ac28-126">Gibt den Namen des zu entfernendes VPN-Clientzertifikats an.</span><span class="sxs-lookup"><span data-stu-id="8ac28-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="8ac28-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac28-127">CommonParameters</span></span>
<span data-ttu-id="8ac28-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac28-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac28-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac28-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac28-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ac28-130">INPUTS</span></span>

## <span data-ttu-id="8ac28-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ac28-131">OUTPUTS</span></span>

## <span data-ttu-id="8ac28-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ac28-132">NOTES</span></span>

## <span data-ttu-id="8ac28-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ac28-133">RELATED LINKS</span></span>

[<span data-ttu-id="8ac28-134">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="8ac28-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="8ac28-135">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="8ac28-135">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="8ac28-136">Neu – AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="8ac28-136">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)


