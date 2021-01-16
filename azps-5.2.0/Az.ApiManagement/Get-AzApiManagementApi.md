---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297872"
---
# <span data-ttu-id="1c047-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1c047-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="1c047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c047-102">SYNOPSIS</span></span>
<span data-ttu-id="1c047-103">Ruft eine API ab.</span><span class="sxs-lookup"><span data-stu-id="1c047-103">Gets an API.</span></span>

## <span data-ttu-id="1c047-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c047-104">SYNTAX</span></span>

### <span data-ttu-id="1c047-105">GetAllApis (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c047-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c047-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="1c047-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c047-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="1c047-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c047-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="1c047-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c047-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="1c047-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c047-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c047-110">DESCRIPTION</span></span>
<span data-ttu-id="1c047-111">Das **Cmdlet "Get-AzApiManagementApi"** ruft mindestens eine Azure API -Verwaltungs-APIs ab.</span><span class="sxs-lookup"><span data-stu-id="1c047-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="1c047-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1c047-112">EXAMPLES</span></span>

### <span data-ttu-id="1c047-113">Beispiel 1: Alle Verwaltungs-APIs erhalten</span><span class="sxs-lookup"><span data-stu-id="1c047-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="1c047-114">Dieser Befehl ruft alle APIs für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="1c047-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="1c047-115">Beispiel 2: Abrufen einer Verwaltungs-API nach ID</span><span class="sxs-lookup"><span data-stu-id="1c047-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="1c047-116">Dieser Befehl ruft die API mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="1c047-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="1c047-117">Beispiel 3: Abrufen einer Verwaltungs-API nach Name</span><span class="sxs-lookup"><span data-stu-id="1c047-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="1c047-118">Dieser Befehl ruft die API mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="1c047-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="1c047-119">Beispiel 4: Abrufen einer Verwaltungs-API von GatewayId</span><span class="sxs-lookup"><span data-stu-id="1c047-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="1c047-120">Dieser Befehl ruft die API für die angegebene Gateway-ID ab.</span><span class="sxs-lookup"><span data-stu-id="1c047-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="1c047-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c047-121">PARAMETERS</span></span>

### <span data-ttu-id="1c047-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1c047-122">-ApiId</span></span>
<span data-ttu-id="1c047-123">Gibt die ID der zu abrufenden API an.</span><span class="sxs-lookup"><span data-stu-id="1c047-123">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c047-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="1c047-124">-ApiRevision</span></span>
<span data-ttu-id="1c047-125">Revisionsbezeichner der jeweiligen API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="1c047-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="1c047-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1c047-126">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c047-127">-Context</span><span class="sxs-lookup"><span data-stu-id="1c047-127">-Context</span></span>
<span data-ttu-id="1c047-128">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="1c047-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c047-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c047-129">-DefaultProfile</span></span>
<span data-ttu-id="1c047-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c047-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c047-131">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="1c047-131">-GatewayId</span></span>
<span data-ttu-id="1c047-132">Wenn diese Angabe angegeben ist, wird versucht, alle Gateway-APIs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1c047-132">If specified will try to get all Gateway APIs.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c047-133">-Name</span><span class="sxs-lookup"><span data-stu-id="1c047-133">-Name</span></span>
<span data-ttu-id="1c047-134">Gibt den Namen der zu abrufenden API an.</span><span class="sxs-lookup"><span data-stu-id="1c047-134">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c047-135">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1c047-135">-ProductId</span></span>
<span data-ttu-id="1c047-136">Gibt die ID des Produkts an, für das die API erhalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c047-136">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c047-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c047-137">CommonParameters</span></span>
<span data-ttu-id="1c047-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c047-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c047-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c047-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c047-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1c047-140">INPUTS</span></span>

### <span data-ttu-id="1c047-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1c047-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1c047-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1c047-142">System.String</span></span>

## <span data-ttu-id="1c047-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1c047-143">OUTPUTS</span></span>

### <span data-ttu-id="1c047-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1c047-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="1c047-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1c047-145">NOTES</span></span>

## <span data-ttu-id="1c047-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1c047-146">RELATED LINKS</span></span>

[<span data-ttu-id="1c047-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1c047-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="1c047-148">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1c047-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="1c047-149">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1c047-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="1c047-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1c047-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="1c047-151">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1c047-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


