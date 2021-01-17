---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382149"
---
# <span data-ttu-id="fe7a8-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="fe7a8-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="fe7a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe7a8-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7a8-103">Entfernt die Cacheentität.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-103">Removes the cache entity.</span></span>

## <span data-ttu-id="fe7a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe7a8-104">SYNTAX</span></span>

### <span data-ttu-id="fe7a8-105">ContextParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe7a8-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe7a8-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe7a8-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe7a8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe7a8-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe7a8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe7a8-108">DESCRIPTION</span></span>
<span data-ttu-id="fe7a8-109">Das Cmdlet **"Remove-AzApiManagementCache"** entfernt die Cacheentität.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="fe7a8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe7a8-110">EXAMPLES</span></span>

### <span data-ttu-id="fe7a8-111">Beispiel 1: Entfernen der Entität "Cache"</span><span class="sxs-lookup"><span data-stu-id="fe7a8-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="fe7a8-112">Dieses Cmdlet entfernt den Cache `centralus` aus dem API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="fe7a8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe7a8-113">PARAMETERS</span></span>

### <span data-ttu-id="fe7a8-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="fe7a8-114">-CacheId</span></span>
<span data-ttu-id="fe7a8-115">Bezeichner der vorhandenen CacheId.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="fe7a8-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7a8-117">-Context</span><span class="sxs-lookup"><span data-stu-id="fe7a8-117">-Context</span></span>
<span data-ttu-id="fe7a8-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fe7a8-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7a8-120">-DefaultProfile</span></span>
<span data-ttu-id="fe7a8-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe7a8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe7a8-122">-InputObject</span></span>
<span data-ttu-id="fe7a8-123">Instanz von PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="fe7a8-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7a8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe7a8-125">-PassThru</span></span>
<span data-ttu-id="fe7a8-126">Wenn angegeben, wird "true" für den Fall geschrieben, dass der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="fe7a8-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-127">This parameter is optional.</span></span>
<span data-ttu-id="fe7a8-128">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="fe7a8-128">Default value is false.</span></span>

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

### <span data-ttu-id="fe7a8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe7a8-129">-ResourceId</span></span>
<span data-ttu-id="fe7a8-130">Arm ResourceId des Caches.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="fe7a8-131">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe7a8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe7a8-132">-Confirm</span></span>
<span data-ttu-id="fe7a8-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe7a8-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fe7a8-134">-WhatIf</span></span>
<span data-ttu-id="fe7a8-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe7a8-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe7a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7a8-137">CommonParameters</span></span>
<span data-ttu-id="fe7a8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe7a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7a8-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe7a8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7a8-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe7a8-140">INPUTS</span></span>

### <span data-ttu-id="fe7a8-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fe7a8-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fe7a8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fe7a8-142">System.String</span></span>

### <span data-ttu-id="fe7a8-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fe7a8-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fe7a8-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe7a8-144">OUTPUTS</span></span>

### <span data-ttu-id="fe7a8-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fe7a8-145">System.Boolean</span></span>

## <span data-ttu-id="fe7a8-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe7a8-146">NOTES</span></span>

## <span data-ttu-id="fe7a8-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe7a8-147">RELATED LINKS</span></span>

[<span data-ttu-id="fe7a8-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="fe7a8-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="fe7a8-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="fe7a8-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="fe7a8-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="fe7a8-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
