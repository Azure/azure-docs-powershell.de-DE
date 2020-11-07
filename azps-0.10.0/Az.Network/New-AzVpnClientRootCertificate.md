---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: bd260deb8e43450b2feacb3c60f34ed6cc4003be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841251"
---
# <span data-ttu-id="1a9d5-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1a9d5-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="1a9d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="1a9d5-103">Erstellt ein neues VPN-Client-Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="1a9d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a9d5-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a9d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a9d5-105">DESCRIPTION</span></span>
<span data-ttu-id="1a9d5-106">Das Cmdlet **New-AzVpnClientRootCertificate** erstellt ein neues VPN-Stammzertifikat zur Verwendung auf einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="1a9d5-107">Stammzertifikate sind X. 509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: alle anderen auf dem Gateway verwendeten Zertifikate vertrauen dem Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="1a9d5-108">Mit diesem Cmdlet wird ein eigenständiges Zertifikat erstellt, das keinem virtuellen Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="1a9d5-109">Stattdessen wird das von **New-AzVpnClientRootCertificate** erstellte Zertifikat zusammen mit dem New-AzVirtualNetworkGateway-Cmdlet beim Erstellen eines neuen Gateways verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="1a9d5-110">Angenommen, Sie erstellen ein neues Zertifikat und speichern es in einer Variablen mit dem Namen $Certificate.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="1a9d5-111">Sie können dieses Certificate-Objekt dann verwenden, wenn Sie ein neues virtuelles Gateway erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="1a9d5-112">Zum Beispiel</span><span class="sxs-lookup"><span data-stu-id="1a9d5-112">For instance,</span></span>

`New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

<span data-ttu-id="1a9d5-113">Weitere Informationen finden Sie in der Dokumentation zum New-AzVirtualNetworkGateway-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="1a9d5-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a9d5-114">EXAMPLES</span></span>

### <span data-ttu-id="1a9d5-115">Beispiel 1: Erstellen eines aclient-Stammzertifikats</span><span class="sxs-lookup"><span data-stu-id="1a9d5-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="1a9d5-116">In diesem Beispiel wird ein Client-Stammzertifikat erstellt und das Certificate-Objekt in einer Variablen mit dem Namen $Certificate gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="1a9d5-117">Diese Variable kann dann vom Cmdlet **New-AzVirtualNetworkGateway** verwendet werden, um ein Stammzertifikat zu einem neuen virtuellen Netzwerkgateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>

<span data-ttu-id="1a9d5-118">Der erste Befehl verwendet das Cmdlet " **Get-Content** ", um eine zuvor exportierte Textdarstellung des Stammzertifikats abzurufen. Diese Textdaten werden in einer Variablen mit dem Namen $Text gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>

<span data-ttu-id="1a9d5-119">Der zweite Befehl verwendet dann eine for-Schleife, um den gesamten Text mit Ausnahme der ersten Zeile und der letzten Zeile zu extrahieren, und speichert den extrahierten Text in einer Variablen mit dem Namen $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>

<span data-ttu-id="1a9d5-120">Der dritte Befehl verwendet das Cmdlet **New-AzVpnClientRootCertificate** , um das Zertifikat zu erstellen und das erstellte Objekt in einer Variablen mit dem Namen $Certificate zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="1a9d5-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a9d5-121">PARAMETERS</span></span>

### <span data-ttu-id="1a9d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a9d5-122">-DefaultProfile</span></span>
<span data-ttu-id="1a9d5-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a9d5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1a9d5-124">-Name</span></span>
<span data-ttu-id="1a9d5-125">Gibt einen Namen für das neue Client-Stammzertifikat an.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-125">Specifies a name for the new client root certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9d5-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="1a9d5-126">-PublicCertData</span></span>
<span data-ttu-id="1a9d5-127">Gibt eine Textdarstellung des Stammzertifikats an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="1a9d5-128">Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (mit Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="1a9d5-129">Die Ausgabe sollte ähnlich wie diese angezeigt werden (Beachten Sie, dass die tatsächliche Ausgabe viele weitere Textzeilen enthält als das hier gezeigte abgekürzte Beispiel):</span><span class="sxs-lookup"><span data-stu-id="1a9d5-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="1a9d5-130">-----Zertifikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Abschlusszertifikat starten-----</span><span class="sxs-lookup"><span data-stu-id="1a9d5-130">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="1a9d5-131">Der PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (-----BEGIN Certificate-----) und der letzten Zeile (-----Ende des Zertifikats-----) in der Datei.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-131">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="1a9d5-132">Sie können die PublicCertData mithilfe von Windows PowerShell-Befehlen abrufen, die wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="1a9d5-132">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="1a9d5-133">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = für ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="1a9d5-133">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="1a9d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a9d5-134">CommonParameters</span></span>
<span data-ttu-id="1a9d5-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a9d5-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a9d5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a9d5-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a9d5-137">INPUTS</span></span>

###  
<span data-ttu-id="1a9d5-138">Dieses Cmdlet akzeptiert keine Pipeline-Eingabe.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-138">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="1a9d5-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a9d5-139">OUTPUTS</span></span>

###  
<span data-ttu-id="1a9d5-140">Dieses Cmdlet erstellt neue Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-140">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="1a9d5-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a9d5-141">NOTES</span></span>

## <span data-ttu-id="1a9d5-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a9d5-142">RELATED LINKS</span></span>

[<span data-ttu-id="1a9d5-143">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1a9d5-143">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="1a9d5-144">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1a9d5-144">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="1a9d5-145">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1a9d5-145">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


