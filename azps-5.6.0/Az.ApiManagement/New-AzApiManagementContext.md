---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: b7124b00452637ca3e496a0417745ee7719278e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931419"
---
# <span data-ttu-id="670f4-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="670f4-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="670f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="670f4-102">SYNOPSIS</span></span>
<span data-ttu-id="670f4-103">Erstellt eine Instanz von PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="670f4-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="670f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="670f4-104">SYNTAX</span></span>

### <span data-ttu-id="670f4-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="670f4-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="670f4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="670f4-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="670f4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="670f4-107">DESCRIPTION</span></span>
<span data-ttu-id="670f4-108">Das **Cmdlet New-AzApiManagementContext** erstellt eine Instanz von **PsAzureApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="670f4-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="670f4-109">Der Kontext wird für alle API-Verwaltungsdienst-Cmdlets verwendet.</span><span class="sxs-lookup"><span data-stu-id="670f4-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="670f4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="670f4-110">EXAMPLES</span></span>

### <span data-ttu-id="670f4-111">Beispiel 1: Erstellen einer PsApiManagementContext-Instanz</span><span class="sxs-lookup"><span data-stu-id="670f4-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="670f4-112">Mit diesem Befehl wird eine Instanz von **PsApiManagementContext erstellt.**</span><span class="sxs-lookup"><span data-stu-id="670f4-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="670f4-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="670f4-113">PARAMETERS</span></span>

### <span data-ttu-id="670f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670f4-114">-DefaultProfile</span></span>
<span data-ttu-id="670f4-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="670f4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="670f4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670f4-116">-ResourceGroupName</span></span>
<span data-ttu-id="670f4-117">Gibt den Namen der Ressourcengruppe an, unter der ein API-Verwaltungsdienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="670f4-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="670f4-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="670f4-118">-ResourceId</span></span>
<span data-ttu-id="670f4-119">Arm Resource Identifier eines ApiManagement-Diensts.</span><span class="sxs-lookup"><span data-stu-id="670f4-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="670f4-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="670f4-120">This parameter is required.</span></span>

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

### <span data-ttu-id="670f4-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="670f4-121">-ServiceName</span></span>
<span data-ttu-id="670f4-122">Gibt den Namen des bereitgestellten API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="670f4-122">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="670f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670f4-123">CommonParameters</span></span>
<span data-ttu-id="670f4-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670f4-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="670f4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670f4-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="670f4-126">INPUTS</span></span>

### <span data-ttu-id="670f4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="670f4-127">System.String</span></span>

## <span data-ttu-id="670f4-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="670f4-128">OUTPUTS</span></span>

### <span data-ttu-id="670f4-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="670f4-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="670f4-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="670f4-130">NOTES</span></span>

## <span data-ttu-id="670f4-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="670f4-131">RELATED LINKS</span></span>
