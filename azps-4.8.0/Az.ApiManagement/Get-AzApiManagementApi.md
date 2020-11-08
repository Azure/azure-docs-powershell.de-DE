---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 8b6f27191ee92240a8dc9e5e8289fda72db856ab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174414"
---
# <span data-ttu-id="ae110-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae110-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="ae110-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae110-102">SYNOPSIS</span></span>
<span data-ttu-id="ae110-103">Ruft eine API ab.</span><span class="sxs-lookup"><span data-stu-id="ae110-103">Gets an API.</span></span>

## <span data-ttu-id="ae110-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae110-104">SYNTAX</span></span>

### <span data-ttu-id="ae110-105">GetAllApis (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae110-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae110-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="ae110-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae110-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="ae110-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae110-108">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="ae110-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae110-109">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="ae110-109">GetByGatewayId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae110-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae110-110">DESCRIPTION</span></span>
<span data-ttu-id="ae110-111">Das Cmdlet " **Get-AzApiManagementApi** " Ruft eine oder mehrere Azure API-Verwaltungs-APIs ab.</span><span class="sxs-lookup"><span data-stu-id="ae110-111">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="ae110-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae110-112">EXAMPLES</span></span>

### <span data-ttu-id="ae110-113">Beispiel 1: Abrufen aller Verwaltungs-APIs</span><span class="sxs-lookup"><span data-stu-id="ae110-113">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="ae110-114">Dieser Befehl ruft alle APIs für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="ae110-114">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="ae110-115">Beispiel 2: Abrufen einer Verwaltungs-API nach ID</span><span class="sxs-lookup"><span data-stu-id="ae110-115">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="ae110-116">Dieser Befehl ruft die API mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="ae110-116">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="ae110-117">Beispiel 3: Abrufen einer Verwaltungs-API nach Name</span><span class="sxs-lookup"><span data-stu-id="ae110-117">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="ae110-118">Dieser Befehl ruft die API mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="ae110-118">This command gets the API with the specified name.</span></span>

### <span data-ttu-id="ae110-119">Beispiel 4: Abrufen einer Verwaltungs-API nach Gateway-Nr</span><span class="sxs-lookup"><span data-stu-id="ae110-119">Example 4: Get a management API by GatewayId</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -GatewayId "g01"
```

<span data-ttu-id="ae110-120">Mit diesem Befehl wird die API für die angegebene Gatewayserver abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ae110-120">This command gets the API for the specified GatewayId.</span></span>

## <span data-ttu-id="ae110-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae110-121">PARAMETERS</span></span>

### <span data-ttu-id="ae110-122">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ae110-122">-ApiId</span></span>
<span data-ttu-id="ae110-123">Gibt die ID der API an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae110-123">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="ae110-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ae110-124">-ApiRevision</span></span>
<span data-ttu-id="ae110-125">Revisions-ID der jeweiligen API-Revision.</span><span class="sxs-lookup"><span data-stu-id="ae110-125">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="ae110-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae110-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="ae110-127">-Context</span><span class="sxs-lookup"><span data-stu-id="ae110-127">-Context</span></span>
<span data-ttu-id="ae110-128">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ae110-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ae110-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae110-129">-DefaultProfile</span></span>
<span data-ttu-id="ae110-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae110-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae110-131">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="ae110-131">-GatewayId</span></span>
<span data-ttu-id="ae110-132">Wenn angegeben, wird versucht, alle Gateway-APIs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ae110-132">If specified will try to get all Gateway APIs.</span></span>

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

### <span data-ttu-id="ae110-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ae110-133">-Name</span></span>
<span data-ttu-id="ae110-134">Gibt den Namen der API an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae110-134">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="ae110-135">-ProductID</span><span class="sxs-lookup"><span data-stu-id="ae110-135">-ProductId</span></span>
<span data-ttu-id="ae110-136">Gibt die ID des Produkts an, für das die API abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae110-136">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="ae110-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae110-137">CommonParameters</span></span>
<span data-ttu-id="ae110-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae110-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae110-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae110-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae110-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae110-140">INPUTS</span></span>

### <span data-ttu-id="ae110-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ae110-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ae110-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ae110-142">System.String</span></span>

## <span data-ttu-id="ae110-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae110-143">OUTPUTS</span></span>

### <span data-ttu-id="ae110-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae110-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="ae110-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae110-145">NOTES</span></span>

## <span data-ttu-id="ae110-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae110-146">RELATED LINKS</span></span>

[<span data-ttu-id="ae110-147">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae110-147">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="ae110-148">Importieren-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae110-148">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="ae110-149">Neu – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae110-149">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="ae110-150">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae110-150">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="ae110-151">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ae110-151">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


