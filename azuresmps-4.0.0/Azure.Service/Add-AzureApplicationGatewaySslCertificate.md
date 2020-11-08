---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005942"
---
# <span data-ttu-id="53f02-101">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53f02-101">Add-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="53f02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53f02-102">SYNOPSIS</span></span>
<span data-ttu-id="53f02-103">Fügt ein SSL-Zertifikat zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="53f02-103">Adds an SSL certificate to an Application Gateway.</span></span>

## <span data-ttu-id="53f02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53f02-104">SYNTAX</span></span>

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="53f02-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53f02-105">DESCRIPTION</span></span>
<span data-ttu-id="53f02-106">Das Cmdlet **Add-AzureApplicationGatewaySslCertificate** fügt einem Azure Application Gateway ein SSL-Zertifikat (Secure Sockets Layer) hinzu.</span><span class="sxs-lookup"><span data-stu-id="53f02-106">The **Add-AzureApplicationGatewaySslCertificate** cmdlet adds a Secure Sockets Layer (SSL) certificate to an Azure Application Gateway.</span></span>

## <span data-ttu-id="53f02-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53f02-107">EXAMPLES</span></span>

### <span data-ttu-id="53f02-108">Beispiel 1: Hinzufügen eines SSL-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="53f02-108">Example 1: Add an SSL certificate</span></span>
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

<span data-ttu-id="53f02-109">Dieser Befehl fügt dem Anwendungs Gateway mit dem Namen ApplicationGateway08 ein SSL-Zertifikat mit dem Namen "SslCertificate13" hinzu.</span><span class="sxs-lookup"><span data-stu-id="53f02-109">This command adds an SSL certificate named SslCertificate13 to the Application Gateway named ApplicationGateway08.</span></span>
<span data-ttu-id="53f02-110">Der Befehl gibt den Pfad der Zertifikatsdatei und das Kennwort für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="53f02-110">The command specifies the path of the certificate file and the password for the certificate.</span></span>

## <span data-ttu-id="53f02-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="53f02-111">PARAMETERS</span></span>

### <span data-ttu-id="53f02-112">-Certificatedatei</span><span class="sxs-lookup"><span data-stu-id="53f02-112">-CertificateFile</span></span>
<span data-ttu-id="53f02-113">Gibt den Pfad einer SSL-Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="53f02-113">Specifies the path of an SSL certificate file.</span></span>
<span data-ttu-id="53f02-114">Mit diesem Cmdlet wird das Zertifikat in der Datei hinzugefügt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="53f02-114">This cmdlet adds the certificate in the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="53f02-115">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="53f02-115">-CertificateName</span></span>
<span data-ttu-id="53f02-116">Gibt den Namen eines SSL-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="53f02-116">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="53f02-117">Mit diesem Cmdlet wird das Zertifikat hinzugefügt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="53f02-117">This cmdlet adds the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="53f02-118">-Name</span><span class="sxs-lookup"><span data-stu-id="53f02-118">-Name</span></span>
<span data-ttu-id="53f02-119">Gibt den Namen des Anwendungs Gateways an, dem dieses Cmdlet ein SSL-Zertifikat hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="53f02-119">Specifies the name of the Application Gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="53f02-120">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="53f02-120">-Password</span></span>
<span data-ttu-id="53f02-121">Gibt das Kennwort des SSL-Zertifikats an, das von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="53f02-121">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="53f02-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="53f02-122">-Profile</span></span>
<span data-ttu-id="53f02-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="53f02-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53f02-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="53f02-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f02-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f02-125">CommonParameters</span></span>
<span data-ttu-id="53f02-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f02-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f02-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53f02-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f02-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53f02-128">INPUTS</span></span>

### <span data-ttu-id="53f02-129">System. String</span><span class="sxs-lookup"><span data-stu-id="53f02-129">System.String</span></span>

## <span data-ttu-id="53f02-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53f02-130">OUTPUTS</span></span>

### <span data-ttu-id="53f02-131">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="53f02-131">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="53f02-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="53f02-132">NOTES</span></span>

## <span data-ttu-id="53f02-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53f02-133">RELATED LINKS</span></span>

[<span data-ttu-id="53f02-134">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53f02-134">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="53f02-135">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53f02-135">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
