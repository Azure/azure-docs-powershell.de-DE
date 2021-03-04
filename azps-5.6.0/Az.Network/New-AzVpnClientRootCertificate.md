---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 866a3b9ac28de57a71fce5fb84b2fa1144d0ff8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924659"
---
# <span data-ttu-id="24c35-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="24c35-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="24c35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24c35-102">SYNOPSIS</span></span>
<span data-ttu-id="24c35-103">Erstellt ein neues VPN-Clientstammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="24c35-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="24c35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24c35-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24c35-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24c35-105">DESCRIPTION</span></span>
<span data-ttu-id="24c35-106">Das **Cmdlet New-AzVpnClientRootCertificate** erstellt ein neues VPN-Stammzertifikat für die Verwendung auf einem Gateway für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="24c35-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="24c35-107">Stammzertifikate sind X.509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: Alle anderen zertifikate, die im Gateway verwendet werden, vertrauen dem Stammzertifikat.</span><span class="sxs-lookup"><span data-stu-id="24c35-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="24c35-108">Dieses Cmdlet erstellt ein eigenständiges Zertifikat, das keinem virtuellen Gateway zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="24c35-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="24c35-109">Stattdessen wird das von **New-AzVpnClientRootCertificate** erstellte Zertifikat beim Erstellen eines neuen Gateways in Verbindung mit dem cmdlet New-AzVirtualNetworkGateway verwendet.</span><span class="sxs-lookup"><span data-stu-id="24c35-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="24c35-110">Angenommen, Sie erstellen ein neues Zertifikat und speichern es in einer Variablen namens $Certificate.</span><span class="sxs-lookup"><span data-stu-id="24c35-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="24c35-111">Sie können dieses Zertifikatobjekt dann verwenden, wenn Sie ein neues virtuelles Gateway erstellen.</span><span class="sxs-lookup"><span data-stu-id="24c35-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="24c35-112">Zum Beispiel `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="24c35-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="24c35-113">Weitere Informationen finden Sie in der Dokumentation zum New-AzVirtualNetworkGateway Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24c35-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="24c35-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="24c35-114">EXAMPLES</span></span>

### <span data-ttu-id="24c35-115">Beispiel 1: Erstellen eines Clientstammzertifikats</span><span class="sxs-lookup"><span data-stu-id="24c35-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="24c35-116">In diesem Beispiel wird ein Clientstammzertifikat erstellt und das Zertifikatobjekt in einer Variablen namens $Certificate.</span><span class="sxs-lookup"><span data-stu-id="24c35-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="24c35-117">Diese Variable kann dann vom **Cmdlet New-AzVirtualNetworkGateway** verwendet werden, um einem neuen virtuellen Netzwerkgateway ein Stammzertifikat hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="24c35-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="24c35-118">Der erste Befehl verwendet das **Cmdlet Get-Content,** um eine zuvor exportierte Textdarstellung des Stammzertifikats zu erhalten. diese Textdaten in einer Variablen mit dem Namen $Text.</span><span class="sxs-lookup"><span data-stu-id="24c35-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="24c35-119">Der zweite Befehl verwendet dann eine for-Schleife, um den ganzen Text mit Ausnahme der ersten und der letzten Zeile zu extrahieren und den extrahierten Text in einer Variablen namens $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="24c35-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="24c35-120">Der dritte Befehl verwendet das **Cmdlet New-AzVpnClientRootCertificate** zum Erstellen des Zertifikats und speichert das erstellte Objekt in einer Variablen namens $Certificate.</span><span class="sxs-lookup"><span data-stu-id="24c35-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="24c35-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="24c35-121">PARAMETERS</span></span>

### <span data-ttu-id="24c35-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c35-122">-DefaultProfile</span></span>
<span data-ttu-id="24c35-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24c35-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24c35-124">-Name</span><span class="sxs-lookup"><span data-stu-id="24c35-124">-Name</span></span>
<span data-ttu-id="24c35-125">Gibt einen Namen für das neue Clientstammzertifikat an.</span><span class="sxs-lookup"><span data-stu-id="24c35-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="24c35-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="24c35-126">-PublicCertData</span></span>
<span data-ttu-id="24c35-127">Gibt eine Textdarstellung des Stammzertifikats an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="24c35-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="24c35-128">Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (unter Verwendung der Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="24c35-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="24c35-129">Eine ähnliche Ausgabe sollte angezeigt werden (beachten Sie, dass die tatsächliche Ausgabe viel mehr Textzeilen enthält als das hier gezeigte abgekürzte Beispiel): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo 09982CVVFAw8w ----- END CERTIFICATE ----- Das PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (----- BEGIN CERTIFICATE -----) und der letzten Zeile (----- END CERTIFICATE -----) in der Datei.</span><span class="sxs-lookup"><span data-stu-id="24c35-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="24c35-130">Sie können die PublicCertData mithilfe von Windows PowerShell-Befehlen wie diesem abrufen: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = für ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="24c35-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="24c35-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c35-131">CommonParameters</span></span>
<span data-ttu-id="24c35-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c35-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c35-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c35-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c35-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="24c35-134">INPUTS</span></span>

### <span data-ttu-id="24c35-135">System.String</span><span class="sxs-lookup"><span data-stu-id="24c35-135">System.String</span></span>

## <span data-ttu-id="24c35-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="24c35-136">OUTPUTS</span></span>

### <span data-ttu-id="24c35-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="24c35-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="24c35-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="24c35-138">NOTES</span></span>

## <span data-ttu-id="24c35-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="24c35-139">RELATED LINKS</span></span>

[<span data-ttu-id="24c35-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="24c35-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="24c35-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="24c35-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="24c35-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="24c35-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


