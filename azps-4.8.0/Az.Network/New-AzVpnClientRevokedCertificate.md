---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175013"
---
# <span data-ttu-id="e041b-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e041b-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="e041b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e041b-102">SYNOPSIS</span></span>
<span data-ttu-id="e041b-103">Erstellt ein neues VPN-Client Sperr Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="e041b-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="e041b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e041b-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e041b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e041b-105">DESCRIPTION</span></span>
<span data-ttu-id="e041b-106">Das Cmdlet **New-AzVpnClientRevokedCertificate** erstellt ein neues virtuelles privates Netzwerk (VPN)-Client Sperr Zertifikat zur Verwendung auf einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="e041b-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="e041b-107">Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e041b-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="e041b-108">Mit diesem Cmdlet wird ein eigenständiges Zertifikat erstellt, das keinem virtuellen Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e041b-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="e041b-109">Stattdessen wird das von **New-AzVpnClientRevokedCertificate** erstellte Zertifikat zusammen mit dem New-AzVirtualNetworkGateway-Cmdlet verwendet, wenn ein neues Gateway erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e041b-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="e041b-110">Nehmen wir beispielsweise an, dass Sie ein neues Zertifikat erstellen und es in einer Variablen mit dem Namen $Certificate speichern.</span><span class="sxs-lookup"><span data-stu-id="e041b-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="e041b-111">Sie können dieses Certificate-Objekt dann verwenden, wenn Sie ein neues virtuelles Gateway erstellen.</span><span class="sxs-lookup"><span data-stu-id="e041b-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="e041b-112">Zum Beispiel `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="e041b-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="e041b-113">Weitere Informationen finden Sie in der Dokumentation zum New-AzVirtualNetworkGateway-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e041b-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="e041b-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e041b-114">EXAMPLES</span></span>

### <span data-ttu-id="e041b-115">Beispiel 1: Erstellen eines neuen, vom Client gesperrten Zertifikats</span><span class="sxs-lookup"><span data-stu-id="e041b-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="e041b-116">Dieser Befehl erstellt ein neues, vom Client gesperrtes Zertifikat und speichert das Certificate-Objekt in einer Variablen mit dem Namen $Certificate.</span><span class="sxs-lookup"><span data-stu-id="e041b-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="e041b-117">Diese Variable kann dann vom Cmdlet **New-AzVirtualNetworkGateway** verwendet werden, um das Zertifikat einem neuen virtuellen Netzwerkgateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e041b-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="e041b-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e041b-118">PARAMETERS</span></span>

### <span data-ttu-id="e041b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e041b-119">-DefaultProfile</span></span>
<span data-ttu-id="e041b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e041b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e041b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e041b-121">-Name</span></span>
<span data-ttu-id="e041b-122">Gibt einen eindeutigen Namen für das neue Client Sperr Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="e041b-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="e041b-123">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="e041b-123">-Thumbprint</span></span>
<span data-ttu-id="e041b-124">Gibt den eindeutigen Bezeichner des hinzuzufügenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="e041b-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="e041b-125">Sie können Fingerabdruckinformationen für Ihre Zertifikate zurückgeben, indem Sie einen Windows PowerShell-Befehl wie den folgenden verwenden: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="e041b-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="e041b-126">Der vorhergehende Befehl gibt Informationen für alle lokalen Computer Zertifikate zurück, die im Stammzertifikatspeicher gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="e041b-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="e041b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e041b-127">CommonParameters</span></span>
<span data-ttu-id="e041b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e041b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e041b-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e041b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e041b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e041b-130">INPUTS</span></span>

### <span data-ttu-id="e041b-131">Keine</span><span class="sxs-lookup"><span data-stu-id="e041b-131">None</span></span>

## <span data-ttu-id="e041b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e041b-132">OUTPUTS</span></span>

### <span data-ttu-id="e041b-133">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e041b-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="e041b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="e041b-134">NOTES</span></span>

## <span data-ttu-id="e041b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e041b-135">RELATED LINKS</span></span>

[<span data-ttu-id="e041b-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e041b-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="e041b-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e041b-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="e041b-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="e041b-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


