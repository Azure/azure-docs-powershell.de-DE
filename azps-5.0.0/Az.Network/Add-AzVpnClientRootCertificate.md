---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180218"
---
# <span data-ttu-id="fab11-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fab11-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="fab11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fab11-102">SYNOPSIS</span></span>
<span data-ttu-id="fab11-103">Fügt ein VPN-Client-Stammzertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="fab11-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="fab11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fab11-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fab11-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fab11-105">DESCRIPTION</span></span>
<span data-ttu-id="fab11-106">Mit dem Cmdlet **Add-AzVpnClientRootCertificate** wird ein Stammzertifikat zu einem virtuellen Netzwerkgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fab11-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="fab11-107">Stammzertifikate sind X. 509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fab11-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="fab11-108">Im Design Vertrauen alle auf dem Gateway verwendeten Zertifikate dem Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="fab11-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="fab11-109">Dieses Cmdlet weist ein vorhandenes Zertifikat als Gateway-Stammzertifikat zu.</span><span class="sxs-lookup"><span data-stu-id="fab11-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="fab11-110">Wenn Sie nicht über ein X. 509-Zertifikat verfügen, können Sie ein Zertifikat über Ihre Infrastruktur öffentlicher Schlüssel generieren oder einen Zertifikat Generator wie makecert.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="fab11-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="fab11-111">Wenn Sie ein Stammzertifikat hinzufügen möchten, müssen Sie den Zertifikatnamen angeben und eine nur-Text-Darstellung des Zertifikats bereitstellen (Weitere Informationen finden Sie *im PublicCertData* -Parameter).</span><span class="sxs-lookup"><span data-stu-id="fab11-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="fab11-112">Azure ermöglicht Ihnen, einem Gateway mehr als ein Stammzertifikat zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="fab11-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="fab11-113">Mehrere Stammzertifikate werden häufig von Organisationen bereitgestellt, die Benutzer aus mehr als einem Unternehmen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="fab11-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="fab11-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fab11-114">EXAMPLES</span></span>

### <span data-ttu-id="fab11-115">Beispiel 1: Hinzufügen eines Client Stammzertifikats zu einem virtuellen Gateway</span><span class="sxs-lookup"><span data-stu-id="fab11-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="fab11-116">In diesem Beispiel wird ein Client-Stammzertifikat zu einem virtuellen Gateway mit dem Namen ContosoVirtualGateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fab11-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="fab11-117">Der erste Befehl verwendet das Cmdlet " **Get-Content** ", um eine zuvor exportierte Textdarstellung des Stammzertifikats abzurufen, und speichert diese Textdaten als die Variable mit dem Namen "$Text".</span><span class="sxs-lookup"><span data-stu-id="fab11-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="fab11-118">Der zweite Befehl verwendet dann eine for-Schleife, um den gesamten Text mit Ausnahme der ersten Zeile und der letzten Zeile zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="fab11-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="fab11-119">Der extrahierte Text wird in einer Variablen mit dem Namen $CertificateText gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fab11-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="fab11-120">Der dritte Befehl verwendet dann den in $CertificateText gespeicherten Text mit dem Cmdlet **Add-AzVpnClientRootCertificate** , um das Stammzertifikat zum Gateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fab11-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="fab11-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="fab11-121">PARAMETERS</span></span>

### <span data-ttu-id="fab11-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab11-122">-DefaultProfile</span></span>
<span data-ttu-id="fab11-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fab11-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fab11-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="fab11-124">-PublicCertData</span></span>
<span data-ttu-id="fab11-125">Gibt die Textdarstellung des Stammzertifikats an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fab11-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="fab11-126">Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (mit Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="fab11-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="fab11-127">Wenn Sie dies tun, wird die Ausgabe ähnlich wie in der folgenden Abbildung angezeigt (Beachten Sie, dass die tatsächliche Ausgabe viele weitere Textzeilen enthält, als das hier gezeigte verkürzte Beispiel):-----Zertifikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Ende des Zertifikats-----der PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (-----BEGIN Certificate-----) und der letzten Zeile (-----End Certificate-----) in der Datei.</span><span class="sxs-lookup"><span data-stu-id="fab11-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="fab11-128">Sie können diese Daten mithilfe von Windows PowerShell-Befehlen abrufen, die wie folgt aussehen: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="fab11-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="fab11-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab11-129">-ResourceGroupName</span></span>
<span data-ttu-id="fab11-130">Gibt den Namen der Ressourcengruppe an, der das Stammzertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="fab11-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="fab11-131">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="fab11-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="fab11-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="fab11-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="fab11-133">Gibt den Namen des virtuellen Netzwerkgateways an, auf dem das Zertifikat hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fab11-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="fab11-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="fab11-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="fab11-135">Gibt den Namen des Client-Stammzertifikats an, das von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fab11-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="fab11-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab11-136">CommonParameters</span></span>
<span data-ttu-id="fab11-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab11-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab11-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab11-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab11-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fab11-139">INPUTS</span></span>

### <span data-ttu-id="fab11-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fab11-140">System.String</span></span>

## <span data-ttu-id="fab11-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fab11-141">OUTPUTS</span></span>

### <span data-ttu-id="fab11-142">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fab11-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="fab11-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="fab11-143">NOTES</span></span>

## <span data-ttu-id="fab11-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fab11-144">RELATED LINKS</span></span>

[<span data-ttu-id="fab11-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fab11-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="fab11-146">Neu – AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fab11-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="fab11-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fab11-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


