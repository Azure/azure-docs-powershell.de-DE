---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7ddfb327931fc7ebb9eac76cdd6818521332483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483190"
---
# <span data-ttu-id="397c0-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="397c0-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="397c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="397c0-102">SYNOPSIS</span></span>
<span data-ttu-id="397c0-103">Erstellt ein API-Verwaltungszertifikat, das während der Authentifizierung mit Back-End verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="397c0-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="397c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="397c0-104">SYNTAX</span></span>

### <span data-ttu-id="397c0-105">Loadfromdatei (Standard)</span><span class="sxs-lookup"><span data-stu-id="397c0-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="397c0-106">Unformatierte</span><span class="sxs-lookup"><span data-stu-id="397c0-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="397c0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="397c0-107">DESCRIPTION</span></span>
<span data-ttu-id="397c0-108">Das Cmdlet **New-AzureRmApiManagementCertificate** erstellt ein Azure API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="397c0-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="397c0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="397c0-109">EXAMPLES</span></span>

### <span data-ttu-id="397c0-110">Beispiel 1: Erstellen und Hochladen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="397c0-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="397c0-111">Mit diesem Befehl wird ein Zertifikat in die API-Verwaltung hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="397c0-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="397c0-112">Dieses Zertifikat kann für die gegenseitige Authentifizierung mit dem Back-End mithilfe von Richtlinien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="397c0-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="397c0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="397c0-113">PARAMETERS</span></span>

### <span data-ttu-id="397c0-114">-Certificate-Nr</span><span class="sxs-lookup"><span data-stu-id="397c0-114">-CertificateId</span></span>
<span data-ttu-id="397c0-115">Gibt die ID des zu erstellenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="397c0-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="397c0-116">Wenn Sie diesen Parameter nicht angeben, wird eine ID für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="397c0-116">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="397c0-117">-Context</span><span class="sxs-lookup"><span data-stu-id="397c0-117">-Context</span></span>
<span data-ttu-id="397c0-118">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="397c0-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="397c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="397c0-119">-DefaultProfile</span></span>
<span data-ttu-id="397c0-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="397c0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="397c0-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="397c0-121">-PfxBytes</span></span>
<span data-ttu-id="397c0-122">Gibt ein Bytearray der Zertifikatsdatei im PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="397c0-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="397c0-123">Dieser Parameter ist erforderlich, wenn Sie den *PfxFilePath* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="397c0-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="397c0-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="397c0-124">-PfxFilePath</span></span>
<span data-ttu-id="397c0-125">Gibt den Pfad zur Zertifikatsdatei im PFX-Format zum Erstellen und Hochladen an.</span><span class="sxs-lookup"><span data-stu-id="397c0-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="397c0-126">Dieser Parameter ist erforderlich, wenn Sie den *PfxBytes* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="397c0-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: LoadFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="397c0-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="397c0-127">-PfxPassword</span></span>
<span data-ttu-id="397c0-128">Gibt das Kennwort für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="397c0-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="397c0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="397c0-129">CommonParameters</span></span>
<span data-ttu-id="397c0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="397c0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="397c0-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="397c0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="397c0-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="397c0-132">INPUTS</span></span>

### <span data-ttu-id="397c0-133">Keine</span><span class="sxs-lookup"><span data-stu-id="397c0-133">None</span></span>
<span data-ttu-id="397c0-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="397c0-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="397c0-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="397c0-135">OUTPUTS</span></span>

### <span data-ttu-id="397c0-136">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="397c0-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="397c0-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="397c0-137">NOTES</span></span>

## <span data-ttu-id="397c0-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="397c0-138">RELATED LINKS</span></span>

[<span data-ttu-id="397c0-139">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="397c0-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="397c0-140">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="397c0-140">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="397c0-141">Satz-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="397c0-141">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


