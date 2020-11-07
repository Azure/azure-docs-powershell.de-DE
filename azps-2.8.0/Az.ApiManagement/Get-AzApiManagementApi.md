---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApi.md
ms.openlocfilehash: 3fccd2becf08ee78ca928bd17043d83b0a277af9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658336"
---
# <span data-ttu-id="09068-101">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09068-101">Get-AzApiManagementApi</span></span>

## <span data-ttu-id="09068-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09068-102">SYNOPSIS</span></span>
<span data-ttu-id="09068-103">Ruft eine API ab.</span><span class="sxs-lookup"><span data-stu-id="09068-103">Gets an API.</span></span>

## <span data-ttu-id="09068-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09068-104">SYNTAX</span></span>

### <span data-ttu-id="09068-105">GetAllApis (Standard)</span><span class="sxs-lookup"><span data-stu-id="09068-105">GetAllApis (Default)</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09068-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="09068-106">GetByApiId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09068-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="09068-107">GetByName</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09068-108">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="09068-108">GetByProductId</span></span>
```
Get-AzApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09068-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09068-109">DESCRIPTION</span></span>
<span data-ttu-id="09068-110">Das Cmdlet " **Get-AzApiManagementApi** " Ruft eine oder mehrere Azure API-Verwaltungs-APIs ab.</span><span class="sxs-lookup"><span data-stu-id="09068-110">The **Get-AzApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="09068-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09068-111">EXAMPLES</span></span>

### <span data-ttu-id="09068-112">Beispiel 1: Abrufen aller Verwaltungs-APIs</span><span class="sxs-lookup"><span data-stu-id="09068-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="09068-113">Dieser Befehl ruft alle APIs für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="09068-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="09068-114">Beispiel 2: Abrufen einer Verwaltungs-API nach ID</span><span class="sxs-lookup"><span data-stu-id="09068-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="09068-115">Dieser Befehl ruft die API mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="09068-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="09068-116">Beispiel 3: Abrufen einer Verwaltungs-API nach Name</span><span class="sxs-lookup"><span data-stu-id="09068-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="09068-117">Dieser Befehl ruft die API mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="09068-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="09068-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="09068-118">PARAMETERS</span></span>

### <span data-ttu-id="09068-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="09068-119">-ApiId</span></span>
<span data-ttu-id="09068-120">Gibt die ID der API an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="09068-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="09068-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="09068-121">-ApiRevision</span></span>
<span data-ttu-id="09068-122">Revisions-ID der jeweiligen API-Revision.</span><span class="sxs-lookup"><span data-stu-id="09068-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="09068-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="09068-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="09068-124">-Context</span><span class="sxs-lookup"><span data-stu-id="09068-124">-Context</span></span>
<span data-ttu-id="09068-125">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="09068-125">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="09068-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09068-126">-DefaultProfile</span></span>
<span data-ttu-id="09068-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09068-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09068-128">-Name</span><span class="sxs-lookup"><span data-stu-id="09068-128">-Name</span></span>
<span data-ttu-id="09068-129">Gibt den Namen der API an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="09068-129">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="09068-130">-ProductID</span><span class="sxs-lookup"><span data-stu-id="09068-130">-ProductId</span></span>
<span data-ttu-id="09068-131">Gibt die ID des Produkts an, für das die API abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="09068-131">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="09068-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09068-132">CommonParameters</span></span>
<span data-ttu-id="09068-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09068-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09068-134">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09068-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09068-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09068-135">INPUTS</span></span>

### <span data-ttu-id="09068-136">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="09068-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="09068-137">System. String</span><span class="sxs-lookup"><span data-stu-id="09068-137">System.String</span></span>

## <span data-ttu-id="09068-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09068-138">OUTPUTS</span></span>

### <span data-ttu-id="09068-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09068-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="09068-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="09068-140">NOTES</span></span>

## <span data-ttu-id="09068-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09068-141">RELATED LINKS</span></span>

[<span data-ttu-id="09068-142">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09068-142">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="09068-143">Importieren-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09068-143">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="09068-144">Neu – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09068-144">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="09068-145">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09068-145">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="09068-146">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09068-146">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


