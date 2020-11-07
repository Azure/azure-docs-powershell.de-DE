---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 60d46a3d61f0799618107e9bc0727a3ff31fc337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841383"
---
# <span data-ttu-id="e3fcf-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3fcf-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e3fcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fcf-103">Erstellt ein SSL-Zertifikat für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e3fcf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3fcf-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3fcf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="e3fcf-106">Das Cmdlet **New-AzApplicationGatewaySslCertificate** erstellt ein SSL-Zertifikat für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e3fcf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3fcf-107">EXAMPLES</span></span>

### <span data-ttu-id="e3fcf-108">Beispiel 1: Erstellen eines SSL-Zertifikats für ein Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e3fcf-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="e3fcf-109">Dieser Befehl erstellt ein SSL-Zertifikat mit dem Namen "Cert01" für das Standard Anwendungsgateway und speichert das Ergebnis in der Variablen mit dem Namen "$CERT".</span><span class="sxs-lookup"><span data-stu-id="e3fcf-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="e3fcf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3fcf-110">PARAMETERS</span></span>

### <span data-ttu-id="e3fcf-111">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="e3fcf-111">-CertificateFile</span></span>
<span data-ttu-id="e3fcf-112">Gibt den Pfad der PFX-Datei des SSL-Zertifikats an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e3fcf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fcf-113">-DefaultProfile</span></span>
<span data-ttu-id="e3fcf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3fcf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e3fcf-115">-Name</span></span>
<span data-ttu-id="e3fcf-116">Gibt den Namen des SSL-Zertifikats an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e3fcf-117">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="e3fcf-117">-Password</span></span>
<span data-ttu-id="e3fcf-118">Gibt das Kennwort des SSL an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3fcf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fcf-119">CommonParameters</span></span>
<span data-ttu-id="e3fcf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3fcf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fcf-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3fcf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fcf-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3fcf-122">INPUTS</span></span>

### <span data-ttu-id="e3fcf-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e3fcf-123">System.String</span></span>

## <span data-ttu-id="e3fcf-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3fcf-124">OUTPUTS</span></span>

### <span data-ttu-id="e3fcf-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3fcf-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e3fcf-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3fcf-126">NOTES</span></span>

## <span data-ttu-id="e3fcf-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3fcf-127">RELATED LINKS</span></span>

[<span data-ttu-id="e3fcf-128">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3fcf-128">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e3fcf-129">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3fcf-129">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e3fcf-130">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3fcf-130">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e3fcf-131">Satz-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e3fcf-131">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


