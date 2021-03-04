---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 9a5c4d553f425d7922fa927451ca9f3029a9f4b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929107"
---
# <span data-ttu-id="d4649-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d4649-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="d4649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4649-102">SYNOPSIS</span></span>
<span data-ttu-id="d4649-103">Entfernt ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="d4649-103">Removes a Backend.</span></span>

## <span data-ttu-id="d4649-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4649-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4649-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4649-105">DESCRIPTION</span></span>
<span data-ttu-id="d4649-106">Entfernt ein vom Bezeichner angegebenes Back-End aus der Api-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="d4649-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="d4649-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4649-107">EXAMPLES</span></span>

### <span data-ttu-id="d4649-108">Beispiel 1: Entfernen des Back-End 123</span><span class="sxs-lookup"><span data-stu-id="d4649-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="d4649-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d4649-109">PARAMETERS</span></span>

### <span data-ttu-id="d4649-110">-Back-EndId</span><span class="sxs-lookup"><span data-stu-id="d4649-110">-BackendId</span></span>
<span data-ttu-id="d4649-111">Bezeichner des vorhandenen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="d4649-111">Identifier of existing backend.</span></span>
<span data-ttu-id="d4649-112">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4649-112">This parameter is required.</span></span>

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

### <span data-ttu-id="d4649-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d4649-113">-Context</span></span>
<span data-ttu-id="d4649-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d4649-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d4649-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4649-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d4649-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4649-116">-DefaultProfile</span></span>
<span data-ttu-id="d4649-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4649-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4649-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4649-118">-PassThru</span></span>
<span data-ttu-id="d4649-119">Wenn angegeben wird, wird "true" geschrieben, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="d4649-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d4649-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d4649-120">This parameter is optional.</span></span>
<span data-ttu-id="d4649-121">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="d4649-121">Default value is false.</span></span>

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

### <span data-ttu-id="d4649-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4649-122">-Confirm</span></span>
<span data-ttu-id="d4649-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4649-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4649-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4649-124">-WhatIf</span></span>
<span data-ttu-id="d4649-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4649-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4649-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4649-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4649-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4649-127">CommonParameters</span></span>
<span data-ttu-id="d4649-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4649-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4649-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4649-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4649-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4649-130">INPUTS</span></span>

### <span data-ttu-id="d4649-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d4649-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d4649-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d4649-132">System.String</span></span>

### <span data-ttu-id="d4649-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d4649-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d4649-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4649-134">OUTPUTS</span></span>

### <span data-ttu-id="d4649-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4649-135">System.Boolean</span></span>

## <span data-ttu-id="d4649-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d4649-136">NOTES</span></span>

## <span data-ttu-id="d4649-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d4649-137">RELATED LINKS</span></span>

[<span data-ttu-id="d4649-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d4649-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="d4649-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d4649-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="d4649-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d4649-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="d4649-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d4649-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="d4649-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d4649-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
