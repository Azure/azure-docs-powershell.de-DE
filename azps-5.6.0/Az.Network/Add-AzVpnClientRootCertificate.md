---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 38a6abb631a77d41e38026edd3bef5abe9c70c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932443"
---
# <span data-ttu-id="23aad-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23aad-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="23aad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23aad-102">SYNOPSIS</span></span>
<span data-ttu-id="23aad-103">Fügt ein VPN-Clientstammzertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="23aad-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="23aad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23aad-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23aad-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23aad-105">DESCRIPTION</span></span>
<span data-ttu-id="23aad-106">Das **Add-AzVpnClientRootCertificate-Cmdlet** fügt einem Gateway für virtuelle Netzwerke ein Stammzertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="23aad-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="23aad-107">Stammzertifikate sind X.509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren.</span><span class="sxs-lookup"><span data-stu-id="23aad-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="23aad-108">Standardmäßig vertrauen alle zertifikate, die im Gateway verwendet werden, dem Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="23aad-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="23aad-109">Dieses Cmdlet weist ein vorhandenes Zertifikat als Gatewaystammzertifikat zu.</span><span class="sxs-lookup"><span data-stu-id="23aad-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="23aad-110">Wenn kein X.509-Zertifikat verfügbar ist, können Sie ein Zertifikat über Ihre Infrastruktur für öffentliche Schlüssel generieren oder einen Zertifikatgenerator wie makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="23aad-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="23aad-111">Zum Hinzufügen eines Stammzertifikats müssen Sie den Zertifikatnamen angeben und eine Textdarstellung des Zertifikats bereitstellen (weitere Informationen finden Sie im *Parameter PublicCertData).*</span><span class="sxs-lookup"><span data-stu-id="23aad-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="23aad-112">Azure ermöglicht es Ihnen, einem Gateway mehr als ein Stammzertifikat zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="23aad-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="23aad-113">Mehrere Stammzertifikate werden häufig von Organisationen bereitgestellt, die Benutzer aus mehreren Unternehmen umfassen.</span><span class="sxs-lookup"><span data-stu-id="23aad-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="23aad-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23aad-114">EXAMPLES</span></span>

### <span data-ttu-id="23aad-115">Beispiel 1: Hinzufügen eines Clientstammzertifikats zu einem virtuellen Gateway</span><span class="sxs-lookup"><span data-stu-id="23aad-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="23aad-116">In diesem Beispiel wird einem virtuellen Gateway namens ContosoVirtualGateway ein Clientstammzertifikat hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="23aad-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="23aad-117">Der erste Befehl verwendet das **Get-Content-Cmdlet,** um eine zuvor exportierte Textdarstellung des Stammzertifikats zu erhalten, und speichert diese Textdaten, die die Variable namens $Text.</span><span class="sxs-lookup"><span data-stu-id="23aad-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="23aad-118">Der zweite Befehl verwendet dann eine for-Schleife, um den ganzen Text mit Ausnahme der ersten und der letzten Zeile zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="23aad-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="23aad-119">Der extrahierte Text wird in einer Variablen mit dem Namen $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="23aad-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="23aad-120">Der dritte Befehl verwendet dann den in $CertificateText mit dem **Add-AzVpnClientRootCertificate-Cmdlet** gespeicherten Text, um das Stammzertifikat zum Gateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="23aad-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="23aad-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="23aad-121">PARAMETERS</span></span>

### <span data-ttu-id="23aad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23aad-122">-DefaultProfile</span></span>
<span data-ttu-id="23aad-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23aad-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23aad-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="23aad-124">-PublicCertData</span></span>
<span data-ttu-id="23aad-125">Gibt die Textdarstellung des Stammzertifikats an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="23aad-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="23aad-126">Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (unter Verwendung der Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="23aad-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="23aad-127">In diesem Beispiel wird eine ähnliche Ausgabe wie die folgende angezeigt (beachten Sie, dass die tatsächliche Ausgabe viel mehr Textzeilen enthält als das hier gezeigte abgekürzte Beispiel): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- Das PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (----- BEGIN CERTIFICATE -----) und der letzten Zeile (----- END CERTIFICATE -----) in der Datei.</span><span class="sxs-lookup"><span data-stu-id="23aad-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="23aad-128">Sie können diese Daten mithilfe der folgenden Windows PowerShell abrufen: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="23aad-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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

### <span data-ttu-id="23aad-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23aad-129">-ResourceGroupName</span></span>
<span data-ttu-id="23aad-130">Gibt den Namen der Ressourcengruppe an, der das Stammzertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="23aad-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="23aad-131">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="23aad-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="23aad-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="23aad-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="23aad-133">Gibt den Namen des Virtuellen Netzwerkgateways an, in dem das Zertifikat hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="23aad-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="23aad-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="23aad-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="23aad-135">Gibt den Namen des Clientstammzertifikats an, das von diesem Cmdlet addiert wird.</span><span class="sxs-lookup"><span data-stu-id="23aad-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="23aad-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23aad-136">CommonParameters</span></span>
<span data-ttu-id="23aad-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23aad-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23aad-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23aad-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23aad-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23aad-139">INPUTS</span></span>

### <span data-ttu-id="23aad-140">System.String</span><span class="sxs-lookup"><span data-stu-id="23aad-140">System.String</span></span>

## <span data-ttu-id="23aad-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23aad-141">OUTPUTS</span></span>

### <span data-ttu-id="23aad-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23aad-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="23aad-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="23aad-143">NOTES</span></span>

## <span data-ttu-id="23aad-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="23aad-144">RELATED LINKS</span></span>

[<span data-ttu-id="23aad-145">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23aad-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="23aad-146">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23aad-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="23aad-147">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23aad-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


