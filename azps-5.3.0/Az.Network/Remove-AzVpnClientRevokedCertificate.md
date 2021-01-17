---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 2dee180dff1489779dd2eb34f8bd5e3d8be10b91
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385187"
---
# <span data-ttu-id="619d5-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="619d5-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="619d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="619d5-102">SYNOPSIS</span></span>
<span data-ttu-id="619d5-103">Entfernt ein ZERTIFIKAT für die Clientsperrung eines VPN-Clients.</span><span class="sxs-lookup"><span data-stu-id="619d5-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="619d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="619d5-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="619d5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="619d5-105">DESCRIPTION</span></span>
<span data-ttu-id="619d5-106">Das **Cmdlet "Remove-AzVpnClientRevokedCertificate"** entfernt ein Zertifikat für die Clientsperrung von einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="619d5-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="619d5-107">Clientsperrzertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="619d5-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="619d5-108">Wenn Sie clientsperrische Zertifikatclientcomputer entfernen, können Sie das zuvor gesperrte Zertifikat verwenden, um eine VPN (Virtuelle Private Network)-Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="619d5-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="619d5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="619d5-109">EXAMPLES</span></span>

### <span data-ttu-id="619d5-110">Beispiel 1: Entfernen eines Zertifikats für die Clientsperrung von einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="619d5-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```powershell
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="619d5-111">Mit diesem Befehl wird ein Zertifikat für die Clientsperrung aus einem virtuellen Netzwerkgateway namens "ContosoVirtualNetwork" entfernt.</span><span class="sxs-lookup"><span data-stu-id="619d5-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="619d5-112">Zum Entfernen eines Zertifikats für die Clientsperrung müssen Sie sowohl den Zertifikatnamen als auch den Fingerabdruck des Zertifikats angeben.</span><span class="sxs-lookup"><span data-stu-id="619d5-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="619d5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="619d5-113">PARAMETERS</span></span>

### <span data-ttu-id="619d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="619d5-114">-DefaultProfile</span></span>
<span data-ttu-id="619d5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="619d5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="619d5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="619d5-116">-ResourceGroupName</span></span>
<span data-ttu-id="619d5-117">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="619d5-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="619d5-118">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Verwaltung von Azure zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="619d5-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="619d5-119">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="619d5-119">-Thumbprint</span></span>
<span data-ttu-id="619d5-120">Gibt den eindeutigen Bezeichner des zu entfernenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="619d5-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="619d5-121">Sie können Fingerabdrückinformationen für Ihre Zertifikate mithilfe eines Windows PowerShell ähnlich dem folgenden zurückgeben: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="619d5-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="619d5-122">Der vorherige Befehl gibt Informationen für alle Zertifikate des lokalen Computers zurück, die im Stammzertifikatspeicher gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="619d5-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="619d5-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="619d5-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="619d5-124">Gibt den Namen des virtuellen Netzwerkgateways an, dem das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="619d5-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="619d5-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="619d5-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="619d5-126">Gibt den Namen des VPN-Clientzertifikats an, das entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="619d5-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="619d5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619d5-127">CommonParameters</span></span>
<span data-ttu-id="619d5-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="619d5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619d5-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="619d5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619d5-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="619d5-130">INPUTS</span></span>

### <span data-ttu-id="619d5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="619d5-131">System.String</span></span>

## <span data-ttu-id="619d5-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="619d5-132">OUTPUTS</span></span>

### <span data-ttu-id="619d5-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="619d5-133">System.Boolean</span></span>

## <span data-ttu-id="619d5-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="619d5-134">NOTES</span></span>

## <span data-ttu-id="619d5-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="619d5-135">RELATED LINKS</span></span>

[<span data-ttu-id="619d5-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="619d5-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="619d5-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="619d5-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="619d5-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="619d5-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


