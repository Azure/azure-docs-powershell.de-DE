---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 3759b5255794fcceb16018ecfc49bba362a03928
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949040"
---
# <span data-ttu-id="3cc83-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3cc83-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="3cc83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc83-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc83-103">Entfernt eine bestimmte API-Version</span><span class="sxs-lookup"><span data-stu-id="3cc83-103">Removes a particular API Release</span></span>

## <span data-ttu-id="3cc83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cc83-104">SYNTAX</span></span>

### <span data-ttu-id="3cc83-105">ByApiReleaseId (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cc83-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc83-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3cc83-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc83-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3cc83-107">DESCRIPTION</span></span>

<span data-ttu-id="3cc83-108">Das **Cmdlet Remove-AzAzureRmApiManagementApiRelease** entfernt eine vorhandene API Release.</span><span class="sxs-lookup"><span data-stu-id="3cc83-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="3cc83-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3cc83-109">EXAMPLES</span></span>

### <span data-ttu-id="3cc83-110">Beispiel 1: Entfernen einer API-Version</span><span class="sxs-lookup"><span data-stu-id="3cc83-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="3cc83-111">Mit diesem Befehl wird die API-Version mit der angegebenen ApiId und ReleaseId entfernt.</span><span class="sxs-lookup"><span data-stu-id="3cc83-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="3cc83-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3cc83-112">PARAMETERS</span></span>

### <span data-ttu-id="3cc83-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3cc83-113">-ApiId</span></span>
<span data-ttu-id="3cc83-114">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="3cc83-114">Identifier of the API.</span></span>
<span data-ttu-id="3cc83-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3cc83-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cc83-116">-Context</span><span class="sxs-lookup"><span data-stu-id="3cc83-116">-Context</span></span>
<span data-ttu-id="3cc83-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3cc83-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3cc83-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3cc83-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cc83-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc83-119">-DefaultProfile</span></span>
<span data-ttu-id="3cc83-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3cc83-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cc83-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cc83-121">-InputObject</span></span>
<span data-ttu-id="3cc83-122">Instanz von PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="3cc83-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="3cc83-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3cc83-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cc83-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cc83-124">-PassThru</span></span>
<span data-ttu-id="3cc83-125">Wenn angegeben wird, wird "true" geschrieben, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3cc83-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3cc83-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="3cc83-126">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cc83-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="3cc83-127">-ReleaseId</span></span>
<span data-ttu-id="3cc83-128">Bezeichner der API-Version.</span><span class="sxs-lookup"><span data-stu-id="3cc83-128">Identifier of the API Release.</span></span>
<span data-ttu-id="3cc83-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3cc83-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cc83-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cc83-130">-Confirm</span></span>
<span data-ttu-id="3cc83-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cc83-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc83-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc83-132">-WhatIf</span></span>
<span data-ttu-id="3cc83-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cc83-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cc83-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cc83-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc83-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc83-135">CommonParameters</span></span>
<span data-ttu-id="3cc83-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc83-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc83-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cc83-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc83-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3cc83-138">INPUTS</span></span>

### <span data-ttu-id="3cc83-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3cc83-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3cc83-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3cc83-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="3cc83-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3cc83-141">System.String</span></span>

## <span data-ttu-id="3cc83-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3cc83-142">OUTPUTS</span></span>

### <span data-ttu-id="3cc83-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3cc83-143">System.Boolean</span></span>

## <span data-ttu-id="3cc83-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3cc83-144">NOTES</span></span>

## <span data-ttu-id="3cc83-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3cc83-145">RELATED LINKS</span></span>

[<span data-ttu-id="3cc83-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3cc83-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="3cc83-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3cc83-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="3cc83-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="3cc83-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)