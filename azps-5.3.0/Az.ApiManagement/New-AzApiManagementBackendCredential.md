---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 069bf57b62d6834a1509adb551d15ce5082b2dc3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471425"
---
# <span data-ttu-id="0e23e-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0e23e-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="0e23e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e23e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e23e-103">Erstellt einen neuen Vertrag für Back-End-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="0e23e-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="0e23e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e23e-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e23e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e23e-105">DESCRIPTION</span></span>
<span data-ttu-id="0e23e-106">Erstellt einen neuen Vertrag für Back-End-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="0e23e-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="0e23e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0e23e-107">EXAMPLES</span></span>

### <span data-ttu-id="0e23e-108">Beispiel 1: Erstellen eines Back-End-In-Memory Objekts</span><span class="sxs-lookup"><span data-stu-id="0e23e-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="0e23e-109">Erstellt einen Vertrag für Back-End-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="0e23e-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="0e23e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e23e-110">PARAMETERS</span></span>

### <span data-ttu-id="0e23e-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="0e23e-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="0e23e-112">Autorisierungsheader, der für das Back-End verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e23e-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="0e23e-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0e23e-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e23e-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="0e23e-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="0e23e-115">Autorisierungsschema, das für das Backend verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e23e-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="0e23e-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0e23e-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e23e-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="0e23e-117">-CertificateThumbprint</span></span>
<span data-ttu-id="0e23e-118">Clientzertifikatdrückdrucke.</span><span class="sxs-lookup"><span data-stu-id="0e23e-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="0e23e-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0e23e-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e23e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e23e-120">-DefaultProfile</span></span>
<span data-ttu-id="0e23e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e23e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e23e-122">-Header</span><span class="sxs-lookup"><span data-stu-id="0e23e-122">-Header</span></span>
<span data-ttu-id="0e23e-123">Headerparameterwerte, die vom Back-End akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="0e23e-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="0e23e-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0e23e-124">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e23e-125">-Query</span><span class="sxs-lookup"><span data-stu-id="0e23e-125">-Query</span></span>
<span data-ttu-id="0e23e-126">Vom Back-End akzeptierte Abfrageparameterwerte.</span><span class="sxs-lookup"><span data-stu-id="0e23e-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="0e23e-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0e23e-127">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e23e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e23e-128">CommonParameters</span></span>
<span data-ttu-id="0e23e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e23e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e23e-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e23e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e23e-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0e23e-131">INPUTS</span></span>

### <span data-ttu-id="0e23e-132">Keine</span><span class="sxs-lookup"><span data-stu-id="0e23e-132">None</span></span>

## <span data-ttu-id="0e23e-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0e23e-133">OUTPUTS</span></span>

### <span data-ttu-id="0e23e-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0e23e-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="0e23e-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0e23e-135">NOTES</span></span>

## <span data-ttu-id="0e23e-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0e23e-136">RELATED LINKS</span></span>

[<span data-ttu-id="0e23e-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0e23e-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="0e23e-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0e23e-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="0e23e-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0e23e-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="0e23e-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0e23e-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="0e23e-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0e23e-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
