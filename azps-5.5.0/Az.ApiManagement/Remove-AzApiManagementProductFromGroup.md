---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164401"
---
# <span data-ttu-id="229df-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="229df-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="229df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="229df-102">SYNOPSIS</span></span>
<span data-ttu-id="229df-103">Entfernt ein Produkt aus einer Gruppe.</span><span class="sxs-lookup"><span data-stu-id="229df-103">Removes a product from a group.</span></span>

## <span data-ttu-id="229df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="229df-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="229df-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="229df-105">DESCRIPTION</span></span>
<span data-ttu-id="229df-106">Das **Cmdlet "Remove-AzApiManagementProductFromGroup"** entfernt ein Produkt aus einer vorhandenen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="229df-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="229df-107">Mit anderen Worten: Mit diesem Cmdlet wird die Gruppenzuordnung aus einem Produkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="229df-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="229df-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="229df-108">EXAMPLES</span></span>

### <span data-ttu-id="229df-109">Beispiel 1: Entfernen eines Produkts aus einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="229df-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="229df-110">Mit diesem Befehl wird ein Produkt aus einer vorhandenen Gruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="229df-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="229df-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="229df-111">PARAMETERS</span></span>

### <span data-ttu-id="229df-112">-Context</span><span class="sxs-lookup"><span data-stu-id="229df-112">-Context</span></span>
<span data-ttu-id="229df-113">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="229df-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="229df-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="229df-114">This parameter is required.</span></span>

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

### <span data-ttu-id="229df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229df-115">-DefaultProfile</span></span>
<span data-ttu-id="229df-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="229df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="229df-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="229df-117">-GroupId</span></span>
<span data-ttu-id="229df-118">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="229df-118">Specifies the group ID.</span></span>
<span data-ttu-id="229df-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="229df-119">This parameter is required.</span></span>

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

### <span data-ttu-id="229df-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="229df-120">-PassThru</span></span>
<span data-ttu-id="229df-121">Gibt an, dass dieses Cmdlet den Wert "$True" zurückgibt, wenn es erfolgreich ist, oder $False.</span><span class="sxs-lookup"><span data-stu-id="229df-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="229df-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="229df-122">-ProductId</span></span>
<span data-ttu-id="229df-123">Gibt die Produkt-ID an.</span><span class="sxs-lookup"><span data-stu-id="229df-123">Specifies the product ID.</span></span>
<span data-ttu-id="229df-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="229df-124">This parameter is required.</span></span>

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

### <span data-ttu-id="229df-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229df-125">CommonParameters</span></span>
<span data-ttu-id="229df-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229df-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229df-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="229df-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229df-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="229df-128">INPUTS</span></span>

### <span data-ttu-id="229df-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="229df-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="229df-130">System.String</span><span class="sxs-lookup"><span data-stu-id="229df-130">System.String</span></span>

### <span data-ttu-id="229df-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="229df-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="229df-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="229df-132">OUTPUTS</span></span>

### <span data-ttu-id="229df-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="229df-133">System.Boolean</span></span>

## <span data-ttu-id="229df-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="229df-134">NOTES</span></span>

## <span data-ttu-id="229df-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="229df-135">RELATED LINKS</span></span>

[<span data-ttu-id="229df-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="229df-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


