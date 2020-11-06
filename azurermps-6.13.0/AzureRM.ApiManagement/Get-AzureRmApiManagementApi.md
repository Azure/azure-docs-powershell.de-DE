---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: d84efcf68885e6d2e39ae15944c5f60298044ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478062"
---
# <span data-ttu-id="e57d5-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e57d5-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="e57d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e57d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e57d5-103">Ruft eine API ab.</span><span class="sxs-lookup"><span data-stu-id="e57d5-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e57d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e57d5-104">SYNTAX</span></span>

### <span data-ttu-id="e57d5-105">GetAllApis (Standard)</span><span class="sxs-lookup"><span data-stu-id="e57d5-105">GetAllApis (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e57d5-106">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="e57d5-106">GetByApiId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57d5-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="e57d5-107">GetByName</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57d5-108">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="e57d5-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e57d5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e57d5-109">DESCRIPTION</span></span>
<span data-ttu-id="e57d5-110">Das Cmdlet " **Get-AzureRmApiManagementApi** " Ruft eine oder mehrere Azure API-Verwaltungs-APIs ab.</span><span class="sxs-lookup"><span data-stu-id="e57d5-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="e57d5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e57d5-111">EXAMPLES</span></span>

### <span data-ttu-id="e57d5-112">Beispiel 1: Abrufen aller Verwaltungs-APIs</span><span class="sxs-lookup"><span data-stu-id="e57d5-112">Example 1: Get all management APIs</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="e57d5-113">Dieser Befehl ruft alle APIs für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="e57d5-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="e57d5-114">Beispiel 2: Abrufen einer Verwaltungs-API nach ID</span><span class="sxs-lookup"><span data-stu-id="e57d5-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="e57d5-115">Dieser Befehl ruft die API mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="e57d5-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="e57d5-116">Beispiel 3: Abrufen einer Verwaltungs-API nach Name</span><span class="sxs-lookup"><span data-stu-id="e57d5-116">Example 3: Get a management API by name</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="e57d5-117">Dieser Befehl ruft die API mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="e57d5-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="e57d5-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e57d5-118">PARAMETERS</span></span>

### <span data-ttu-id="e57d5-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e57d5-119">-ApiId</span></span>
<span data-ttu-id="e57d5-120">Gibt die ID der API an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e57d5-120">Specifies the ID of the API to get.</span></span>

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

### <span data-ttu-id="e57d5-121">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e57d5-121">-ApiRevision</span></span>
<span data-ttu-id="e57d5-122">Revisions-ID der jeweiligen API-Revision.</span><span class="sxs-lookup"><span data-stu-id="e57d5-122">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="e57d5-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e57d5-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="e57d5-124">-Context</span><span class="sxs-lookup"><span data-stu-id="e57d5-124">-Context</span></span>
<span data-ttu-id="e57d5-125">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e57d5-125">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57d5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57d5-126">-DefaultProfile</span></span>
<span data-ttu-id="e57d5-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e57d5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57d5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e57d5-128">-Name</span></span>
<span data-ttu-id="e57d5-129">Gibt den Namen der API an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e57d5-129">Specifies the name of the API to get.</span></span>

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

### <span data-ttu-id="e57d5-130">-ProductID</span><span class="sxs-lookup"><span data-stu-id="e57d5-130">-ProductId</span></span>
<span data-ttu-id="e57d5-131">Gibt die ID des Produkts an, für das die API abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e57d5-131">Specifies the ID of the product for which to get the API.</span></span>

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

### <span data-ttu-id="e57d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57d5-132">CommonParameters</span></span>
<span data-ttu-id="e57d5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57d5-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e57d5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57d5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e57d5-135">INPUTS</span></span>

### <span data-ttu-id="e57d5-136">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e57d5-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e57d5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e57d5-137">System.String</span></span>

## <span data-ttu-id="e57d5-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e57d5-138">OUTPUTS</span></span>

### <span data-ttu-id="e57d5-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e57d5-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e57d5-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="e57d5-140">NOTES</span></span>

## <span data-ttu-id="e57d5-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e57d5-141">RELATED LINKS</span></span>

[<span data-ttu-id="e57d5-142">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e57d5-142">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="e57d5-143">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e57d5-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="e57d5-144">Neu – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e57d5-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="e57d5-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e57d5-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="e57d5-146">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e57d5-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


