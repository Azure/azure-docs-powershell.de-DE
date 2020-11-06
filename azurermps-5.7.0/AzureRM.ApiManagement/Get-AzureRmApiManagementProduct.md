---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: a4bbc330b5cd4d7eaeec1d2e68252ceb5dd261f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483221"
---
# <span data-ttu-id="7b348-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7b348-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="7b348-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b348-102">SYNOPSIS</span></span>
<span data-ttu-id="7b348-103">Ruft eine Liste oder ein bestimmtes Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="7b348-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b348-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b348-104">SYNTAX</span></span>

### <span data-ttu-id="7b348-105">GetAllProducts (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b348-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b348-106">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="7b348-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b348-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="7b348-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b348-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b348-108">DESCRIPTION</span></span>
<span data-ttu-id="7b348-109">Das Cmdlet " **Get-AzureRmApiManagementProduct** " Ruft eine Liste oder ein bestimmtes Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="7b348-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="7b348-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b348-110">EXAMPLES</span></span>

### <span data-ttu-id="7b348-111">Beispiel 1: Abrufen aller Produkte</span><span class="sxs-lookup"><span data-stu-id="7b348-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="7b348-112">Mit diesem Befehl werden alle API-Verwaltungsprodukte abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7b348-112">This command get all API Management products.</span></span>

### <span data-ttu-id="7b348-113">Beispiel 2: Abrufen eines Produkts nach ID</span><span class="sxs-lookup"><span data-stu-id="7b348-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="7b348-114">Mit diesem Befehl wird ein API-Verwaltungsprodukt nach ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7b348-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="7b348-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b348-115">PARAMETERS</span></span>

### <span data-ttu-id="7b348-116">-Context</span><span class="sxs-lookup"><span data-stu-id="7b348-116">-Context</span></span>
<span data-ttu-id="7b348-117">Gibt eine Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="7b348-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b348-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b348-118">-DefaultProfile</span></span>
<span data-ttu-id="7b348-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b348-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b348-120">-ProductID</span><span class="sxs-lookup"><span data-stu-id="7b348-120">-ProductId</span></span>
<span data-ttu-id="7b348-121">Gibt den Bezeichner des Produkts an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b348-121">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b348-122">-Title</span><span class="sxs-lookup"><span data-stu-id="7b348-122">-Title</span></span>
<span data-ttu-id="7b348-123">Gibt den Titel des Produkts an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b348-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="7b348-124">Wenn angegeben, versucht das Cmdlet, das Produkt nach Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7b348-124">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: String
Parameter Sets: GetByTitle
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b348-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b348-125">CommonParameters</span></span>
<span data-ttu-id="7b348-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b348-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b348-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b348-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b348-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b348-128">INPUTS</span></span>

### <span data-ttu-id="7b348-129">Keine</span><span class="sxs-lookup"><span data-stu-id="7b348-129">None</span></span>
<span data-ttu-id="7b348-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7b348-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b348-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b348-131">OUTPUTS</span></span>

### <span data-ttu-id="7b348-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7b348-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>
<span data-ttu-id="7b348-133">Die Details des Produkts im API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="7b348-133">The details of the Product in API Management service.</span></span>

### <span data-ttu-id="7b348-134">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="7b348-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>
<span data-ttu-id="7b348-135">Die Liste des Produkts im API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="7b348-135">The list of Product in API Management service.</span></span>

## <span data-ttu-id="7b348-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b348-136">NOTES</span></span>

## <span data-ttu-id="7b348-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b348-137">RELATED LINKS</span></span>

[<span data-ttu-id="7b348-138">Neu – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7b348-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="7b348-139">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7b348-139">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="7b348-140">Satz-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7b348-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


