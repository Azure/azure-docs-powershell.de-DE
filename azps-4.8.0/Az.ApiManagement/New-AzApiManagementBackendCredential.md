---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 069bf57b62d6834a1509adb551d15ce5082b2dc3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010098"
---
# <span data-ttu-id="3dac9-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="3dac9-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="3dac9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3dac9-102">SYNOPSIS</span></span>
<span data-ttu-id="3dac9-103">Erstellt einen neuen Back-End-Anmelde Informations Vertrag.</span><span class="sxs-lookup"><span data-stu-id="3dac9-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="3dac9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dac9-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dac9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3dac9-105">DESCRIPTION</span></span>
<span data-ttu-id="3dac9-106">Erstellt einen neuen Back-End-Anmelde Informations Vertrag.</span><span class="sxs-lookup"><span data-stu-id="3dac9-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="3dac9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3dac9-107">EXAMPLES</span></span>

### <span data-ttu-id="3dac9-108">Beispiel 1: Erstellen einer Back-End-Anmeldeinformationen In-Memory Objekt</span><span class="sxs-lookup"><span data-stu-id="3dac9-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="3dac9-109">Erstellt einen Back-End-Anmelde Informations Vertrag</span><span class="sxs-lookup"><span data-stu-id="3dac9-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="3dac9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dac9-110">PARAMETERS</span></span>

### <span data-ttu-id="3dac9-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="3dac9-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="3dac9-112">Für das Back-End verwendeter Autorisierungs Header.</span><span class="sxs-lookup"><span data-stu-id="3dac9-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="3dac9-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3dac9-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="3dac9-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="3dac9-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="3dac9-115">Das für das Back-End verwendete Autorisierungsschema.</span><span class="sxs-lookup"><span data-stu-id="3dac9-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="3dac9-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3dac9-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="3dac9-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="3dac9-117">-CertificateThumbprint</span></span>
<span data-ttu-id="3dac9-118">Fingerabdrücke des Client Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="3dac9-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="3dac9-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3dac9-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="3dac9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dac9-120">-DefaultProfile</span></span>
<span data-ttu-id="3dac9-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3dac9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dac9-122">-Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="3dac9-122">-Header</span></span>
<span data-ttu-id="3dac9-123">Vom Back-End akzeptierte Header Parameter Werte.</span><span class="sxs-lookup"><span data-stu-id="3dac9-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="3dac9-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3dac9-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="3dac9-125">-Query</span><span class="sxs-lookup"><span data-stu-id="3dac9-125">-Query</span></span>
<span data-ttu-id="3dac9-126">Vom Back-End akzeptierte Abfrage Parameter Werte.</span><span class="sxs-lookup"><span data-stu-id="3dac9-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="3dac9-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3dac9-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="3dac9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dac9-128">CommonParameters</span></span>
<span data-ttu-id="3dac9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dac9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dac9-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dac9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dac9-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3dac9-131">INPUTS</span></span>

### <span data-ttu-id="3dac9-132">Keine</span><span class="sxs-lookup"><span data-stu-id="3dac9-132">None</span></span>

## <span data-ttu-id="3dac9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3dac9-133">OUTPUTS</span></span>

### <span data-ttu-id="3dac9-134">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="3dac9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="3dac9-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="3dac9-135">NOTES</span></span>

## <span data-ttu-id="3dac9-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3dac9-136">RELATED LINKS</span></span>

[<span data-ttu-id="3dac9-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3dac9-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="3dac9-138">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3dac9-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="3dac9-139">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="3dac9-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="3dac9-140">Satz-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3dac9-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="3dac9-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3dac9-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
