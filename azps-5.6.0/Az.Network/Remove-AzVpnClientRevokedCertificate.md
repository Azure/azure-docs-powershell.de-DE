---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: d7665d490979ca15189650572c083a94efb6c123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944920"
---
# <span data-ttu-id="35dad-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="35dad-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="35dad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35dad-102">SYNOPSIS</span></span>
<span data-ttu-id="35dad-103">Entfernt ein VPN-Client-Widerrufszertifikat.</span><span class="sxs-lookup"><span data-stu-id="35dad-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="35dad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35dad-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35dad-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35dad-105">DESCRIPTION</span></span>
<span data-ttu-id="35dad-106">Das **Cmdlet Remove-AzVpnClientRevokedCertificate** entfernt ein Clientperrzertifikat aus einem Gateway für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="35dad-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="35dad-107">Clientperrzertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="35dad-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="35dad-108">Wenn Sie ein Clientperrzertifikat entfernen, können Clientcomputer das zuvor gesperrte Zertifikat verwenden, um eine VPN-Verbindung (Virtual Private Network) herzustellen.</span><span class="sxs-lookup"><span data-stu-id="35dad-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="35dad-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="35dad-109">EXAMPLES</span></span>

### <span data-ttu-id="35dad-110">Beispiel 1: Entfernen eines Clientsperrzertifikats aus einem Gateway für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="35dad-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```powershell
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="35dad-111">Mit diesem Befehl wird ein Clientperrzertifikat aus einem Gateway für virtuelle Netzwerke mit dem Namen ContosoVirtualNetwork entfernt.</span><span class="sxs-lookup"><span data-stu-id="35dad-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="35dad-112">Um ein Clientperrzertifikat zu entfernen, müssen Sie sowohl den Zertifikatnamen als auch den Fingerabdruck des Zertifikats angeben.</span><span class="sxs-lookup"><span data-stu-id="35dad-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="35dad-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="35dad-113">PARAMETERS</span></span>

### <span data-ttu-id="35dad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35dad-114">-DefaultProfile</span></span>
<span data-ttu-id="35dad-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35dad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35dad-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35dad-116">-ResourceGroupName</span></span>
<span data-ttu-id="35dad-117">Gibt den Namen der Ressourcengruppe an, der das Virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="35dad-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="35dad-118">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="35dad-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="35dad-119">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="35dad-119">-Thumbprint</span></span>
<span data-ttu-id="35dad-120">Gibt den eindeutigen Bezeichner des zertifikats an, das entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="35dad-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="35dad-121">Sie können Fingerabdruckinformationen für Ihre Zertifikate mithilfe eines Befehls zurückgeben, der Windows PowerShell wie der folgenden ähnelt: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="35dad-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="35dad-122">Der vorhergehende Befehl gibt Informationen für alle Zertifikate des lokalen Computers zurück, die im Stammzertifikatspeicher gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="35dad-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="35dad-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="35dad-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="35dad-124">Gibt den Namen des virtuellen Netzwerkgateways an, dem das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="35dad-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="35dad-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="35dad-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="35dad-126">Gibt den Namen des entfernten VPN-Clientzertifikats an.</span><span class="sxs-lookup"><span data-stu-id="35dad-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="35dad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35dad-127">CommonParameters</span></span>
<span data-ttu-id="35dad-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35dad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35dad-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35dad-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35dad-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="35dad-130">INPUTS</span></span>

### <span data-ttu-id="35dad-131">System.String</span><span class="sxs-lookup"><span data-stu-id="35dad-131">System.String</span></span>

## <span data-ttu-id="35dad-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="35dad-132">OUTPUTS</span></span>

### <span data-ttu-id="35dad-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35dad-133">System.Boolean</span></span>

## <span data-ttu-id="35dad-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="35dad-134">NOTES</span></span>

## <span data-ttu-id="35dad-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="35dad-135">RELATED LINKS</span></span>

[<span data-ttu-id="35dad-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="35dad-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="35dad-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="35dad-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="35dad-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="35dad-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


