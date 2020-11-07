---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 2f5d73cd06d975d6458776dee4242b392b5c160b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850772"
---
# <span data-ttu-id="9407e-101">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9407e-101">Add-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="9407e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9407e-102">SYNOPSIS</span></span>
<span data-ttu-id="9407e-103">Fügt ein VPN-Client-Stammzertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="9407e-103">Adds a VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9407e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9407e-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9407e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9407e-105">DESCRIPTION</span></span>
<span data-ttu-id="9407e-106">Mit dem Cmdlet **Add-AzureRmVpnClientRootCertificate** wird ein Stammzertifikat zu einem virtuellen Netzwerkgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9407e-106">The **Add-AzureRmVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="9407e-107">Stammzertifikate sind X. 509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9407e-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="9407e-108">Im Design Vertrauen alle auf dem Gateway verwendeten Zertifikate dem Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="9407e-108">By design, all certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="9407e-109">Dieses Cmdlet weist ein vorhandenes Zertifikat als Gateway-Stammzertifikat zu.</span><span class="sxs-lookup"><span data-stu-id="9407e-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="9407e-110">Wenn Sie nicht über ein X. 509-Zertifikat verfügen, können Sie ein Zertifikat über Ihre Infrastruktur öffentlicher Schlüssel generieren oder einen Zertifikat Generator wie makecert.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="9407e-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>

<span data-ttu-id="9407e-111">Wenn Sie ein Stammzertifikat hinzufügen möchten, müssen Sie den Zertifikatnamen angeben und eine nur-Text-Darstellung des Zertifikats bereitstellen (Weitere Informationen finden Sie *im PublicCertData* -Parameter).</span><span class="sxs-lookup"><span data-stu-id="9407e-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="9407e-112">Azure ermöglicht Ihnen, einem Gateway mehr als ein Stammzertifikat zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="9407e-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="9407e-113">Mehrere Stammzertifikate werden häufig von Organisationen bereitgestellt, die Benutzer aus mehr als einem Unternehmen einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="9407e-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="9407e-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9407e-114">EXAMPLES</span></span>

### <span data-ttu-id="9407e-115">Beispiel 1: Hinzufügen eines Client Stammzertifikats zu einem virtuellen Gateway</span><span class="sxs-lookup"><span data-stu-id="9407e-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="9407e-116">In diesem Beispiel wird ein Client-Stammzertifikat zu einem virtuellen Gateway mit dem Namen ContosoVirtualGateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9407e-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="9407e-117">Der erste Befehl verwendet das Cmdlet " **Get-Content** ", um eine zuvor exportierte Textdarstellung des Stammzertifikats abzurufen, und speichert diese Textdaten als die Variable mit dem Namen "$Text".</span><span class="sxs-lookup"><span data-stu-id="9407e-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>

<span data-ttu-id="9407e-118">Der zweite Befehl verwendet dann eine for-Schleife, um den gesamten Text mit Ausnahme der ersten Zeile und der letzten Zeile zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="9407e-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="9407e-119">Der extrahierte Text wird in einer Variablen mit dem Namen $CertificateText gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9407e-119">The extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="9407e-120">Der dritte Befehl verwendet dann den in $CertificateText gespeicherten Text mit dem Cmdlet **Add-AzureRmVpnClientRootCertificate** , um das Stammzertifikat zum Gateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9407e-120">The third command then uses the text stored in $CertificateText with the **Add-AzureRmVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="9407e-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="9407e-121">PARAMETERS</span></span>

### <span data-ttu-id="9407e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9407e-122">-DefaultProfile</span></span>
<span data-ttu-id="9407e-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9407e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9407e-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="9407e-124">-PublicCertData</span></span>
<span data-ttu-id="9407e-125">Gibt die Textdarstellung des Stammzertifikats an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9407e-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="9407e-126">Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (mit Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="9407e-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="9407e-127">Wenn Sie dies tun, wird die Ausgabe ähnlich wie in der folgenden Abbildung angezeigt (Beachten Sie, dass die tatsächliche Ausgabe viele weitere Textzeilen enthalten wird, als das hier gezeigte abgekürzte Beispiel):</span><span class="sxs-lookup"><span data-stu-id="9407e-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="9407e-128">-----Zertifikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Abschlusszertifikat starten-----</span><span class="sxs-lookup"><span data-stu-id="9407e-128">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="9407e-129">Der PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (-----BEGIN Certificate-----) und der letzten Zeile (-----Ende des Zertifikats-----) in der Datei.</span><span class="sxs-lookup"><span data-stu-id="9407e-129">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="9407e-130">Sie können diese Daten mithilfe von Windows PowerShell-Befehlen abrufen, die wie folgt aussehen: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="9407e-130">You can retrieve this data  by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="9407e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9407e-131">-ResourceGroupName</span></span>
<span data-ttu-id="9407e-132">Gibt den Namen der Ressourcengruppe an, der das Stammzertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9407e-132">Specifies the name of the resource group that the root certificate is assigned to.</span></span>

<span data-ttu-id="9407e-133">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="9407e-133">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="9407e-134">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9407e-134">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9407e-135">Gibt den Namen des virtuellen Netzwerkgateways an, auf dem das Zertifikat hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9407e-135">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="9407e-136">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="9407e-136">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="9407e-137">Gibt den Namen des Client-Stammzertifikats an, das von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9407e-137">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9407e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9407e-138">CommonParameters</span></span>
<span data-ttu-id="9407e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9407e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9407e-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9407e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9407e-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9407e-141">INPUTS</span></span>

## <span data-ttu-id="9407e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9407e-142">OUTPUTS</span></span>

### <span data-ttu-id="9407e-143">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9407e-143">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="9407e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="9407e-144">NOTES</span></span>

## <span data-ttu-id="9407e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9407e-145">RELATED LINKS</span></span>

[<span data-ttu-id="9407e-146">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9407e-146">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="9407e-147">Neu – AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9407e-147">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="9407e-148">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9407e-148">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


