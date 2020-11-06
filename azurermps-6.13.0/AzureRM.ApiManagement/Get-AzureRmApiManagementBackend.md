---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 11d832bc74aca4ac274ee17ff0b38de06b77e377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480682"
---
# <span data-ttu-id="2c900-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c900-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="2c900-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c900-102">SYNOPSIS</span></span>
<span data-ttu-id="2c900-103">Rufen Sie die Details des Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="2c900-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c900-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c900-104">SYNTAX</span></span>

### <span data-ttu-id="2c900-105">GetAllBackends (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c900-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c900-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="2c900-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c900-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c900-107">DESCRIPTION</span></span>
<span data-ttu-id="2c900-108">Rufen Sie die Details des Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="2c900-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="2c900-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c900-109">EXAMPLES</span></span>

### <span data-ttu-id="2c900-110">Beispiel 1: Abrufen aller backends</span><span class="sxs-lookup"><span data-stu-id="2c900-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="2c900-111">Ruft eine Liste aller Backends ab, die im API-Verwaltungsdienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="2c900-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="2c900-112">Beispiel 2: Abrufen des vom Bezeichner 123 angegebenen Back-Ends</span><span class="sxs-lookup"><span data-stu-id="2c900-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="2c900-113">Abrufen der Details des angegebenen Back-Ends, die durch den Bezeichner "123" identifiziert werden</span><span class="sxs-lookup"><span data-stu-id="2c900-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="2c900-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c900-114">PARAMETERS</span></span>

### <span data-ttu-id="2c900-115">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="2c900-115">-BackendId</span></span>
<span data-ttu-id="2c900-116">Bezeichner eines Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="2c900-116">Identifier of a backend.</span></span>
<span data-ttu-id="2c900-117">Wenn angegeben, wird versucht, das Back-End nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="2c900-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="2c900-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="2c900-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByBackendId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c900-119">-Context</span><span class="sxs-lookup"><span data-stu-id="2c900-119">-Context</span></span>
<span data-ttu-id="2c900-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2c900-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2c900-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2c900-121">This parameter is required.</span></span>

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

### <span data-ttu-id="2c900-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c900-122">-DefaultProfile</span></span>
<span data-ttu-id="2c900-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c900-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c900-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c900-124">CommonParameters</span></span>
<span data-ttu-id="2c900-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c900-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c900-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c900-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c900-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c900-127">INPUTS</span></span>

### <span data-ttu-id="2c900-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2c900-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2c900-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2c900-129">System.String</span></span>

## <span data-ttu-id="2c900-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c900-130">OUTPUTS</span></span>

### <span data-ttu-id="2c900-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c900-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="2c900-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c900-132">NOTES</span></span>

## <span data-ttu-id="2c900-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c900-133">RELATED LINKS</span></span>

[<span data-ttu-id="2c900-134">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c900-134">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="2c900-135">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2c900-135">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="2c900-136">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2c900-136">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="2c900-137">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c900-137">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="2c900-138">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c900-138">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
