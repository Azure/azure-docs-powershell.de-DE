---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 95784b084f6d106413c65b840dd73f313a47799e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664493"
---
# <span data-ttu-id="dc00c-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc00c-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="dc00c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc00c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc00c-103">Ruft eine API ab.</span><span class="sxs-lookup"><span data-stu-id="dc00c-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc00c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc00c-104">SYNTAX</span></span>

### <span data-ttu-id="dc00c-105">Alle APIs (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc00c-105">All APIs (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc00c-106">Nach ID suchen</span><span class="sxs-lookup"><span data-stu-id="dc00c-106">Find by ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc00c-107">Nach Namen suchen</span><span class="sxs-lookup"><span data-stu-id="dc00c-107">Find by Name</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc00c-108">Nach Produkt-ID suchen</span><span class="sxs-lookup"><span data-stu-id="dc00c-108">Find by product ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc00c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc00c-109">DESCRIPTION</span></span>
<span data-ttu-id="dc00c-110">Das Cmdlet " **Get-AzureRmApiManagementApi** " Ruft eine oder mehrere Azure API-Verwaltungs-APIs ab.</span><span class="sxs-lookup"><span data-stu-id="dc00c-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="dc00c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc00c-111">EXAMPLES</span></span>

### <span data-ttu-id="dc00c-112">Beispiel 1: Abrufen aller Verwaltungs-APIs</span><span class="sxs-lookup"><span data-stu-id="dc00c-112">Example 1: Get all management APIs</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="dc00c-113">Dieser Befehl ruft alle APIs für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="dc00c-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="dc00c-114">Beispiel 2: Abrufen einer Verwaltungs-API nach ID</span><span class="sxs-lookup"><span data-stu-id="dc00c-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="dc00c-115">Dieser Befehl ruft die API mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="dc00c-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="dc00c-116">Beispiel 3: Abrufen einer Verwaltungs-API nach Name</span><span class="sxs-lookup"><span data-stu-id="dc00c-116">Example 3: Get a management API by name</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="dc00c-117">Dieser Befehl ruft die API mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="dc00c-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="dc00c-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc00c-118">PARAMETERS</span></span>

### <span data-ttu-id="dc00c-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dc00c-119">-ApiId</span></span>
<span data-ttu-id="dc00c-120">Gibt die ID der API an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc00c-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc00c-121">-Context</span><span class="sxs-lookup"><span data-stu-id="dc00c-121">-Context</span></span>
<span data-ttu-id="dc00c-122">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="dc00c-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dc00c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dc00c-123">-Name</span></span>
<span data-ttu-id="dc00c-124">Gibt den Namen der API an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc00c-124">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by Name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc00c-125">-ProductID</span><span class="sxs-lookup"><span data-stu-id="dc00c-125">-ProductId</span></span>
<span data-ttu-id="dc00c-126">Gibt die ID des Produkts an, für das die API abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc00c-126">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by product ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc00c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc00c-127">-DefaultProfile</span></span>
<span data-ttu-id="dc00c-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc00c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc00c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc00c-129">CommonParameters</span></span>
<span data-ttu-id="dc00c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc00c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc00c-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc00c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc00c-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc00c-132">INPUTS</span></span>

## <span data-ttu-id="dc00c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc00c-133">OUTPUTS</span></span>

### <span data-ttu-id="dc00c-134">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi></span><span class="sxs-lookup"><span data-stu-id="dc00c-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>

## <span data-ttu-id="dc00c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc00c-135">NOTES</span></span>

## <span data-ttu-id="dc00c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc00c-136">RELATED LINKS</span></span>

[<span data-ttu-id="dc00c-137">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc00c-137">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="dc00c-138">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc00c-138">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="dc00c-139">Neu – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc00c-139">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="dc00c-140">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc00c-140">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="dc00c-141">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dc00c-141">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


