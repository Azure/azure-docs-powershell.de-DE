---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305288"
---
# <span data-ttu-id="2183e-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="2183e-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="2183e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2183e-102">SYNOPSIS</span></span>
<span data-ttu-id="2183e-103">Entfernt ein Produkt aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2183e-103">Removes a product from a group.</span></span>

## <span data-ttu-id="2183e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2183e-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2183e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2183e-105">DESCRIPTION</span></span>
<span data-ttu-id="2183e-106">Das **Cmdlet "Remove-AzApiManagementProductFromGroup"** entfernt ein Produkt aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2183e-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="2183e-107">Mit anderen Worten: Mit diesem Cmdlet wird die Gruppenzuordnung aus einem Produkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="2183e-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="2183e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2183e-108">EXAMPLES</span></span>

### <span data-ttu-id="2183e-109">Beispiel 1: Entfernen eines Produkts aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="2183e-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="2183e-110">Mit diesem Befehl wird ein Produkt aus einer vorhandenen Gruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="2183e-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="2183e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2183e-111">PARAMETERS</span></span>

### <span data-ttu-id="2183e-112">-Context</span><span class="sxs-lookup"><span data-stu-id="2183e-112">-Context</span></span>
<span data-ttu-id="2183e-113">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="2183e-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2183e-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2183e-114">This parameter is required.</span></span>

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

### <span data-ttu-id="2183e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2183e-115">-DefaultProfile</span></span>
<span data-ttu-id="2183e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2183e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2183e-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2183e-117">-GroupId</span></span>
<span data-ttu-id="2183e-118">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="2183e-118">Specifies the group ID.</span></span>
<span data-ttu-id="2183e-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2183e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="2183e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2183e-120">-PassThru</span></span>
<span data-ttu-id="2183e-121">Gibt an, dass dieses Cmdlet den Wert "$True" zurückgibt, wenn es erfolgreich ist, oder $False.</span><span class="sxs-lookup"><span data-stu-id="2183e-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="2183e-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2183e-122">-ProductId</span></span>
<span data-ttu-id="2183e-123">Gibt die Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="2183e-123">Specifies the product ID.</span></span>
<span data-ttu-id="2183e-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2183e-124">This parameter is required.</span></span>

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

### <span data-ttu-id="2183e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2183e-125">CommonParameters</span></span>
<span data-ttu-id="2183e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2183e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2183e-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2183e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2183e-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2183e-128">INPUTS</span></span>

### <span data-ttu-id="2183e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2183e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2183e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2183e-130">System.String</span></span>

### <span data-ttu-id="2183e-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2183e-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2183e-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2183e-132">OUTPUTS</span></span>

### <span data-ttu-id="2183e-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2183e-133">System.Boolean</span></span>

## <span data-ttu-id="2183e-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2183e-134">NOTES</span></span>

## <span data-ttu-id="2183e-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2183e-135">RELATED LINKS</span></span>

[<span data-ttu-id="2183e-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="2183e-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


