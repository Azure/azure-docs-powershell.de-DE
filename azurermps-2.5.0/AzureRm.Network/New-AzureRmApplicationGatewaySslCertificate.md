---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: e22760c2838cf0b4fb0597dbd45532374b604b79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848435"
---
# <span data-ttu-id="fe030-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe030-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="fe030-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe030-102">SYNOPSIS</span></span>
<span data-ttu-id="fe030-103">Erstellt ein SSL-Zertifikat für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="fe030-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe030-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe030-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe030-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe030-105">DESCRIPTION</span></span>
<span data-ttu-id="fe030-106">Das Cmdlet **New-AzureRmApplicationGatewaySslCertificate** erstellt ein SSL-Zertifikat für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="fe030-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="fe030-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe030-107">EXAMPLES</span></span>

### <span data-ttu-id="fe030-108">Beispiel 1: Erstellen eines SSL-Zertifikats für ein Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="fe030-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="fe030-109">Dieser Befehl erstellt ein SSL-Zertifikat mit dem Namen "Cert01" für das Standard Anwendungsgateway und speichert das Ergebnis in der Variablen mit dem Namen "$CERT".</span><span class="sxs-lookup"><span data-stu-id="fe030-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="fe030-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe030-110">PARAMETERS</span></span>

### <span data-ttu-id="fe030-111">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="fe030-111">-CertificateFile</span></span>
<span data-ttu-id="fe030-112">Gibt den Pfad der PFX-Datei des SSL-Zertifikats an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fe030-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fe030-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe030-113">-DefaultProfile</span></span>
<span data-ttu-id="fe030-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe030-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe030-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fe030-115">-Name</span></span>
<span data-ttu-id="fe030-116">Gibt den Namen des SSL-Zertifikats an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fe030-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fe030-117">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="fe030-117">-Password</span></span>
<span data-ttu-id="fe030-118">Gibt das Kennwort des SSL an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fe030-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fe030-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe030-119">CommonParameters</span></span>
<span data-ttu-id="fe030-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe030-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe030-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe030-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe030-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe030-122">INPUTS</span></span>

### <span data-ttu-id="fe030-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fe030-123">System.String</span></span>

## <span data-ttu-id="fe030-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe030-124">OUTPUTS</span></span>

### <span data-ttu-id="fe030-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe030-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="fe030-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe030-126">NOTES</span></span>

## <span data-ttu-id="fe030-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe030-127">RELATED LINKS</span></span>

[<span data-ttu-id="fe030-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe030-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="fe030-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe030-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="fe030-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe030-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="fe030-131">Satz-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe030-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


