---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 08d6d8e5ecbcaa8b6810bd173062c5bb244ec5e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663272"
---
# <span data-ttu-id="9a253-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="9a253-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="9a253-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a253-102">SYNOPSIS</span></span>
<span data-ttu-id="9a253-103">Fügt eine API zu einem Produkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="9a253-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a253-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a253-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a253-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a253-105">DESCRIPTION</span></span>
<span data-ttu-id="9a253-106">Das Cmdlet **Add-AzureRmApiManagementApiToProduct** fügt einem Produkt eine Azure API-Verwaltungs-API hinzu.</span><span class="sxs-lookup"><span data-stu-id="9a253-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="9a253-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a253-107">EXAMPLES</span></span>

### <span data-ttu-id="9a253-108">Beispiel 1: Hinzufügen einer API zu einem Produkt</span><span class="sxs-lookup"><span data-stu-id="9a253-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="9a253-109">Mit diesem Befehl wird die angegebene API dem angegebenen Produkt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9a253-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="9a253-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a253-110">PARAMETERS</span></span>

### <span data-ttu-id="9a253-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9a253-111">-ApiId</span></span>
<span data-ttu-id="9a253-112">Gibt die ID einer API an, die einem Produkt hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a253-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a253-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9a253-113">-Context</span></span>
<span data-ttu-id="9a253-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9a253-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9a253-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a253-115">-DefaultProfile</span></span>
<span data-ttu-id="9a253-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a253-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a253-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a253-117">-PassThru</span></span>
<span data-ttu-id="9a253-118">passthru</span><span class="sxs-lookup"><span data-stu-id="9a253-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a253-119">-ProductID</span><span class="sxs-lookup"><span data-stu-id="9a253-119">-ProductId</span></span>
<span data-ttu-id="9a253-120">Gibt die ID des Produkts an, dem die API hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a253-120">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a253-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a253-121">CommonParameters</span></span>
<span data-ttu-id="9a253-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a253-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a253-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a253-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a253-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a253-124">INPUTS</span></span>

### <span data-ttu-id="9a253-125">Keine</span><span class="sxs-lookup"><span data-stu-id="9a253-125">None</span></span>
<span data-ttu-id="9a253-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9a253-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a253-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a253-127">OUTPUTS</span></span>

### <span data-ttu-id="9a253-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="9a253-128">Boolean</span></span>

## <span data-ttu-id="9a253-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a253-129">NOTES</span></span>

## <span data-ttu-id="9a253-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a253-130">RELATED LINKS</span></span>

[<span data-ttu-id="9a253-131">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="9a253-131">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


