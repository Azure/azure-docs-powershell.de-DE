---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: ab0aeb77bd5f28520e39548f539d07516cd17ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498098"
---
# <span data-ttu-id="fdaf5-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fdaf5-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="fdaf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fdaf5-102">SYNOPSIS</span></span>
<span data-ttu-id="fdaf5-103">Ruft eine Liste oder ein bestimmtes Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="fdaf5-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdaf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdaf5-104">SYNTAX</span></span>

### <span data-ttu-id="fdaf5-105">Abrufen aller producest (Standard)</span><span class="sxs-lookup"><span data-stu-id="fdaf5-105">Get all producst (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdaf5-106">Abrufen nach ID</span><span class="sxs-lookup"><span data-stu-id="fdaf5-106">Get by Id</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdaf5-107">Nach Titel abrufen</span><span class="sxs-lookup"><span data-stu-id="fdaf5-107">Get by Title</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdaf5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdaf5-108">DESCRIPTION</span></span>
<span data-ttu-id="fdaf5-109">Das Cmdlet " **Get-AzureRmApiManagementProduct** " Ruft eine Liste oder ein bestimmtes Produkt ab.</span><span class="sxs-lookup"><span data-stu-id="fdaf5-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="fdaf5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdaf5-110">EXAMPLES</span></span>

### <span data-ttu-id="fdaf5-111">Beispiel 1: Abrufen aller Produkte</span><span class="sxs-lookup"><span data-stu-id="fdaf5-111">Example 1: Get all products</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext
```

<span data-ttu-id="fdaf5-112">Mit diesem Befehl werden alle API-Verwaltungsprodukte abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fdaf5-112">This command get all API Management products.</span></span>

### <span data-ttu-id="fdaf5-113">Beispiel 2: Abrufen eines Produkts nach ID</span><span class="sxs-lookup"><span data-stu-id="fdaf5-113">Example 2: Get a product by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="fdaf5-114">Mit diesem Befehl wird ein API-Verwaltungsprodukt nach ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fdaf5-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="fdaf5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdaf5-115">PARAMETERS</span></span>

### <span data-ttu-id="fdaf5-116">-Context</span><span class="sxs-lookup"><span data-stu-id="fdaf5-116">-Context</span></span>
<span data-ttu-id="fdaf5-117">Gibt eine Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="fdaf5-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fdaf5-118">-ProductID</span><span class="sxs-lookup"><span data-stu-id="fdaf5-118">-ProductId</span></span>
<span data-ttu-id="fdaf5-119">Gibt den Bezeichner des Produkts an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="fdaf5-119">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdaf5-120">-Title</span><span class="sxs-lookup"><span data-stu-id="fdaf5-120">-Title</span></span>
<span data-ttu-id="fdaf5-121">Gibt den Titel des Produkts an, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="fdaf5-121">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="fdaf5-122">Wenn angegeben, versucht das Cmdlet, das Produkt nach Titel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fdaf5-122">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Title
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdaf5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdaf5-123">-DefaultProfile</span></span>
<span data-ttu-id="fdaf5-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fdaf5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdaf5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdaf5-125">CommonParameters</span></span>
<span data-ttu-id="fdaf5-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdaf5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdaf5-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdaf5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdaf5-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fdaf5-128">INPUTS</span></span>

## <span data-ttu-id="fdaf5-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fdaf5-129">OUTPUTS</span></span>

### <span data-ttu-id="fdaf5-130">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="fdaf5-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>

## <span data-ttu-id="fdaf5-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="fdaf5-131">NOTES</span></span>

## <span data-ttu-id="fdaf5-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fdaf5-132">RELATED LINKS</span></span>

[<span data-ttu-id="fdaf5-133">Neu – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fdaf5-133">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="fdaf5-134">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fdaf5-134">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="fdaf5-135">Satz-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="fdaf5-135">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


