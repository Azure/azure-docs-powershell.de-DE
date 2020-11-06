---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 58f80b6ff1742bfc6360844648d6ad18d12d8389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498069"
---
# <span data-ttu-id="da014-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="da014-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="da014-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da014-102">SYNOPSIS</span></span>
<span data-ttu-id="da014-103">Erstellt einen neuen Back-End-Anmelde Informations Vertrag.</span><span class="sxs-lookup"><span data-stu-id="da014-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da014-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da014-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da014-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da014-105">DESCRIPTION</span></span>
<span data-ttu-id="da014-106">Erstellt einen neuen Back-End-Anmelde Informations Vertrag.</span><span class="sxs-lookup"><span data-stu-id="da014-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="da014-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da014-107">EXAMPLES</span></span>

### <span data-ttu-id="da014-108">Erstellen einer Back-End-Anmeldeinformationen In-Memory Objekt</span><span class="sxs-lookup"><span data-stu-id="da014-108">Create a Backend Credentials In-Memory Object</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="da014-109">Erstellt einen Back-End-Anmelde Informations Vertrag</span><span class="sxs-lookup"><span data-stu-id="da014-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="da014-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="da014-110">PARAMETERS</span></span>

### <span data-ttu-id="da014-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="da014-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="da014-112">Für das Back-End verwendeter Autorisierungs Header.</span><span class="sxs-lookup"><span data-stu-id="da014-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="da014-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="da014-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="da014-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="da014-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="da014-115">Das für das Back-End verwendete Autorisierungsschema.</span><span class="sxs-lookup"><span data-stu-id="da014-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="da014-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="da014-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="da014-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="da014-117">-CertificateThumbprint</span></span>
<span data-ttu-id="da014-118">Fingerabdrücke des Client Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="da014-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="da014-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="da014-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="da014-120">-Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="da014-120">-Header</span></span>
<span data-ttu-id="da014-121">Vom Back-End akzeptierte Header Parameter Werte.</span><span class="sxs-lookup"><span data-stu-id="da014-121">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="da014-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="da014-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="da014-123">-Query</span><span class="sxs-lookup"><span data-stu-id="da014-123">-Query</span></span>
<span data-ttu-id="da014-124">Vom Back-End akzeptierte Abfrage Parameter Werte.</span><span class="sxs-lookup"><span data-stu-id="da014-124">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="da014-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="da014-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="da014-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da014-126">-DefaultProfile</span></span>
<span data-ttu-id="da014-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da014-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da014-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da014-128">CommonParameters</span></span>
<span data-ttu-id="da014-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da014-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da014-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da014-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da014-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da014-131">INPUTS</span></span>

## <span data-ttu-id="da014-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da014-132">OUTPUTS</span></span>

### <span data-ttu-id="da014-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="da014-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="da014-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="da014-134">NOTES</span></span>

## <span data-ttu-id="da014-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da014-135">RELATED LINKS</span></span>

[<span data-ttu-id="da014-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="da014-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="da014-137">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="da014-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="da014-138">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="da014-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="da014-139">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="da014-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="da014-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="da014-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
