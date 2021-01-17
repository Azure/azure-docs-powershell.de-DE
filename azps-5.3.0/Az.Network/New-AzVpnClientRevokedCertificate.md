---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378942"
---
# <span data-ttu-id="486db-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="486db-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="486db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="486db-102">SYNOPSIS</span></span>
<span data-ttu-id="486db-103">Erstellt ein neues ZERTIFIKAT für die Clientsperrung von VPN.</span><span class="sxs-lookup"><span data-stu-id="486db-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="486db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="486db-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="486db-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="486db-105">DESCRIPTION</span></span>
<span data-ttu-id="486db-106">Das **Cmdlet "New-AzVpnClientRevokedCertificate"** erstellt ein neues VPN (Virtual Private Network)-Clientsperrzertifikat zur Verwendung auf einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="486db-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="486db-107">Clientsperrzertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="486db-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="486db-108">Dieses Cmdlet erstellt ein eigenständiges Zertifikat, das keinem virtuellen Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="486db-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="486db-109">Stattdessen wird das mit **"New-AzVpnClientRevokedCertificate"** erstellte Zertifikat beim Erstellen eines neuen Gateways in Verbindung mit dem Cmdlet New-AzVirtualNetworkGateway verwendet.</span><span class="sxs-lookup"><span data-stu-id="486db-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="486db-110">Angenommen, Sie erstellen ein neues Zertifikat und speichern es in einer Variablen namens $Certificate.</span><span class="sxs-lookup"><span data-stu-id="486db-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="486db-111">Sie können dieses Zertifikatobjekt dann verwenden, wenn Sie ein neues virtuelles Gateway erstellen.</span><span class="sxs-lookup"><span data-stu-id="486db-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="486db-112">Zum Beispiel `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="486db-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="486db-113">Weitere Informationen finden Sie in der Dokumentation zum New-AzVirtualNetworkGateway Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="486db-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="486db-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="486db-114">EXAMPLES</span></span>

### <span data-ttu-id="486db-115">Beispiel 1: Erstellen eines neuen Zertifikats mit Client widerrufen</span><span class="sxs-lookup"><span data-stu-id="486db-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="486db-116">Dieser Befehl erstellt ein neues Zertifikat mit Client widerrufen und speichert das Zertifikatobjekt in einer Variablen namens $Certificate.</span><span class="sxs-lookup"><span data-stu-id="486db-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="486db-117">Diese Variable kann dann vom **Cmdlet "New-AzVirtualNetworkGateway"** verwendet werden, um das Zertifikat einem neuen virtuellen Netzwerkgateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="486db-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="486db-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="486db-118">PARAMETERS</span></span>

### <span data-ttu-id="486db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486db-119">-DefaultProfile</span></span>
<span data-ttu-id="486db-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="486db-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="486db-121">-Name</span><span class="sxs-lookup"><span data-stu-id="486db-121">-Name</span></span>
<span data-ttu-id="486db-122">Gibt einen eindeutigen Namen für das neue Zertifikat für die Clientsperrung an.</span><span class="sxs-lookup"><span data-stu-id="486db-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="486db-123">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="486db-123">-Thumbprint</span></span>
<span data-ttu-id="486db-124">Gibt den eindeutigen Bezeichner des hinzugefügten Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="486db-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="486db-125">Sie können Fingerabdrückinformationen für Ihre Zertifikate mithilfe eines Windows PowerShell ähnlich dem folgenden zurückgeben: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="486db-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="486db-126">Der vorherige Befehl gibt Informationen für alle Zertifikate des lokalen Computers zurück, die im Stammzertifikatspeicher gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="486db-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="486db-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486db-127">CommonParameters</span></span>
<span data-ttu-id="486db-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="486db-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486db-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="486db-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486db-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="486db-130">INPUTS</span></span>

### <span data-ttu-id="486db-131">Keine</span><span class="sxs-lookup"><span data-stu-id="486db-131">None</span></span>

## <span data-ttu-id="486db-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="486db-132">OUTPUTS</span></span>

### <span data-ttu-id="486db-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="486db-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="486db-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="486db-134">NOTES</span></span>

## <span data-ttu-id="486db-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="486db-135">RELATED LINKS</span></span>

[<span data-ttu-id="486db-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="486db-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="486db-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="486db-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="486db-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="486db-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


