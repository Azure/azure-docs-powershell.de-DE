---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159764"
---
# <span data-ttu-id="b2744-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b2744-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="b2744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2744-102">SYNOPSIS</span></span>
<span data-ttu-id="b2744-103">Ruft einen API-Verwaltungsautorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="b2744-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="b2744-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2744-104">SYNTAX</span></span>

### <span data-ttu-id="b2744-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2744-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2744-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2744-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2744-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2744-107">DESCRIPTION</span></span>
<span data-ttu-id="b2744-108">Das **Cmdlet "Get-AzApiManagementAuthorizationServer"** ruft alle Azure API Management Authorization Server oder angegebenen Autorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="b2744-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="b2744-109">ClientSecret wird nicht in die Ergebnisdetails eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b2744-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="b2744-110">Um den geheimen Clientgeheimnis zu erhalten, **verwenden Sie "Get-AzApiManagementAuthorizationServerClientSecret".**</span><span class="sxs-lookup"><span data-stu-id="b2744-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="b2744-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2744-111">EXAMPLES</span></span>

### <span data-ttu-id="b2744-112">Beispiel 1: Alle Autorisierungsserver erhalten</span><span class="sxs-lookup"><span data-stu-id="b2744-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="b2744-113">Dieser Befehl ruft alle API-Verwaltungsautorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="b2744-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="b2744-114">Beispiel 2: Erhalten eines angegebenen Autorisierungsservers</span><span class="sxs-lookup"><span data-stu-id="b2744-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="b2744-115">Dieser Befehl ruft den angegebenen Autorisierungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="b2744-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="b2744-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2744-116">PARAMETERS</span></span>

### <span data-ttu-id="b2744-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b2744-117">-Context</span></span>

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

### <span data-ttu-id="b2744-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2744-118">-DefaultProfile</span></span>
<span data-ttu-id="b2744-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2744-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2744-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2744-120">-ResourceId</span></span>
<span data-ttu-id="b2744-121">Arm Resource Identifier des Autorisierungsservers.</span><span class="sxs-lookup"><span data-stu-id="b2744-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="b2744-122">Bei Angabe wird versucht, den Autorisierungsserver nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="b2744-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="b2744-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b2744-123">This parameter is required.</span></span>

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

### <span data-ttu-id="b2744-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="b2744-124">-ServerId</span></span>
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

### <span data-ttu-id="b2744-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2744-125">CommonParameters</span></span>
<span data-ttu-id="b2744-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2744-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2744-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2744-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2744-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2744-128">INPUTS</span></span>

### <span data-ttu-id="b2744-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b2744-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b2744-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b2744-130">System.String</span></span>

## <span data-ttu-id="b2744-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2744-131">OUTPUTS</span></span>

### <span data-ttu-id="b2744-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b2744-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="b2744-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b2744-133">NOTES</span></span>

## <span data-ttu-id="b2744-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b2744-134">RELATED LINKS</span></span>

[<span data-ttu-id="b2744-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b2744-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="b2744-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b2744-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="b2744-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b2744-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


