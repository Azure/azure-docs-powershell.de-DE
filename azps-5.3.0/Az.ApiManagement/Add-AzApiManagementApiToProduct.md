---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471530"
---
# <span data-ttu-id="30c63-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="30c63-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="30c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30c63-102">SYNOPSIS</span></span>
<span data-ttu-id="30c63-103">Fügt einem Produkt eine API hinzu.</span><span class="sxs-lookup"><span data-stu-id="30c63-103">Adds an API to a product.</span></span>

## <span data-ttu-id="30c63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30c63-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30c63-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30c63-105">DESCRIPTION</span></span>
<span data-ttu-id="30c63-106">Das **Cmdlet "Add-AzApiManagementApiToProduct"** fügt einem Produkt eine Azure API Management API hinzu.</span><span class="sxs-lookup"><span data-stu-id="30c63-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="30c63-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30c63-107">EXAMPLES</span></span>

### <span data-ttu-id="30c63-108">Beispiel 1: Hinzufügen einer API zu einem Produkt</span><span class="sxs-lookup"><span data-stu-id="30c63-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="30c63-109">Mit diesem Befehl wird dem angegebenen Produkt die angegebene API hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="30c63-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="30c63-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30c63-110">PARAMETERS</span></span>

### <span data-ttu-id="30c63-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="30c63-111">-ApiId</span></span>
<span data-ttu-id="30c63-112">Gibt die ID einer API an, die einem Produkt hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="30c63-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="30c63-113">-Context</span><span class="sxs-lookup"><span data-stu-id="30c63-113">-Context</span></span>
<span data-ttu-id="30c63-114">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="30c63-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="30c63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c63-115">-DefaultProfile</span></span>
<span data-ttu-id="30c63-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30c63-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c63-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30c63-117">-PassThru</span></span>
<span data-ttu-id="30c63-118">passthru</span><span class="sxs-lookup"><span data-stu-id="30c63-118">passthru</span></span>

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

### <span data-ttu-id="30c63-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="30c63-119">-ProductId</span></span>
<span data-ttu-id="30c63-120">Gibt die ID des Produkts an, dem die API hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="30c63-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="30c63-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c63-121">CommonParameters</span></span>
<span data-ttu-id="30c63-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c63-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c63-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30c63-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c63-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30c63-124">INPUTS</span></span>

### <span data-ttu-id="30c63-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="30c63-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="30c63-126">System.String</span><span class="sxs-lookup"><span data-stu-id="30c63-126">System.String</span></span>

### <span data-ttu-id="30c63-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="30c63-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="30c63-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30c63-128">OUTPUTS</span></span>

### <span data-ttu-id="30c63-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30c63-129">System.Boolean</span></span>

## <span data-ttu-id="30c63-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="30c63-130">NOTES</span></span>

## <span data-ttu-id="30c63-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="30c63-131">RELATED LINKS</span></span>

[<span data-ttu-id="30c63-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="30c63-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


