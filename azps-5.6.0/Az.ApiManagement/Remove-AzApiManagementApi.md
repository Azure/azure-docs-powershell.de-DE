---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: d1ef516fc8b95814685350eb309e0a56d08d4b59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922171"
---
# <span data-ttu-id="9a329-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9a329-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="9a329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a329-102">SYNOPSIS</span></span>
<span data-ttu-id="9a329-103">Entfernt eine API.</span><span class="sxs-lookup"><span data-stu-id="9a329-103">Removes an API.</span></span>

## <span data-ttu-id="9a329-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a329-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a329-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a329-105">DESCRIPTION</span></span>
<span data-ttu-id="9a329-106">Das **Cmdlet Remove-AzApiManagementApi** entfernt eine vorhandene API.</span><span class="sxs-lookup"><span data-stu-id="9a329-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="9a329-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9a329-107">EXAMPLES</span></span>

### <span data-ttu-id="9a329-108">Beispiel 1: Entfernen einer API</span><span class="sxs-lookup"><span data-stu-id="9a329-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="9a329-109">Mit diesem Befehl wird die API mit der angegebenen ID entfernt.</span><span class="sxs-lookup"><span data-stu-id="9a329-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="9a329-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9a329-110">PARAMETERS</span></span>

### <span data-ttu-id="9a329-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9a329-111">-ApiId</span></span>
<span data-ttu-id="9a329-112">Gibt die ID der API remove an.</span><span class="sxs-lookup"><span data-stu-id="9a329-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="9a329-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9a329-113">-Context</span></span>
<span data-ttu-id="9a329-114">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="9a329-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9a329-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a329-115">-DefaultProfile</span></span>
<span data-ttu-id="9a329-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a329-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a329-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a329-117">-PassThru</span></span>
<span data-ttu-id="9a329-118">passthru</span><span class="sxs-lookup"><span data-stu-id="9a329-118">passthru</span></span>

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

### <span data-ttu-id="9a329-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9a329-119">-Confirm</span></span>
<span data-ttu-id="9a329-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a329-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a329-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a329-121">-WhatIf</span></span>
<span data-ttu-id="9a329-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a329-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a329-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a329-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a329-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a329-124">CommonParameters</span></span>
<span data-ttu-id="9a329-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a329-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a329-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a329-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a329-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9a329-127">INPUTS</span></span>

### <span data-ttu-id="9a329-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9a329-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9a329-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9a329-129">System.String</span></span>

### <span data-ttu-id="9a329-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a329-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9a329-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9a329-131">OUTPUTS</span></span>

### <span data-ttu-id="9a329-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a329-132">System.Boolean</span></span>

## <span data-ttu-id="9a329-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9a329-133">NOTES</span></span>

## <span data-ttu-id="9a329-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9a329-134">RELATED LINKS</span></span>

[<span data-ttu-id="9a329-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9a329-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="9a329-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9a329-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="9a329-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9a329-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="9a329-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9a329-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="9a329-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9a329-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


