---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
ms.openlocfilehash: e66e87f7169ba48498e58384aed7b0cd7c81c68d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996946"
---
# <span data-ttu-id="af567-101">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="af567-101">New-AzApiManagementCertificate</span></span>

## <span data-ttu-id="af567-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af567-102">SYNOPSIS</span></span>
<span data-ttu-id="af567-103">Erstellt ein API-Verwaltungszertifikat, das während der Authentifizierung mit Back-End verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="af567-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

## <span data-ttu-id="af567-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af567-104">SYNTAX</span></span>

### <span data-ttu-id="af567-105">Loadfromdatei (Standard)</span><span class="sxs-lookup"><span data-stu-id="af567-105">LoadFromFile (Default)</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af567-106">Unformatierte</span><span class="sxs-lookup"><span data-stu-id="af567-106">Raw</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>] -PfxBytes <Byte[]>
 -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af567-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af567-107">DESCRIPTION</span></span>
<span data-ttu-id="af567-108">Das Cmdlet **New-AzApiManagementCertificate** erstellt ein Azure API-Verwaltungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="af567-108">The **New-AzApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="af567-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af567-109">EXAMPLES</span></span>

### <span data-ttu-id="af567-110">Beispiel 1: Erstellen und Hochladen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="af567-110">Example 1: Create and upload a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="af567-111">Mit diesem Befehl wird ein Zertifikat in die API-Verwaltung hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="af567-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="af567-112">Dieses Zertifikat kann für die gegenseitige Authentifizierung mit dem Back-End mithilfe von Richtlinien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af567-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="af567-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="af567-113">PARAMETERS</span></span>

### <span data-ttu-id="af567-114">-Certificate-Nr</span><span class="sxs-lookup"><span data-stu-id="af567-114">-CertificateId</span></span>
<span data-ttu-id="af567-115">Gibt die ID des zu erstellenden Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="af567-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="af567-116">Wenn Sie diesen Parameter nicht angeben, wird eine ID für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="af567-116">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="af567-117">-Context</span><span class="sxs-lookup"><span data-stu-id="af567-117">-Context</span></span>
<span data-ttu-id="af567-118">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="af567-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af567-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af567-119">-DefaultProfile</span></span>
<span data-ttu-id="af567-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af567-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af567-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="af567-121">-PfxBytes</span></span>
<span data-ttu-id="af567-122">Gibt ein Bytearray der Zertifikatsdatei im PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="af567-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="af567-123">Dieser Parameter ist erforderlich, wenn Sie den *PfxFilePath* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="af567-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="af567-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="af567-124">-PfxFilePath</span></span>
<span data-ttu-id="af567-125">Gibt den Pfad zur Zertifikatsdatei im PFX-Format zum Erstellen und Hochladen an.</span><span class="sxs-lookup"><span data-stu-id="af567-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="af567-126">Dieser Parameter ist erforderlich, wenn Sie den *PfxBytes* -Parameter nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="af567-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af567-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="af567-127">-PfxPassword</span></span>
<span data-ttu-id="af567-128">Gibt das Kennwort für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="af567-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="af567-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af567-129">CommonParameters</span></span>
<span data-ttu-id="af567-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af567-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af567-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af567-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af567-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af567-132">INPUTS</span></span>

### <span data-ttu-id="af567-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="af567-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="af567-134">System. String</span><span class="sxs-lookup"><span data-stu-id="af567-134">System.String</span></span>

### <span data-ttu-id="af567-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="af567-135">System.Byte[]</span></span>

## <span data-ttu-id="af567-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af567-136">OUTPUTS</span></span>

### <span data-ttu-id="af567-137">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="af567-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="af567-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="af567-138">NOTES</span></span>

## <span data-ttu-id="af567-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af567-139">RELATED LINKS</span></span>

[<span data-ttu-id="af567-140">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="af567-140">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="af567-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="af567-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="af567-142">Satz-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="af567-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


