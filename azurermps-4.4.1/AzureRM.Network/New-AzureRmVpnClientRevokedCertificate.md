---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e1f85cbb90e1318c6eab595ef00929ceb1a5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479082"
---
# <span data-ttu-id="28e90-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="28e90-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="28e90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28e90-102">SYNOPSIS</span></span>
<span data-ttu-id="28e90-103">Erstellt ein neues VPN-Client Sperr Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="28e90-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28e90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28e90-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28e90-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28e90-105">DESCRIPTION</span></span>
<span data-ttu-id="28e90-106">Das Cmdlet **New-AzureRmVpnClientRevokedCertificate** erstellt ein neues virtuelles privates Netzwerk (VPN)-Client Sperr Zertifikat zur Verwendung auf einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="28e90-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="28e90-107">Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="28e90-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>

<span data-ttu-id="28e90-108">Mit diesem Cmdlet wird ein eigenständiges Zertifikat erstellt, das keinem virtuellen Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="28e90-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="28e90-109">Stattdessen wird das von **New-AzureRmVpnClientRevokedCertificate** erstellte Zertifikat zusammen mit dem New-AzureRmVirtualNetworkGateway-Cmdlet verwendet, wenn ein neues Gateway erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="28e90-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="28e90-110">Nehmen wir beispielsweise an, dass Sie ein neues Zertifikat erstellen und es in einer Variablen mit dem Namen $Certificate speichern.</span><span class="sxs-lookup"><span data-stu-id="28e90-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="28e90-111">Sie können dieses Certificate-Objekt dann verwenden, wenn Sie ein neues virtuelles Gateway erstellen.</span><span class="sxs-lookup"><span data-stu-id="28e90-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="28e90-112">Zum Beispiel</span><span class="sxs-lookup"><span data-stu-id="28e90-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

<span data-ttu-id="28e90-113">Weitere Informationen finden Sie in der Dokumentation zum New-AzureRmVirtualNetworkGateway-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28e90-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="28e90-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28e90-114">EXAMPLES</span></span>

### <span data-ttu-id="28e90-115">Beispiel 1: Erstellen eines neuen, vom Client gesperrten Zertifikats</span><span class="sxs-lookup"><span data-stu-id="28e90-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="28e90-116">Dieser Befehl erstellt ein neues, vom Client gesperrtes Zertifikat und speichert das Certificate-Objekt in einer Variablen mit dem Namen $Certificate.</span><span class="sxs-lookup"><span data-stu-id="28e90-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="28e90-117">Diese Variable kann dann vom Cmdlet **New-AzureRmVirtualNetworkGateway** verwendet werden, um das Zertifikat einem neuen virtuellen Netzwerkgateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="28e90-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="28e90-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="28e90-118">PARAMETERS</span></span>

### <span data-ttu-id="28e90-119">-Name</span><span class="sxs-lookup"><span data-stu-id="28e90-119">-Name</span></span>
<span data-ttu-id="28e90-120">Gibt einen eindeutigen Namen für das neue Client Sperr Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="28e90-120">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="28e90-121">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="28e90-121">-Thumbprint</span></span>
<span data-ttu-id="28e90-122">Gibt den eindeutigen Bezeichner des hinzuzufügenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="28e90-122">Specifies the unique identifier of the certificate being added.</span></span>

<span data-ttu-id="28e90-123">Sie können Fingerabdruckinformationen für Ihre Zertifikate zurückgeben, indem Sie einen Windows PowerShell-Befehl wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="28e90-123">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path Cert:\LocalMachine\Root`

<span data-ttu-id="28e90-124">Der vorhergehende Befehl gibt Informationen für alle lokalen Computer Zertifikate zurück, die im Stammzertifikatspeicher gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="28e90-124">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="28e90-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e90-125">-DefaultProfile</span></span>
<span data-ttu-id="28e90-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28e90-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e90-127">CommonParameters</span></span>
<span data-ttu-id="28e90-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28e90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e90-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28e90-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e90-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28e90-130">INPUTS</span></span>

###  
<span data-ttu-id="28e90-131">Dieses Cmdlet akzeptiert keine Pipeline-Eingabe.</span><span class="sxs-lookup"><span data-stu-id="28e90-131">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="28e90-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28e90-132">OUTPUTS</span></span>

###  
<span data-ttu-id="28e90-133">Dieses Cmdlet erstellt neue Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="28e90-133">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="28e90-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="28e90-134">NOTES</span></span>

## <span data-ttu-id="28e90-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28e90-135">RELATED LINKS</span></span>

[<span data-ttu-id="28e90-136">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="28e90-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="28e90-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="28e90-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="28e90-138">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="28e90-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


