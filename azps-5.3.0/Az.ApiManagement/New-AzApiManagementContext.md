---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471414"
---
# <span data-ttu-id="a049c-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a049c-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="a049c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a049c-102">SYNOPSIS</span></span>
<span data-ttu-id="a049c-103">Erstellt eine Instanz von "PsAzureApiManagementContext".</span><span class="sxs-lookup"><span data-stu-id="a049c-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="a049c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a049c-104">SYNTAX</span></span>

### <span data-ttu-id="a049c-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a049c-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a049c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a049c-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a049c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a049c-107">DESCRIPTION</span></span>
<span data-ttu-id="a049c-108">Das **Cmdlet "New-AzApiManagementContext"** erstellt eine Instanz von **PsAzureApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="a049c-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="a049c-109">Der Kontext wird für alle API-Verwaltungsdienst-Cmdlets verwendet.</span><span class="sxs-lookup"><span data-stu-id="a049c-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="a049c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a049c-110">EXAMPLES</span></span>

### <span data-ttu-id="a049c-111">Beispiel 1: Erstellen einer Instanz "PsApiManagementContext"</span><span class="sxs-lookup"><span data-stu-id="a049c-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="a049c-112">Mit diesem Befehl wird eine Instanz von **"PsApiManagementContext" erstellt.**</span><span class="sxs-lookup"><span data-stu-id="a049c-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="a049c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a049c-113">PARAMETERS</span></span>

### <span data-ttu-id="a049c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a049c-114">-DefaultProfile</span></span>
<span data-ttu-id="a049c-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a049c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a049c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a049c-116">-ResourceGroupName</span></span>
<span data-ttu-id="a049c-117">Gibt den Namen der Ressourcengruppe an, unter der ein API-Verwaltungsdienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a049c-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a049c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a049c-118">-ResourceId</span></span>
<span data-ttu-id="a049c-119">Arm Resource Identifier eines ApiManagement-Diensts.</span><span class="sxs-lookup"><span data-stu-id="a049c-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="a049c-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a049c-120">This parameter is required.</span></span>

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

### <span data-ttu-id="a049c-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a049c-121">-ServiceName</span></span>
<span data-ttu-id="a049c-122">Gibt den Namen des bereitgestellten API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="a049c-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a049c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a049c-123">CommonParameters</span></span>
<span data-ttu-id="a049c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a049c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a049c-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a049c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a049c-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a049c-126">INPUTS</span></span>

### <span data-ttu-id="a049c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a049c-127">System.String</span></span>

## <span data-ttu-id="a049c-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a049c-128">OUTPUTS</span></span>

### <span data-ttu-id="a049c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a049c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="a049c-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a049c-130">NOTES</span></span>

## <span data-ttu-id="a049c-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a049c-131">RELATED LINKS</span></span>
