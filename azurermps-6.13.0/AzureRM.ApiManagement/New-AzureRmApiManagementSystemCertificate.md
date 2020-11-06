---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476382"
---
# <span data-ttu-id="17605-101">New-AzureRmApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="17605-101">New-AzureRmApiManagementSystemCertificate</span></span>

## <span data-ttu-id="17605-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17605-102">SYNOPSIS</span></span>
<span data-ttu-id="17605-103">Erstellt eine Instanz von `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="17605-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="17605-104">Das Zertifikat kann von der privaten Zertifizierungsstelle ausgestellt werden und wird im API-Verwaltungsdienst in `CertificateAuthority` oder `Root` Store installiert.</span><span class="sxs-lookup"><span data-stu-id="17605-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17605-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17605-105">SYNTAX</span></span>

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17605-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17605-106">DESCRIPTION</span></span>
<span data-ttu-id="17605-107">Das Cmdlet **New-AzureRmApiManagementSystemCertificate** ist ein Hilfsbefehl, mit dem eine Instanz von **PsApiManagementSystemCertificate** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="17605-107">The **New-AzureRmApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="17605-108">Dieser Befehl wird mit dem Cmdlet New-AzureRmApiManagement und Set-AzureRmApiManagement verwendet.</span><span class="sxs-lookup"><span data-stu-id="17605-108">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="17605-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17605-109">EXAMPLES</span></span>

### <span data-ttu-id="17605-110">Beispiel 1: Erstellen und Initialisieren einer Instanz von PsApiManagementSystemCertificate mit einem SSL-Zertifikat aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="17605-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="17605-111">Mit diesem Befehl wird eine Instanz von **PsApiManagementSystemCertificate** mit einem Stammzertifizierungsstellenzertifikat erstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="17605-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="17605-112">Anschließend erstellt und API-Verwaltungsdienst, der das Zertifizierungsstellen-Zertifikat im Stammspeicher installiert.</span><span class="sxs-lookup"><span data-stu-id="17605-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="17605-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="17605-113">PARAMETERS</span></span>

### <span data-ttu-id="17605-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17605-114">-DefaultProfile</span></span>
<span data-ttu-id="17605-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17605-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17605-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="17605-116">-PfxPassword</span></span>
<span data-ttu-id="17605-117">Kennwort für die PFX-Zertifikatsdatei.</span><span class="sxs-lookup"><span data-stu-id="17605-117">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17605-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="17605-118">-PfxPath</span></span>
<span data-ttu-id="17605-119">Pfad zu einer PFX-Zertifikatsdatei</span><span class="sxs-lookup"><span data-stu-id="17605-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="17605-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="17605-120">-StoreName</span></span>
<span data-ttu-id="17605-121">Zertifikat StoreName</span><span class="sxs-lookup"><span data-stu-id="17605-121">Certificate StoreName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17605-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17605-122">CommonParameters</span></span>
<span data-ttu-id="17605-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17605-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17605-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17605-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17605-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17605-125">INPUTS</span></span>

### <span data-ttu-id="17605-126">System. String</span><span class="sxs-lookup"><span data-stu-id="17605-126">System.String</span></span>

### <span data-ttu-id="17605-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="17605-127">System.Security.SecureString</span></span>

## <span data-ttu-id="17605-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17605-128">OUTPUTS</span></span>

### <span data-ttu-id="17605-129">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="17605-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="17605-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="17605-130">NOTES</span></span>

## <span data-ttu-id="17605-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17605-131">RELATED LINKS</span></span>

[<span data-ttu-id="17605-132">Neu – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="17605-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="17605-133">Satz-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="17605-133">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
