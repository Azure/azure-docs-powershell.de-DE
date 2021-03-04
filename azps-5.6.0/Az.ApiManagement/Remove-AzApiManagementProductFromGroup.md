---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: 05f3ac10171c9135b59b9fb6894f5b5fbf670de0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923064"
---
# <span data-ttu-id="9e767-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="9e767-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="9e767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e767-102">SYNOPSIS</span></span>
<span data-ttu-id="9e767-103">Entfernt ein Produkt aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9e767-103">Removes a product from a group.</span></span>

## <span data-ttu-id="9e767-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e767-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e767-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e767-105">DESCRIPTION</span></span>
<span data-ttu-id="9e767-106">Das **Cmdlet Remove-AzApiManagementProductFromGroup** entfernt ein Produkt aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9e767-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="9e767-107">Mit anderen Worten: Mit diesem Cmdlet wird die Gruppenzuordnung aus einem Produkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="9e767-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="9e767-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e767-108">EXAMPLES</span></span>

### <span data-ttu-id="9e767-109">Beispiel 1: Entfernen eines Produkts aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="9e767-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="9e767-110">Mit diesem Befehl wird ein Produkt aus einer vorhandenen Gruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="9e767-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="9e767-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9e767-111">PARAMETERS</span></span>

### <span data-ttu-id="9e767-112">-Context</span><span class="sxs-lookup"><span data-stu-id="9e767-112">-Context</span></span>
<span data-ttu-id="9e767-113">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="9e767-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="9e767-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e767-114">This parameter is required.</span></span>

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

### <span data-ttu-id="9e767-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e767-115">-DefaultProfile</span></span>
<span data-ttu-id="9e767-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e767-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e767-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="9e767-117">-GroupId</span></span>
<span data-ttu-id="9e767-118">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="9e767-118">Specifies the group ID.</span></span>
<span data-ttu-id="9e767-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e767-119">This parameter is required.</span></span>

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

### <span data-ttu-id="9e767-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e767-120">-PassThru</span></span>
<span data-ttu-id="9e767-121">Gibt an, dass dieses Cmdlet einen Wert von $True zurückgibt, wenn es erfolgreich ist, oder andernfalls $False.</span><span class="sxs-lookup"><span data-stu-id="9e767-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="9e767-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9e767-122">-ProductId</span></span>
<span data-ttu-id="9e767-123">Gibt die Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="9e767-123">Specifies the product ID.</span></span>
<span data-ttu-id="9e767-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e767-124">This parameter is required.</span></span>

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

### <span data-ttu-id="9e767-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e767-125">CommonParameters</span></span>
<span data-ttu-id="9e767-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e767-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e767-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e767-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e767-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e767-128">INPUTS</span></span>

### <span data-ttu-id="9e767-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9e767-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e767-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9e767-130">System.String</span></span>

### <span data-ttu-id="9e767-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9e767-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9e767-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e767-132">OUTPUTS</span></span>

### <span data-ttu-id="9e767-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e767-133">System.Boolean</span></span>

## <span data-ttu-id="9e767-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9e767-134">NOTES</span></span>

## <span data-ttu-id="9e767-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9e767-135">RELATED LINKS</span></span>

[<span data-ttu-id="9e767-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="9e767-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


