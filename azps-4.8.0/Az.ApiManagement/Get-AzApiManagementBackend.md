---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009465"
---
# <span data-ttu-id="44b99-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="44b99-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="44b99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44b99-102">SYNOPSIS</span></span>
<span data-ttu-id="44b99-103">Rufen Sie die Details des Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="44b99-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="44b99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44b99-104">SYNTAX</span></span>

### <span data-ttu-id="44b99-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="44b99-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b99-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44b99-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44b99-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44b99-107">DESCRIPTION</span></span>
<span data-ttu-id="44b99-108">Rufen Sie die Details des Back-Ends ab.</span><span class="sxs-lookup"><span data-stu-id="44b99-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="44b99-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44b99-109">EXAMPLES</span></span>

### <span data-ttu-id="44b99-110">Beispiel 1: Abrufen aller backends</span><span class="sxs-lookup"><span data-stu-id="44b99-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="44b99-111">Ruft eine Liste aller Backends ab, die im API-Verwaltungsdienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="44b99-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="44b99-112">Beispiel 2: Abrufen des vom Bezeichner 123 angegebenen Back-Ends</span><span class="sxs-lookup"><span data-stu-id="44b99-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="44b99-113">Abrufen der Details des angegebenen Back-Ends, die durch den Bezeichner "123" identifiziert werden</span><span class="sxs-lookup"><span data-stu-id="44b99-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="44b99-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="44b99-114">PARAMETERS</span></span>

### <span data-ttu-id="44b99-115">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="44b99-115">-BackendId</span></span>
<span data-ttu-id="44b99-116">Bezeichner eines Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="44b99-116">Identifier of a backend.</span></span>
<span data-ttu-id="44b99-117">Wenn angegeben, wird versucht, das Back-End nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="44b99-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="44b99-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="44b99-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="44b99-119">-Context</span><span class="sxs-lookup"><span data-stu-id="44b99-119">-Context</span></span>
<span data-ttu-id="44b99-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="44b99-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="44b99-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="44b99-121">This parameter is required.</span></span>

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

### <span data-ttu-id="44b99-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b99-122">-DefaultProfile</span></span>
<span data-ttu-id="44b99-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44b99-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44b99-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="44b99-124">-ResourceId</span></span>
<span data-ttu-id="44b99-125">Arm-Ressourcenbezeichner des Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="44b99-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="44b99-126">Wenn angegeben, wird versucht, das Back-End nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="44b99-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="44b99-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="44b99-127">This parameter is required.</span></span>

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

### <span data-ttu-id="44b99-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b99-128">CommonParameters</span></span>
<span data-ttu-id="44b99-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44b99-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b99-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44b99-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b99-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44b99-131">INPUTS</span></span>

### <span data-ttu-id="44b99-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="44b99-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="44b99-133">System. String</span><span class="sxs-lookup"><span data-stu-id="44b99-133">System.String</span></span>

## <span data-ttu-id="44b99-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44b99-134">OUTPUTS</span></span>

### <span data-ttu-id="44b99-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="44b99-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="44b99-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="44b99-136">NOTES</span></span>

## <span data-ttu-id="44b99-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44b99-137">RELATED LINKS</span></span>

[<span data-ttu-id="44b99-138">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="44b99-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="44b99-139">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="44b99-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="44b99-140">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="44b99-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="44b99-141">Satz-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="44b99-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="44b99-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="44b99-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
