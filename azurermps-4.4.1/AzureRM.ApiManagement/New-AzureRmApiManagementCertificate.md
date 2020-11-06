---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 55b95cec3e699872688fad5daeb0d2f7e89059c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498057"
---
# <span data-ttu-id="94543-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="94543-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="94543-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94543-102">SYNOPSIS</span></span>
<span data-ttu-id="94543-103">Erstellt ein API-Verwaltungszertifikat, das während der Authentifizierung mit Back-End verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="94543-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94543-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94543-104">SYNTAX</span></span>

### <span data-ttu-id="94543-105">Aus Datei laden (Standard)</span><span class="sxs-lookup"><span data-stu-id="94543-105">Load from file (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94543-106">Unformatierte</span><span class="sxs-lookup"><span data-stu-id="94543-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94543-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94543-107">DESCRIPTION</span></span>
<span data-ttu-id="94543-108">Das Cmdlet **New-AzureRmApiManagementCertificate** erstellt ein Azure API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="94543-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="94543-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94543-109">EXAMPLES</span></span>

### <span data-ttu-id="94543-110">Beispiel 1: Erstellen und Hochladen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="94543-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="94543-111">Mit diesem Befehl wird ein API-Verwaltungszertifikat erstellt und hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="94543-111">This command creates an API Management certificate and uploads it.</span></span>

## <span data-ttu-id="94543-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="94543-112">PARAMETERS</span></span>

### <span data-ttu-id="94543-113">-Certificate-Nr</span><span class="sxs-lookup"><span data-stu-id="94543-113">-CertificateId</span></span>
<span data-ttu-id="94543-114">Gibt die ID des zu erstellenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="94543-114">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="94543-115">Wenn Sie diesen Parameter nicht angeben, wird eine ID für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="94543-115">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94543-116">-Context</span><span class="sxs-lookup"><span data-stu-id="94543-116">-Context</span></span>
<span data-ttu-id="94543-117">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="94543-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94543-118">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="94543-118">-PfxBytes</span></span>
<span data-ttu-id="94543-119">Gibt ein Bytearray der Zertifikatsdatei im PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="94543-119">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="94543-120">Dieser Parameter ist erforderlich, wenn Sie den *PfxFilePath* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="94543-120">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94543-121">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="94543-121">-PfxFilePath</span></span>
<span data-ttu-id="94543-122">Gibt den Pfad zur Zertifikatsdatei im PFX-Format zum Erstellen und Hochladen an.</span><span class="sxs-lookup"><span data-stu-id="94543-122">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="94543-123">Dieser Parameter ist erforderlich, wenn Sie den *PfxBytes* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="94543-123">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Load from file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94543-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="94543-124">-PfxPassword</span></span>
<span data-ttu-id="94543-125">Gibt das Kennwort für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="94543-125">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="94543-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94543-126">-DefaultProfile</span></span>
<span data-ttu-id="94543-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94543-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94543-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94543-128">CommonParameters</span></span>
<span data-ttu-id="94543-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94543-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94543-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94543-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94543-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94543-131">INPUTS</span></span>

## <span data-ttu-id="94543-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94543-132">OUTPUTS</span></span>

### <span data-ttu-id="94543-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="94543-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="94543-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="94543-134">NOTES</span></span>

## <span data-ttu-id="94543-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94543-135">RELATED LINKS</span></span>

[<span data-ttu-id="94543-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="94543-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="94543-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="94543-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="94543-138">Satz-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="94543-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


