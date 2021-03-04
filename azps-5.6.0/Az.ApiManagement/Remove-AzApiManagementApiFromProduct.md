---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: af83bb3d6daa11eb62de81378e4e7d3e040b2db4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922139"
---
# <span data-ttu-id="64b11-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="64b11-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="64b11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64b11-102">SYNOPSIS</span></span>
<span data-ttu-id="64b11-103">Entfernt eine API aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="64b11-103">Removes an API from a product.</span></span>

## <span data-ttu-id="64b11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64b11-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64b11-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64b11-105">DESCRIPTION</span></span>
<span data-ttu-id="64b11-106">Das **Cmdlet Remove-AzApiManagementApiFromProduct** entfernt eine Azure API Management API aus einem Produkt.</span><span class="sxs-lookup"><span data-stu-id="64b11-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="64b11-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64b11-107">EXAMPLES</span></span>

### <span data-ttu-id="64b11-108">Beispiel 1: Entfernen einer API aus einem Produkt</span><span class="sxs-lookup"><span data-stu-id="64b11-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="64b11-109">Mit diesem Befehl wird die angegebene API aus einem Produkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="64b11-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="64b11-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="64b11-110">PARAMETERS</span></span>

### <span data-ttu-id="64b11-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="64b11-111">-ApiId</span></span>
<span data-ttu-id="64b11-112">Gibt die ID der API an, die aus dem Produkt entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64b11-112">Specifies the ID of the API to remove from the product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b11-113">-Context</span><span class="sxs-lookup"><span data-stu-id="64b11-113">-Context</span></span>
<span data-ttu-id="64b11-114">Gibt einen **PsApiManagementContext an.**</span><span class="sxs-lookup"><span data-stu-id="64b11-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="64b11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b11-115">-DefaultProfile</span></span>
<span data-ttu-id="64b11-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64b11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64b11-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64b11-117">-PassThru</span></span>
<span data-ttu-id="64b11-118">Gibt an, dass dieses Cmdlet einen Wert von $True, wenn es erfolgreich ist, oder andernfalls $False zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="64b11-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b11-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="64b11-119">-ProductId</span></span>
<span data-ttu-id="64b11-120">Gibt die ID des Produkts an, aus dem die API entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64b11-120">Specifies the ID of the product from which to remove the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64b11-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b11-121">CommonParameters</span></span>
<span data-ttu-id="64b11-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64b11-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b11-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64b11-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b11-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64b11-124">INPUTS</span></span>

### <span data-ttu-id="64b11-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="64b11-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="64b11-126">System.String</span><span class="sxs-lookup"><span data-stu-id="64b11-126">System.String</span></span>

### <span data-ttu-id="64b11-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="64b11-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="64b11-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64b11-128">OUTPUTS</span></span>

### <span data-ttu-id="64b11-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64b11-129">System.Boolean</span></span>

## <span data-ttu-id="64b11-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="64b11-130">NOTES</span></span>

## <span data-ttu-id="64b11-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="64b11-131">RELATED LINKS</span></span>

[<span data-ttu-id="64b11-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="64b11-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


