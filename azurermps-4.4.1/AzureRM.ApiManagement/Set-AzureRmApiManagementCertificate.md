---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: ca9305b2d5863276c5d898e310dfab8be7488382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664484"
---
# <span data-ttu-id="1d78d-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1d78d-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="1d78d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d78d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d78d-103">Ändert ein API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="1d78d-103">Modifies an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d78d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d78d-104">SYNTAX</span></span>

### <span data-ttu-id="1d78d-105">Aus Datei laden (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d78d-105">Load from file (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1d78d-106">Unformatierte</span><span class="sxs-lookup"><span data-stu-id="1d78d-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d78d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d78d-107">DESCRIPTION</span></span>
<span data-ttu-id="1d78d-108">Das Cmdlet " **Satz-AzureRmApiManagementCertificate** " ändert ein Azure API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="1d78d-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="1d78d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d78d-109">EXAMPLES</span></span>

### <span data-ttu-id="1d78d-110">Beispiel 1: Ändern eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="1d78d-110">Example 1: Modify a certificate</span></span>
```
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="1d78d-111">Mit diesem Befehl wird das angegebene API-Verwaltungszertifikat geändert.</span><span class="sxs-lookup"><span data-stu-id="1d78d-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="1d78d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d78d-112">PARAMETERS</span></span>

### <span data-ttu-id="1d78d-113">-Certificate-Nr</span><span class="sxs-lookup"><span data-stu-id="1d78d-113">-CertificateId</span></span>
<span data-ttu-id="1d78d-114">Gibt die ID des zu ändernden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="1d78d-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="1d78d-115">-Context</span><span class="sxs-lookup"><span data-stu-id="1d78d-115">-Context</span></span>
<span data-ttu-id="1d78d-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1d78d-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1d78d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d78d-117">-PassThru</span></span>
<span data-ttu-id="1d78d-118">passthru</span><span class="sxs-lookup"><span data-stu-id="1d78d-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d78d-119">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="1d78d-119">-PfxBytes</span></span>
<span data-ttu-id="1d78d-120">Gibt ein Bytearray der Zertifikatsdatei im PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="1d78d-120">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="1d78d-121">Dieser Parameter ist erforderlich, wenn Sie den *PfxFilePath* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="1d78d-121">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="1d78d-122">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="1d78d-122">-PfxFilePath</span></span>
<span data-ttu-id="1d78d-123">Gibt den Pfad zur Zertifikatsdatei im PFX-Format zum Erstellen und Hochladen an.</span><span class="sxs-lookup"><span data-stu-id="1d78d-123">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="1d78d-124">Dieser Parameter ist erforderlich, wenn Sie den *PfxBytes* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="1d78d-124">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="1d78d-125">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="1d78d-125">-PfxPassword</span></span>
<span data-ttu-id="1d78d-126">Gibt das Kennwort für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="1d78d-126">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="1d78d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d78d-127">-DefaultProfile</span></span>
<span data-ttu-id="1d78d-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d78d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d78d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d78d-129">CommonParameters</span></span>
<span data-ttu-id="1d78d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d78d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d78d-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d78d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d78d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d78d-132">INPUTS</span></span>

## <span data-ttu-id="1d78d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d78d-133">OUTPUTS</span></span>

### <span data-ttu-id="1d78d-134">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1d78d-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="1d78d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d78d-135">NOTES</span></span>

## <span data-ttu-id="1d78d-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d78d-136">RELATED LINKS</span></span>

[<span data-ttu-id="1d78d-137">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1d78d-137">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1d78d-138">Neu – AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1d78d-138">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1d78d-139">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1d78d-139">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


