---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 8e59cbb9885587ee57103b78400ce8ece9aafd46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008219"
---
# <span data-ttu-id="2c9cf-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2c9cf-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="2c9cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9cf-103">Ruft eine Liste oder ein bestimmtes Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="2c9cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c9cf-104">SYNTAX</span></span>

### <span data-ttu-id="2c9cf-105">GetAllProducts (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c9cf-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c9cf-106">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="2c9cf-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c9cf-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="2c9cf-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c9cf-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="2c9cf-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c9cf-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c9cf-109">DESCRIPTION</span></span>
<span data-ttu-id="2c9cf-110">Das Cmdlet " **Get-AzApiManagementProduct** " Ruft eine Liste oder ein bestimmtes Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="2c9cf-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c9cf-111">EXAMPLES</span></span>

### <span data-ttu-id="2c9cf-112">Beispiel 1: Abrufen aller Produkte</span><span class="sxs-lookup"><span data-stu-id="2c9cf-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="2c9cf-113">Mit diesem Befehl werden alle API-Verwaltungsprodukte abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-113">This command get all API Management products.</span></span>

### <span data-ttu-id="2c9cf-114">Beispiel 2: Abrufen eines Produkts nach ID</span><span class="sxs-lookup"><span data-stu-id="2c9cf-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="2c9cf-115">Mit diesem Befehl wird ein API-Verwaltungsprodukt nach ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="2c9cf-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c9cf-116">PARAMETERS</span></span>

### <span data-ttu-id="2c9cf-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2c9cf-117">-ApiId</span></span>
<span data-ttu-id="2c9cf-118">ApiId der API, um die korrelierten Produkte zu finden.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="2c9cf-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c9cf-120">-Context</span><span class="sxs-lookup"><span data-stu-id="2c9cf-120">-Context</span></span>
<span data-ttu-id="2c9cf-121">Gibt eine Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2c9cf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9cf-122">-DefaultProfile</span></span>
<span data-ttu-id="2c9cf-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c9cf-124">-ProductID</span><span class="sxs-lookup"><span data-stu-id="2c9cf-124">-ProductId</span></span>
<span data-ttu-id="2c9cf-125">Gibt den Bezeichner des Produkts an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="2c9cf-126">-Title</span><span class="sxs-lookup"><span data-stu-id="2c9cf-126">-Title</span></span>
<span data-ttu-id="2c9cf-127">Gibt den Titel des Produkts an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="2c9cf-128">Wenn angegeben, versucht das Cmdlet, das Produkt nach Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-128">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTitle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c9cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9cf-129">CommonParameters</span></span>
<span data-ttu-id="2c9cf-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9cf-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c9cf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9cf-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c9cf-132">INPUTS</span></span>

### <span data-ttu-id="2c9cf-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2c9cf-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2c9cf-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2c9cf-134">System.String</span></span>

## <span data-ttu-id="2c9cf-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c9cf-135">OUTPUTS</span></span>

### <span data-ttu-id="2c9cf-136">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2c9cf-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="2c9cf-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c9cf-137">NOTES</span></span>

## <span data-ttu-id="2c9cf-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c9cf-138">RELATED LINKS</span></span>

[<span data-ttu-id="2c9cf-139">Neu – AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2c9cf-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="2c9cf-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2c9cf-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="2c9cf-141">Satz-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2c9cf-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


