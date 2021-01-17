---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471500"
---
# <span data-ttu-id="e3d27-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3d27-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="e3d27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3d27-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d27-103">Erfahren Sie mehr über das Back-End.</span><span class="sxs-lookup"><span data-stu-id="e3d27-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="e3d27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3d27-104">SYNTAX</span></span>

### <span data-ttu-id="e3d27-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3d27-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3d27-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3d27-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3d27-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3d27-107">DESCRIPTION</span></span>
<span data-ttu-id="e3d27-108">Erfahren Sie mehr über das Back-End.</span><span class="sxs-lookup"><span data-stu-id="e3d27-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="e3d27-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3d27-109">EXAMPLES</span></span>

### <span data-ttu-id="e3d27-110">Beispiel 1: Alle Backends erhalten</span><span class="sxs-lookup"><span data-stu-id="e3d27-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="e3d27-111">Ruft eine Liste aller im Api-Verwaltungsdienst konfigurierten Back-End-Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="e3d27-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="e3d27-112">Beispiel 2: So erhalten Sie das Back-End, das durch den Bezeichner 123 angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e3d27-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="e3d27-113">Details zum angegebenen Back-End erhalten, das durch den Bezeichner '123' identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="e3d27-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="e3d27-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3d27-114">PARAMETERS</span></span>

### <span data-ttu-id="e3d27-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="e3d27-115">-BackendId</span></span>
<span data-ttu-id="e3d27-116">Bezeichner eines Backends.</span><span class="sxs-lookup"><span data-stu-id="e3d27-116">Identifier of a backend.</span></span>
<span data-ttu-id="e3d27-117">Bei Angabe wird versucht, das Backend nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="e3d27-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="e3d27-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e3d27-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="e3d27-119">-Context</span><span class="sxs-lookup"><span data-stu-id="e3d27-119">-Context</span></span>
<span data-ttu-id="e3d27-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e3d27-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e3d27-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3d27-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e3d27-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d27-122">-DefaultProfile</span></span>
<span data-ttu-id="e3d27-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3d27-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3d27-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3d27-124">-ResourceId</span></span>
<span data-ttu-id="e3d27-125">Arm Resource Identifier des Backends.</span><span class="sxs-lookup"><span data-stu-id="e3d27-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="e3d27-126">Bei Angabe wird versucht, das Backend nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="e3d27-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="e3d27-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e3d27-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e3d27-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d27-128">CommonParameters</span></span>
<span data-ttu-id="e3d27-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d27-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d27-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3d27-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d27-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3d27-131">INPUTS</span></span>

### <span data-ttu-id="e3d27-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e3d27-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e3d27-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e3d27-133">System.String</span></span>

## <span data-ttu-id="e3d27-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3d27-134">OUTPUTS</span></span>

### <span data-ttu-id="e3d27-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3d27-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="e3d27-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e3d27-136">NOTES</span></span>

## <span data-ttu-id="e3d27-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e3d27-137">RELATED LINKS</span></span>

[<span data-ttu-id="e3d27-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3d27-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e3d27-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e3d27-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="e3d27-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e3d27-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e3d27-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3d27-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="e3d27-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e3d27-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
