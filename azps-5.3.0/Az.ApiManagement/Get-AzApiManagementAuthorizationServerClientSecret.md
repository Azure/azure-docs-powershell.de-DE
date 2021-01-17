---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471502"
---
# <span data-ttu-id="c05bd-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="c05bd-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="c05bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c05bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c05bd-103">Ruft einen geheimen Serverclient für die API-Verwaltungsautorisierung ab.</span><span class="sxs-lookup"><span data-stu-id="c05bd-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="c05bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c05bd-104">SYNTAX</span></span>

### <span data-ttu-id="c05bd-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c05bd-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c05bd-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c05bd-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c05bd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c05bd-107">DESCRIPTION</span></span>
<span data-ttu-id="c05bd-108">Das **Cmdlet "Get-AzApiManagementAuthorizationServerClientSecret"** ruft den geheimen Clientgeheimnis des Azure API Management Authorization Servers ab.</span><span class="sxs-lookup"><span data-stu-id="c05bd-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="c05bd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c05bd-109">EXAMPLES</span></span>

### <span data-ttu-id="c05bd-110">Beispiel 1: Einen angegebenen Autorisierungsserverclient geheim nach ID erhalten</span><span class="sxs-lookup"><span data-stu-id="c05bd-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="c05bd-111">Dieser Befehl ruft den angegebenen geheimen Schlüssel des Autorisierungsservers ab.</span><span class="sxs-lookup"><span data-stu-id="c05bd-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="c05bd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c05bd-112">PARAMETERS</span></span>

### <span data-ttu-id="c05bd-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c05bd-113">-Context</span></span>
<span data-ttu-id="c05bd-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c05bd-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c05bd-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c05bd-115">This parameter is required.</span></span>

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

### <span data-ttu-id="c05bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05bd-116">-DefaultProfile</span></span>
<span data-ttu-id="c05bd-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c05bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c05bd-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c05bd-118">-ResourceId</span></span>
<span data-ttu-id="c05bd-119">Arm Resource Identifier des Autorisierungsservers.</span><span class="sxs-lookup"><span data-stu-id="c05bd-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="c05bd-120">Wenn angegeben, wird versucht, den Autorisierungsserver nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="c05bd-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="c05bd-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c05bd-121">This parameter is required.</span></span>

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

### <span data-ttu-id="c05bd-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="c05bd-122">-ServerId</span></span>
<span data-ttu-id="c05bd-123">Id des Autorisierungsservers.</span><span class="sxs-lookup"><span data-stu-id="c05bd-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="c05bd-124">Wenn angegeben, wird der Autorisierungsserver nach dem Bezeichner suchen.</span><span class="sxs-lookup"><span data-stu-id="c05bd-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="c05bd-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c05bd-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="c05bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05bd-126">CommonParameters</span></span>
<span data-ttu-id="c05bd-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c05bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05bd-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c05bd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05bd-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c05bd-129">INPUTS</span></span>

### <span data-ttu-id="c05bd-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c05bd-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c05bd-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c05bd-131">System.String</span></span>

## <span data-ttu-id="c05bd-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c05bd-132">OUTPUTS</span></span>

### <span data-ttu-id="c05bd-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="c05bd-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="c05bd-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c05bd-134">NOTES</span></span>

## <span data-ttu-id="c05bd-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c05bd-135">RELATED LINKS</span></span>
