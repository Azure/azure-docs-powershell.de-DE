---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996645"
---
# <span data-ttu-id="1167c-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1167c-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="1167c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1167c-102">SYNOPSIS</span></span>
<span data-ttu-id="1167c-103">Rufen Sie die Details des Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="1167c-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="1167c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1167c-104">SYNTAX</span></span>

### <span data-ttu-id="1167c-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1167c-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1167c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1167c-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1167c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1167c-107">DESCRIPTION</span></span>
<span data-ttu-id="1167c-108">Rufen Sie die Details des Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="1167c-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="1167c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1167c-109">EXAMPLES</span></span>

### <span data-ttu-id="1167c-110">Beispiel 1: Abrufen aller backends</span><span class="sxs-lookup"><span data-stu-id="1167c-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="1167c-111">Ruft eine Liste aller Backends ab, die im API-Verwaltungsdienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="1167c-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="1167c-112">Beispiel 2: Abrufen des vom Bezeichner 123 angegebenen Back-Ends</span><span class="sxs-lookup"><span data-stu-id="1167c-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="1167c-113">Abrufen der Details des angegebenen Back-Ends, die durch den Bezeichner "123" identifiziert werden</span><span class="sxs-lookup"><span data-stu-id="1167c-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="1167c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1167c-114">PARAMETERS</span></span>

### <span data-ttu-id="1167c-115">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="1167c-115">-BackendId</span></span>
<span data-ttu-id="1167c-116">Bezeichner eines Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="1167c-116">Identifier of a backend.</span></span>
<span data-ttu-id="1167c-117">Wenn angegeben, wird versucht, das Back-End nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="1167c-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="1167c-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1167c-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="1167c-119">-Context</span><span class="sxs-lookup"><span data-stu-id="1167c-119">-Context</span></span>
<span data-ttu-id="1167c-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1167c-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1167c-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1167c-121">This parameter is required.</span></span>

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

### <span data-ttu-id="1167c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1167c-122">-DefaultProfile</span></span>
<span data-ttu-id="1167c-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1167c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1167c-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1167c-124">-ResourceId</span></span>
<span data-ttu-id="1167c-125">Arm-Ressourcenbezeichner des Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="1167c-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="1167c-126">Wenn angegeben, wird versucht, das Back-End nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="1167c-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="1167c-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1167c-127">This parameter is required.</span></span>

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

### <span data-ttu-id="1167c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1167c-128">CommonParameters</span></span>
<span data-ttu-id="1167c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1167c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1167c-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1167c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1167c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1167c-131">INPUTS</span></span>

### <span data-ttu-id="1167c-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1167c-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1167c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1167c-133">System.String</span></span>

## <span data-ttu-id="1167c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1167c-134">OUTPUTS</span></span>

### <span data-ttu-id="1167c-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1167c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="1167c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="1167c-136">NOTES</span></span>

## <span data-ttu-id="1167c-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1167c-137">RELATED LINKS</span></span>

[<span data-ttu-id="1167c-138">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1167c-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="1167c-139">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1167c-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="1167c-140">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1167c-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="1167c-141">Satz-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1167c-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="1167c-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1167c-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
