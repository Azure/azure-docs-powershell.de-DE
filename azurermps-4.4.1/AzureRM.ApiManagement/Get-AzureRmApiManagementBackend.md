---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499289"
---
# <span data-ttu-id="a9f2b-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a9f2b-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="a9f2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f2b-103">Rufen Sie die Details des Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="a9f2b-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9f2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9f2b-104">SYNTAX</span></span>

### <span data-ttu-id="a9f2b-105">Abrufen aller backends (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9f2b-105">Get all backends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9f2b-106">Abrufen nach Back-End-ID</span><span class="sxs-lookup"><span data-stu-id="a9f2b-106">Get by backend ID</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f2b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9f2b-107">DESCRIPTION</span></span>
<span data-ttu-id="a9f2b-108">Rufen Sie die Details des Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="a9f2b-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="a9f2b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9f2b-109">EXAMPLES</span></span>

### <span data-ttu-id="a9f2b-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a9f2b-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="a9f2b-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a9f2b-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="a9f2b-112">Ruft eine Liste aller Backends ab, die im API-Verwaltungsdienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="a9f2b-112">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="a9f2b-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a9f2b-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="a9f2b-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a9f2b-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="a9f2b-115">Abrufen der Details des angegebenen Back-Ends, die durch den Bezeichner "123" identifiziert werden</span><span class="sxs-lookup"><span data-stu-id="a9f2b-115">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="a9f2b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9f2b-116">PARAMETERS</span></span>

### <span data-ttu-id="a9f2b-117">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="a9f2b-117">-BackendId</span></span>
<span data-ttu-id="a9f2b-118">Bezeichner eines Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="a9f2b-118">Identifier of a backend.</span></span>
<span data-ttu-id="a9f2b-119">Wenn angegeben, wird versucht, das Back-End nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="a9f2b-119">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="a9f2b-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a9f2b-120">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9f2b-121">-Context</span><span class="sxs-lookup"><span data-stu-id="a9f2b-121">-Context</span></span>
<span data-ttu-id="a9f2b-122">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a9f2b-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a9f2b-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9f2b-123">This parameter is required.</span></span>

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

### <span data-ttu-id="a9f2b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f2b-124">-DefaultProfile</span></span>
<span data-ttu-id="a9f2b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9f2b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9f2b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f2b-126">CommonParameters</span></span>
<span data-ttu-id="a9f2b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9f2b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f2b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9f2b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f2b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9f2b-129">INPUTS</span></span>

## <span data-ttu-id="a9f2b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9f2b-130">OUTPUTS</span></span>

### <span data-ttu-id="a9f2b-131">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="a9f2b-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>

### <span data-ttu-id="a9f2b-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a9f2b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger.PsApiManagementBackend</span></span>

## <span data-ttu-id="a9f2b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9f2b-133">NOTES</span></span>

## <span data-ttu-id="a9f2b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9f2b-134">RELATED LINKS</span></span>

[<span data-ttu-id="a9f2b-135">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a9f2b-135">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a9f2b-136">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a9f2b-136">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="a9f2b-137">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a9f2b-137">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="a9f2b-138">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a9f2b-138">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a9f2b-139">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a9f2b-139">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
