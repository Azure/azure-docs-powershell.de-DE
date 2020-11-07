---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 88a48edf3ae7e576aa78e989a5fda7515499a7f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650389"
---
# <span data-ttu-id="cb426-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cb426-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="cb426-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb426-102">SYNOPSIS</span></span>
<span data-ttu-id="cb426-103">Rufen Sie die Details des Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="cb426-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="cb426-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb426-104">SYNTAX</span></span>

### <span data-ttu-id="cb426-105">GetAllBackends (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb426-105">GetAllBackends (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb426-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="cb426-106">GetByBackendId</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb426-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb426-107">DESCRIPTION</span></span>
<span data-ttu-id="cb426-108">Rufen Sie die Details des Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="cb426-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="cb426-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb426-109">EXAMPLES</span></span>

### <span data-ttu-id="cb426-110">Beispiel 1: Abrufen aller backends</span><span class="sxs-lookup"><span data-stu-id="cb426-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="cb426-111">Ruft eine Liste aller Backends ab, die im API-Verwaltungsdienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="cb426-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="cb426-112">Beispiel 2: Abrufen des vom Bezeichner 123 angegebenen Back-Ends</span><span class="sxs-lookup"><span data-stu-id="cb426-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="cb426-113">Abrufen der Details des angegebenen Back-Ends, die durch den Bezeichner "123" identifiziert werden</span><span class="sxs-lookup"><span data-stu-id="cb426-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="cb426-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb426-114">PARAMETERS</span></span>

### <span data-ttu-id="cb426-115">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="cb426-115">-BackendId</span></span>
<span data-ttu-id="cb426-116">Bezeichner eines Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="cb426-116">Identifier of a backend.</span></span>
<span data-ttu-id="cb426-117">Wenn angegeben, wird versucht, das Back-End nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="cb426-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="cb426-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="cb426-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="cb426-119">-Context</span><span class="sxs-lookup"><span data-stu-id="cb426-119">-Context</span></span>
<span data-ttu-id="cb426-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cb426-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cb426-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb426-121">This parameter is required.</span></span>

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

### <span data-ttu-id="cb426-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb426-122">-DefaultProfile</span></span>
<span data-ttu-id="cb426-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb426-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb426-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb426-124">CommonParameters</span></span>
<span data-ttu-id="cb426-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb426-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb426-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb426-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb426-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb426-127">INPUTS</span></span>

### <span data-ttu-id="cb426-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cb426-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cb426-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cb426-129">System.String</span></span>

## <span data-ttu-id="cb426-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb426-130">OUTPUTS</span></span>

### <span data-ttu-id="cb426-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cb426-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="cb426-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb426-132">NOTES</span></span>

## <span data-ttu-id="cb426-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb426-133">RELATED LINKS</span></span>

[<span data-ttu-id="cb426-134">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cb426-134">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="cb426-135">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="cb426-135">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="cb426-136">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="cb426-136">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="cb426-137">Satz-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cb426-137">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="cb426-138">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="cb426-138">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
