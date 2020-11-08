---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003416"
---
# <span data-ttu-id="17b97-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="17b97-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="17b97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17b97-102">SYNOPSIS</span></span>
<span data-ttu-id="17b97-103">Erstellt ein neues VPN-Client-Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="17b97-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="17b97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17b97-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17b97-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17b97-105">DESCRIPTION</span></span>
<span data-ttu-id="17b97-106">Das Cmdlet **New-AzVpnClientRootCertificate** erstellt ein neues VPN-Stammzertifikat zur Verwendung auf einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="17b97-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="17b97-107">Stammzertifikate sind X. 509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: alle anderen auf dem Gateway verwendeten Zertifikate vertrauen dem Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="17b97-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="17b97-108">Mit diesem Cmdlet wird ein eigenständiges Zertifikat erstellt, das keinem virtuellen Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="17b97-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="17b97-109">Stattdessen wird das von **New-AzVpnClientRootCertificate** erstellte Zertifikat zusammen mit dem New-AzVirtualNetworkGateway-Cmdlet beim Erstellen eines neuen Gateways verwendet.</span><span class="sxs-lookup"><span data-stu-id="17b97-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="17b97-110">Angenommen, Sie erstellen ein neues Zertifikat und speichern es in einer Variablen mit dem Namen $Certificate.</span><span class="sxs-lookup"><span data-stu-id="17b97-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="17b97-111">Sie können dieses Certificate-Objekt dann verwenden, wenn Sie ein neues virtuelles Gateway erstellen.</span><span class="sxs-lookup"><span data-stu-id="17b97-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="17b97-112">Zum Beispiel `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="17b97-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="17b97-113">Weitere Informationen finden Sie in der Dokumentation zum New-AzVirtualNetworkGateway-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17b97-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="17b97-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17b97-114">EXAMPLES</span></span>

### <span data-ttu-id="17b97-115">Beispiel 1: Erstellen eines Client Stammzertifikats</span><span class="sxs-lookup"><span data-stu-id="17b97-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="17b97-116">In diesem Beispiel wird ein Client-Stammzertifikat erstellt und das Certificate-Objekt in einer Variablen mit dem Namen $Certificate gespeichert.</span><span class="sxs-lookup"><span data-stu-id="17b97-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="17b97-117">Diese Variable kann dann vom Cmdlet **New-AzVirtualNetworkGateway** verwendet werden, um ein Stammzertifikat zu einem neuen virtuellen Netzwerkgateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="17b97-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="17b97-118">Der erste Befehl verwendet das Cmdlet " **Get-Content** ", um eine zuvor exportierte Textdarstellung des Stammzertifikats abzurufen. Diese Textdaten werden in einer Variablen mit dem Namen $Text gespeichert.</span><span class="sxs-lookup"><span data-stu-id="17b97-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="17b97-119">Der zweite Befehl verwendet dann eine for-Schleife, um den gesamten Text mit Ausnahme der ersten Zeile und der letzten Zeile zu extrahieren, und speichert den extrahierten Text in einer Variablen mit dem Namen $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="17b97-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="17b97-120">Der dritte Befehl verwendet das Cmdlet **New-AzVpnClientRootCertificate** , um das Zertifikat zu erstellen und das erstellte Objekt in einer Variablen mit dem Namen $Certificate zu speichern.</span><span class="sxs-lookup"><span data-stu-id="17b97-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="17b97-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="17b97-121">PARAMETERS</span></span>

### <span data-ttu-id="17b97-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b97-122">-DefaultProfile</span></span>
<span data-ttu-id="17b97-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17b97-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17b97-124">-Name</span><span class="sxs-lookup"><span data-stu-id="17b97-124">-Name</span></span>
<span data-ttu-id="17b97-125">Gibt einen Namen für das neue Client-Stammzertifikat an.</span><span class="sxs-lookup"><span data-stu-id="17b97-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="17b97-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="17b97-126">-PublicCertData</span></span>
<span data-ttu-id="17b97-127">Gibt eine Textdarstellung des Stammzertifikats an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="17b97-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="17b97-128">Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (mit Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="17b97-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="17b97-129">Die Ausgabe sollte ähnlich wie diese angezeigt werden (Beachten Sie, dass die tatsächliche Ausgabe viele weitere Textzeilen enthält, als das hier gezeigte abgekürzte Beispiel):-----Zertifikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Ende des Zertifikats-----der PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (-----BEGIN Certificate-----) und der letzten Zeile (-----End Certificate-----) in der Datei.</span><span class="sxs-lookup"><span data-stu-id="17b97-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="17b97-130">Sie können die PublicCertData mithilfe von Windows PowerShell-Befehlen abrufen, die wie folgt aussehen: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = für ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="17b97-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="17b97-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b97-131">CommonParameters</span></span>
<span data-ttu-id="17b97-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b97-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b97-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b97-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b97-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17b97-134">INPUTS</span></span>

### <span data-ttu-id="17b97-135">System. String</span><span class="sxs-lookup"><span data-stu-id="17b97-135">System.String</span></span>

## <span data-ttu-id="17b97-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17b97-136">OUTPUTS</span></span>

### <span data-ttu-id="17b97-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="17b97-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="17b97-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="17b97-138">NOTES</span></span>

## <span data-ttu-id="17b97-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17b97-139">RELATED LINKS</span></span>

[<span data-ttu-id="17b97-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="17b97-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="17b97-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="17b97-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="17b97-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="17b97-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


