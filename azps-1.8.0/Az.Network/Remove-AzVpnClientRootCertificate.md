---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: ad000878256eea429582881be90e2b15156015d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660294"
---
# <span data-ttu-id="477c8-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="477c8-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="477c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="477c8-102">SYNOPSIS</span></span>
<span data-ttu-id="477c8-103">Entfernt ein vorhandenes VPN-Client-Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="477c8-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="477c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="477c8-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="477c8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="477c8-105">DESCRIPTION</span></span>
<span data-ttu-id="477c8-106">Das Cmdlet **Remove-AzVpnClientRootCertificate** entfernt das angegebene Stammzertifikat von einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="477c8-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="477c8-107">Stammzertifikate sind X. 509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: alle anderen auf dem Gateway verwendeten Zertifikate vertrauen dem Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="477c8-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="477c8-108">Wenn Sie ein Stammzertifikat Computer entfernen, die das Zertifikat für Authentifizierungszwecke verwenden, kann keine Verbindung mehr mit dem Gateway hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="477c8-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="477c8-109">Wenn Sie **Remove-AzVpnClientRootCertificate** verwenden, müssen Sie sowohl den Zertifikatsnamen als auch eine Textdarstellung der Zertifikatsdaten angeben.</span><span class="sxs-lookup"><span data-stu-id="477c8-109">When you use **Remove-AzVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="477c8-110">Weitere Informationen zur Textdarstellung eines Zertifikats finden Sie in der Beschreibung des *PublicCertData* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="477c8-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="477c8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="477c8-111">EXAMPLES</span></span>

### <span data-ttu-id="477c8-112">Beispiel 1: Entfernen eines Client Stammzertifikats von einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="477c8-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="477c8-113">In diesem Beispiel wird ein Client-Stammzertifikat namens ContosoRootCertificate aus dem virtuellen Netzwerkgateway ContosoVirtualGateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="477c8-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="477c8-114">Der erste Befehl verwendet das Cmdlet " **Get-Content** ", um eine zuvor exportierte Textdarstellung des Zertifikats abzurufen. Diese Textdarstellung wird in einer Variablen mit dem Namen $Text gespeichert.</span><span class="sxs-lookup"><span data-stu-id="477c8-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="477c8-115">Der zweite Befehl verwendet dann eine for-Schleife, um den gesamten Text in $Text mit Ausnahme der ersten Zeile und der letzten Zeile zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="477c8-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="477c8-116">Dieser extrahierte Text wird in einer Variablen mit dem Namen $CertificateText gespeichert.</span><span class="sxs-lookup"><span data-stu-id="477c8-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="477c8-117">Der dritte Befehl verwendet die in der $CertificateText-Variablen gespeicherten Informationen zusammen mit dem Cmdlet **Remove-AzVpnClientRootCertificate** , um das Zertifikat vom Gateway zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="477c8-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="477c8-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="477c8-118">PARAMETERS</span></span>

### <span data-ttu-id="477c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477c8-119">-DefaultProfile</span></span>
<span data-ttu-id="477c8-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="477c8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="477c8-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="477c8-121">-PublicCertData</span></span>
<span data-ttu-id="477c8-122">Gibt die Textdarstellung des zu entfernende Stammzertifikats an.</span><span class="sxs-lookup"><span data-stu-id="477c8-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="477c8-123">Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (mit Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="477c8-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="477c8-124">Es sollte eine Ausgabe ähnlich der folgenden angezeigt werden (Beachten Sie, dass die tatsächliche Ausgabe viele weitere Textzeilen enthält, als das hier gezeigte verkürzte Beispiel):-----Zertifikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Ende des Zertifikats-----der PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (-----BEGIN Certificate-----) und der letzten Zeile (-----Ende des Zertifikats-----) in der Datei.</span><span class="sxs-lookup"><span data-stu-id="477c8-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="477c8-125">Sie können die PublicCertData mit Windows PowerShell-Befehlen abrufen, die wie folgt aussehen: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = für ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="477c8-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="477c8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="477c8-126">-ResourceGroupName</span></span>
<span data-ttu-id="477c8-127">Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="477c8-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="477c8-128">Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="477c8-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="477c8-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="477c8-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="477c8-130">Gibt den Namen des virtuellen Netzwerkgateways an, aus dem das Zertifikat entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="477c8-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="477c8-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="477c8-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="477c8-132">Gibt den Namen des Client Stammzertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="477c8-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="477c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477c8-133">CommonParameters</span></span>
<span data-ttu-id="477c8-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="477c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477c8-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="477c8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477c8-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="477c8-136">INPUTS</span></span>

### <span data-ttu-id="477c8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="477c8-137">System.String</span></span>

## <span data-ttu-id="477c8-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="477c8-138">OUTPUTS</span></span>

### <span data-ttu-id="477c8-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="477c8-139">System.Boolean</span></span>

## <span data-ttu-id="477c8-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="477c8-140">NOTES</span></span>

## <span data-ttu-id="477c8-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="477c8-141">RELATED LINKS</span></span>

[<span data-ttu-id="477c8-142">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="477c8-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="477c8-143">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="477c8-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="477c8-144">Neu – AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="477c8-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


