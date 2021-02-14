---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176180"
---
# <span data-ttu-id="b3a56-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3a56-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="b3a56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a56-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a56-103">aktualisiert einen Cache im API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="b3a56-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="b3a56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3a56-104">SYNTAX</span></span>

### <span data-ttu-id="b3a56-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3a56-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a56-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3a56-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a56-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a56-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3a56-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3a56-108">DESCRIPTION</span></span>
<span data-ttu-id="b3a56-109">Das Cmdlet **"Update-AzApiManagementCache"** aktualisiert einen Cache im ApiManagement-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b3a56-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="b3a56-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3a56-110">EXAMPLES</span></span>

### <span data-ttu-id="b3a56-111">Beispiel 1: Aktualisiert die Beschreibung des Caches in zentral</span><span class="sxs-lookup"><span data-stu-id="b3a56-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
```powershell
PS D:\github\azure-powershell> $context=New-AzApiManagementContext -ResourceGroupName Api-Default-Central-US -ServiceName contoso
PS D:\github\azure-powershell> Update-AzApiManagementCache -Context $context -CacheId centralus -Description "Team new cache" -PassThru


CacheId              : centralus
Description          : Team new cache
ConnectionString     : {{5cc19889e6ed3b0524c3f7d3}}
AzureRedisResourceId :
Id                   : /subscriptions/subid/resourceGroups/Api-Default-Central-US/providers/M
                       icrosoft.ApiManagement/service/contoso/caches/centralus
ResourceGroupName    : Api-Default-Central-US
ServiceName          : contoso
```

<span data-ttu-id="b3a56-112">Aktualisiert die Beschreibung des Caches in der Mitte der USA.</span><span class="sxs-lookup"><span data-stu-id="b3a56-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="b3a56-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3a56-113">PARAMETERS</span></span>

### <span data-ttu-id="b3a56-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a56-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="b3a56-115">Arm ResourceId der Azure Redis Cache-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b3a56-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="b3a56-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b3a56-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a56-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="b3a56-117">-CacheId</span></span>
<span data-ttu-id="b3a56-118">Id des neuen Caches.</span><span class="sxs-lookup"><span data-stu-id="b3a56-118">Identifier of new cache.</span></span>
<span data-ttu-id="b3a56-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3a56-119">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a56-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b3a56-120">-ConnectionString</span></span>
<span data-ttu-id="b3a56-121">Redis-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b3a56-121">Redis Connection String.</span></span>
<span data-ttu-id="b3a56-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b3a56-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a56-123">-Context</span><span class="sxs-lookup"><span data-stu-id="b3a56-123">-Context</span></span>
<span data-ttu-id="b3a56-124">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b3a56-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b3a56-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3a56-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a56-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a56-126">-DefaultProfile</span></span>
<span data-ttu-id="b3a56-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3a56-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a56-128">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3a56-128">-Description</span></span>
<span data-ttu-id="b3a56-129">Cachebeschreibung.</span><span class="sxs-lookup"><span data-stu-id="b3a56-129">Cache Description.</span></span>
<span data-ttu-id="b3a56-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b3a56-130">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a56-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3a56-131">-InputObject</span></span>
<span data-ttu-id="b3a56-132">Instanz von PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="b3a56-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="b3a56-133">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3a56-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a56-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3a56-134">-PassThru</span></span>
<span data-ttu-id="b3a56-135">Wenn angegeben, wird eine Instanz des Typs "Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache", der den geänderten Cache darstellt, in die Ausgabe geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b3a56-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="b3a56-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a56-136">-ResourceId</span></span>
<span data-ttu-id="b3a56-137">Arm ResourceId des Caches.</span><span class="sxs-lookup"><span data-stu-id="b3a56-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="b3a56-138">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b3a56-138">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a56-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3a56-139">-Confirm</span></span>
<span data-ttu-id="b3a56-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3a56-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a56-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b3a56-141">-WhatIf</span></span>
<span data-ttu-id="b3a56-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3a56-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a56-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3a56-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a56-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a56-144">CommonParameters</span></span>
<span data-ttu-id="b3a56-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a56-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a56-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3a56-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a56-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3a56-147">INPUTS</span></span>

### <span data-ttu-id="b3a56-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b3a56-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b3a56-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b3a56-149">System.String</span></span>

### <span data-ttu-id="b3a56-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3a56-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="b3a56-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3a56-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b3a56-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3a56-152">OUTPUTS</span></span>

### <span data-ttu-id="b3a56-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3a56-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="b3a56-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3a56-154">NOTES</span></span>

## <span data-ttu-id="b3a56-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3a56-155">RELATED LINKS</span></span>

[<span data-ttu-id="b3a56-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3a56-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="b3a56-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3a56-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="b3a56-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b3a56-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
