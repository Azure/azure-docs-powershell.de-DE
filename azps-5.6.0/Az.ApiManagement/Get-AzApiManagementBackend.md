---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: ea9975038f1c738461f8c3bbda4cba70bafe8ad9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920867"
---
# <span data-ttu-id="9f35f-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9f35f-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="9f35f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f35f-102">SYNOPSIS</span></span>
<span data-ttu-id="9f35f-103">Hier erhalten Sie die Details des Backends.</span><span class="sxs-lookup"><span data-stu-id="9f35f-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="9f35f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f35f-104">SYNTAX</span></span>

### <span data-ttu-id="9f35f-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9f35f-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f35f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f35f-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f35f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f35f-107">DESCRIPTION</span></span>
<span data-ttu-id="9f35f-108">Hier erhalten Sie die Details des Backends.</span><span class="sxs-lookup"><span data-stu-id="9f35f-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="9f35f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f35f-109">EXAMPLES</span></span>

### <span data-ttu-id="9f35f-110">Beispiel 1: Alle Back-Ends erhalten</span><span class="sxs-lookup"><span data-stu-id="9f35f-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="9f35f-111">Ruft eine Liste aller im Api-Verwaltungsdienst konfigurierten Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="9f35f-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="9f35f-112">Beispiel 2: Das vom Bezeichner 123 angegebene Back-End</span><span class="sxs-lookup"><span data-stu-id="9f35f-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="9f35f-113">Erhalten Sie die Details des angegebenen Back-Ends, das durch den Bezeichner "123" identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="9f35f-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="9f35f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f35f-114">PARAMETERS</span></span>

### <span data-ttu-id="9f35f-115">-Back-EndId</span><span class="sxs-lookup"><span data-stu-id="9f35f-115">-BackendId</span></span>
<span data-ttu-id="9f35f-116">Bezeichner eines Back-End-Ends</span><span class="sxs-lookup"><span data-stu-id="9f35f-116">Identifier of a backend.</span></span>
<span data-ttu-id="9f35f-117">Wenn angegeben, wird versucht, das Back-End vom Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="9f35f-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="9f35f-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="9f35f-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f35f-119">-Context</span><span class="sxs-lookup"><span data-stu-id="9f35f-119">-Context</span></span>
<span data-ttu-id="9f35f-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9f35f-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9f35f-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9f35f-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f35f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f35f-122">-DefaultProfile</span></span>
<span data-ttu-id="9f35f-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f35f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f35f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f35f-124">-ResourceId</span></span>
<span data-ttu-id="9f35f-125">Arm Resource Identifier des Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="9f35f-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="9f35f-126">Wenn angegeben, wird versucht, das Back-End vom Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="9f35f-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="9f35f-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9f35f-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f35f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f35f-128">CommonParameters</span></span>
<span data-ttu-id="9f35f-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f35f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f35f-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f35f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f35f-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f35f-131">INPUTS</span></span>

### <span data-ttu-id="9f35f-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9f35f-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9f35f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9f35f-133">System.String</span></span>

## <span data-ttu-id="9f35f-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f35f-134">OUTPUTS</span></span>

### <span data-ttu-id="9f35f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9f35f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="9f35f-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9f35f-136">NOTES</span></span>

## <span data-ttu-id="9f35f-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9f35f-137">RELATED LINKS</span></span>

[<span data-ttu-id="9f35f-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9f35f-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="9f35f-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="9f35f-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="9f35f-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="9f35f-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="9f35f-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9f35f-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="9f35f-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9f35f-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
