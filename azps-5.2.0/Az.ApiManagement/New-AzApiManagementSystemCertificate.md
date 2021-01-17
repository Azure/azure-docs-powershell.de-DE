---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 657a1b729bfa5de8b62c58ed590b5cbf2cf7dca8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304651"
---
# <span data-ttu-id="80546-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="80546-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="80546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80546-102">SYNOPSIS</span></span>
<span data-ttu-id="80546-103">Erstellt eine Instanz von `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="80546-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="80546-104">Das Zertifikat kann von privaten Zertifizierungsstellen ausgestellt werden und wird im API-Verwaltungsdienst in oder in einem `CertificateAuthority` Speicher `Root` installiert.</span><span class="sxs-lookup"><span data-stu-id="80546-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="80546-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80546-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80546-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80546-106">DESCRIPTION</span></span>
<span data-ttu-id="80546-107">Das **Cmdlet "New-AzApiManagementSystemCertificate"** ist ein Hilfsbefehl, der eine Instanz von **"PsApiManagementSystemCertificate" erstellt.**</span><span class="sxs-lookup"><span data-stu-id="80546-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="80546-108">Dieser Befehl wird mit dem Cmdlet New-AzApiManagement und Set-AzApiManagement verwendet.</span><span class="sxs-lookup"><span data-stu-id="80546-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="80546-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="80546-109">EXAMPLES</span></span>

### <span data-ttu-id="80546-110">Beispiel 1: Erstellen und Initialisieren einer Instanz von PsApiManagementSystemCertificate mithilfe eines Ssl-Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="80546-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="80546-111">Mit diesem Befehl wird eine Instanz von **"PsApiManagementSystemCertificate"** mit einem Stammzertifikat der Zertifizierungsstelle erstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="80546-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="80546-112">Anschließend erstellt und erstellt er den API-Verwaltungsdienst, der das Zertifizierungsstellenzertifikat im Stammspeicher installiert.</span><span class="sxs-lookup"><span data-stu-id="80546-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="80546-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80546-113">PARAMETERS</span></span>

### <span data-ttu-id="80546-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80546-114">-DefaultProfile</span></span>
<span data-ttu-id="80546-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80546-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80546-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="80546-116">-PfxPassword</span></span>
<span data-ttu-id="80546-117">Kennwort für die PFX-Zertifikatdatei.</span><span class="sxs-lookup"><span data-stu-id="80546-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="80546-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="80546-118">-PfxPath</span></span>
<span data-ttu-id="80546-119">Pfad zu einer PFX-Zertifikatdatei.</span><span class="sxs-lookup"><span data-stu-id="80546-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="80546-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="80546-120">-StoreName</span></span>
<span data-ttu-id="80546-121">Certificate StoreName</span><span class="sxs-lookup"><span data-stu-id="80546-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="80546-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80546-122">CommonParameters</span></span>
<span data-ttu-id="80546-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80546-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80546-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80546-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80546-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="80546-125">INPUTS</span></span>

### <span data-ttu-id="80546-126">System.String</span><span class="sxs-lookup"><span data-stu-id="80546-126">System.String</span></span>

### <span data-ttu-id="80546-127">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="80546-127">System.Security.SecureString</span></span>

## <span data-ttu-id="80546-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="80546-128">OUTPUTS</span></span>

### <span data-ttu-id="80546-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="80546-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="80546-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="80546-130">NOTES</span></span>

## <span data-ttu-id="80546-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="80546-131">RELATED LINKS</span></span>

[<span data-ttu-id="80546-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="80546-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="80546-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="80546-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)