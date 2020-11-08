---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008205"
---
# <span data-ttu-id="d2ec2-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d2ec2-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="d2ec2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ec2-103">Erstellt eine Instanz von PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d2ec2-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="d2ec2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2ec2-104">SYNTAX</span></span>

### <span data-ttu-id="d2ec2-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2ec2-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2ec2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2ec2-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2ec2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2ec2-107">DESCRIPTION</span></span>
<span data-ttu-id="d2ec2-108">Das Cmdlet **New-AzApiManagementContext** erstellt eine Instanz von **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="d2ec2-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="d2ec2-109">Der Kontext wird für alle Cmdlets des API-Verwaltungsdiensts verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2ec2-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="d2ec2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2ec2-110">EXAMPLES</span></span>

### <span data-ttu-id="d2ec2-111">Beispiel 1: Erstellen einer PsApiManagementContext-Instanz</span><span class="sxs-lookup"><span data-stu-id="d2ec2-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="d2ec2-112">Dieser Befehl erstellt eine Instanz von **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="d2ec2-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="d2ec2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2ec2-113">PARAMETERS</span></span>

### <span data-ttu-id="d2ec2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ec2-114">-DefaultProfile</span></span>
<span data-ttu-id="d2ec2-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2ec2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2ec2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ec2-116">-ResourceGroupName</span></span>
<span data-ttu-id="d2ec2-117">Gibt den Namen der Ressourcengruppe an, unter der ein API-Verwaltungsdienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d2ec2-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="d2ec2-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d2ec2-118">-ResourceId</span></span>
<span data-ttu-id="d2ec2-119">Arm-Ressourcenbezeichner eines ApiManagement-Diensts.</span><span class="sxs-lookup"><span data-stu-id="d2ec2-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="d2ec2-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d2ec2-120">This parameter is required.</span></span>

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

### <span data-ttu-id="d2ec2-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d2ec2-121">-ServiceName</span></span>
<span data-ttu-id="d2ec2-122">Gibt den Namen des bereitgestellten API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="d2ec2-122">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="d2ec2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ec2-123">CommonParameters</span></span>
<span data-ttu-id="d2ec2-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ec2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ec2-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2ec2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ec2-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2ec2-126">INPUTS</span></span>

### <span data-ttu-id="d2ec2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d2ec2-127">System.String</span></span>

## <span data-ttu-id="d2ec2-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2ec2-128">OUTPUTS</span></span>

### <span data-ttu-id="d2ec2-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d2ec2-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="d2ec2-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2ec2-130">NOTES</span></span>

## <span data-ttu-id="d2ec2-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2ec2-131">RELATED LINKS</span></span>
