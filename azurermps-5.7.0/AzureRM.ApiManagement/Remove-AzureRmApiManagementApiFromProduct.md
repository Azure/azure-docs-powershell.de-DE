---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 413d03723ee2acdc162c1f1f5501d90156e16069
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504633"
---
# <span data-ttu-id="a8210-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="a8210-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="a8210-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8210-102">SYNOPSIS</span></span>
<span data-ttu-id="a8210-103">Entfernt eine API aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="a8210-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8210-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8210-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8210-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8210-105">DESCRIPTION</span></span>
<span data-ttu-id="a8210-106">Das Cmdlet **Remove-AzureRmApiManagementApiFromProduct** entfernt eine Azure API-Verwaltungs-API aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="a8210-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="a8210-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8210-107">EXAMPLES</span></span>

### <span data-ttu-id="a8210-108">Beispiel 1: Entfernen einer API von einem Produkt</span><span class="sxs-lookup"><span data-stu-id="a8210-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="a8210-109">Diese commnd entfernt die angegebene API aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="a8210-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="a8210-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8210-110">PARAMETERS</span></span>

### <span data-ttu-id="a8210-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a8210-111">-ApiId</span></span>
<span data-ttu-id="a8210-112">Gibt die ID der API an, die aus dem Produkt entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8210-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="a8210-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a8210-113">-Context</span></span>
<span data-ttu-id="a8210-114">Gibt einen **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="a8210-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="a8210-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8210-115">-DefaultProfile</span></span>
<span data-ttu-id="a8210-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8210-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a8210-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8210-117">-PassThru</span></span>
<span data-ttu-id="a8210-118">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="a8210-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="a8210-119">-ProductID</span><span class="sxs-lookup"><span data-stu-id="a8210-119">-ProductId</span></span>
<span data-ttu-id="a8210-120">Gibt die ID des Produkts an, aus dem die API entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8210-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="a8210-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8210-121">CommonParameters</span></span>
<span data-ttu-id="a8210-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8210-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8210-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8210-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8210-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8210-124">INPUTS</span></span>

### <span data-ttu-id="a8210-125">Keine</span><span class="sxs-lookup"><span data-stu-id="a8210-125">None</span></span>
<span data-ttu-id="a8210-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a8210-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8210-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8210-127">OUTPUTS</span></span>

### <span data-ttu-id="a8210-128">bool</span><span class="sxs-lookup"><span data-stu-id="a8210-128">bool</span></span>

## <span data-ttu-id="a8210-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8210-129">NOTES</span></span>

## <span data-ttu-id="a8210-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8210-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8210-131">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="a8210-131">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


