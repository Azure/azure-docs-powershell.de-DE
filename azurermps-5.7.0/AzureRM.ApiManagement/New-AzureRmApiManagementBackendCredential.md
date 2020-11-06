---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 4453b7fc3e13f4de2632c41cea966fdada1d84f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504637"
---
# <span data-ttu-id="75b8a-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="75b8a-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="75b8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="75b8a-103">Erstellt einen neuen Back-End-Anmelde Informations Vertrag.</span><span class="sxs-lookup"><span data-stu-id="75b8a-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75b8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75b8a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75b8a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75b8a-105">DESCRIPTION</span></span>
<span data-ttu-id="75b8a-106">Erstellt einen neuen Back-End-Anmelde Informations Vertrag.</span><span class="sxs-lookup"><span data-stu-id="75b8a-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="75b8a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75b8a-107">EXAMPLES</span></span>

### <span data-ttu-id="75b8a-108">Erstellen einer Back-End-Anmeldeinformationen In-Memory Objekt</span><span class="sxs-lookup"><span data-stu-id="75b8a-108">Create a Backend Credentials In-Memory Object</span></span>
```
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="75b8a-109">Erstellt einen Back-End-Anmelde Informations Vertrag</span><span class="sxs-lookup"><span data-stu-id="75b8a-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="75b8a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="75b8a-110">PARAMETERS</span></span>

### <span data-ttu-id="75b8a-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="75b8a-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="75b8a-112">Für das Back-End verwendeter Autorisierungs Header.</span><span class="sxs-lookup"><span data-stu-id="75b8a-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="75b8a-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75b8a-113">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b8a-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="75b8a-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="75b8a-115">Das für das Back-End verwendete Autorisierungsschema.</span><span class="sxs-lookup"><span data-stu-id="75b8a-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="75b8a-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75b8a-116">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b8a-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="75b8a-117">-CertificateThumbprint</span></span>
<span data-ttu-id="75b8a-118">Fingerabdrücke des Client Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="75b8a-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="75b8a-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75b8a-119">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b8a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b8a-120">-DefaultProfile</span></span>
<span data-ttu-id="75b8a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75b8a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="75b8a-122">-Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="75b8a-122">-Header</span></span>
<span data-ttu-id="75b8a-123">Vom Back-End akzeptierte Header Parameter Werte.</span><span class="sxs-lookup"><span data-stu-id="75b8a-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="75b8a-124">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75b8a-124">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b8a-125">-Query</span><span class="sxs-lookup"><span data-stu-id="75b8a-125">-Query</span></span>
<span data-ttu-id="75b8a-126">Vom Back-End akzeptierte Abfrage Parameter Werte.</span><span class="sxs-lookup"><span data-stu-id="75b8a-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="75b8a-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="75b8a-127">This parameter is optional.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b8a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b8a-128">CommonParameters</span></span>
<span data-ttu-id="75b8a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b8a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b8a-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b8a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b8a-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75b8a-131">INPUTS</span></span>

### <span data-ttu-id="75b8a-132">Keine</span><span class="sxs-lookup"><span data-stu-id="75b8a-132">None</span></span>
<span data-ttu-id="75b8a-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="75b8a-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75b8a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75b8a-134">OUTPUTS</span></span>

### <span data-ttu-id="75b8a-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="75b8a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="75b8a-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="75b8a-136">NOTES</span></span>

## <span data-ttu-id="75b8a-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75b8a-137">RELATED LINKS</span></span>

[<span data-ttu-id="75b8a-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="75b8a-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="75b8a-139">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="75b8a-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="75b8a-140">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="75b8a-140">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="75b8a-141">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="75b8a-141">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="75b8a-142">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="75b8a-142">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
