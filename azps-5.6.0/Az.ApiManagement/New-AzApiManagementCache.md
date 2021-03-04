---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 13fe16c2612a267df0760aad939b46e427d6fab1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923067"
---
# <span data-ttu-id="5498d-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="5498d-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="5498d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5498d-102">SYNOPSIS</span></span>
<span data-ttu-id="5498d-103">Erstellt eine neue Cacheentität</span><span class="sxs-lookup"><span data-stu-id="5498d-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="5498d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5498d-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5498d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5498d-105">DESCRIPTION</span></span>
<span data-ttu-id="5498d-106">Das Cmdlet **New-AzApiManagementCache** erstellt eine neue Cacheentität im Api-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="5498d-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="5498d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5498d-107">EXAMPLES</span></span>

### <span data-ttu-id="5498d-108">Beispiel 1: Erstellen einer neuen Cacheentität</span><span class="sxs-lookup"><span data-stu-id="5498d-108">Example 1 : Create a new Cache entity</span></span>
```powershell
PS c:\> New-AzApiManagementCache -Context $context -ConnectionString "teamdemo.redis.cache.windows.net:6380,password=xxxxxx+xxxxx=,ssl=True,abortConnect=False" -Description "Team Cache"

CacheId           : centralus
Description       : Team Cache
ConnectionString  : {{5cc19889e6ed3b0524c3f7d3}}
ResourceId        :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsof
                    t.ApiManagement/service/contoso/caches/centralus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="5498d-109">Die Cmdlets erstellen eine neue Cacheentität am Masterspeicherort des Api-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="5498d-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="5498d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5498d-110">PARAMETERS</span></span>

### <span data-ttu-id="5498d-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="5498d-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="5498d-112">Arm ResourceId der Azure Redis Cache-Instanz.</span><span class="sxs-lookup"><span data-stu-id="5498d-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="5498d-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="5498d-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="5498d-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="5498d-114">-CacheId</span></span>
<span data-ttu-id="5498d-115">Bezeichner des neuen Caches.</span><span class="sxs-lookup"><span data-stu-id="5498d-115">Identifier of new cache.</span></span>
<span data-ttu-id="5498d-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="5498d-116">This parameter is optional.</span></span>
<span data-ttu-id="5498d-117">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="5498d-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="5498d-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5498d-118">-ConnectionString</span></span>
<span data-ttu-id="5498d-119">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="5498d-119">Redis Connection String.</span></span>
<span data-ttu-id="5498d-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5498d-120">This parameter is required.</span></span>

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

### <span data-ttu-id="5498d-121">-Context</span><span class="sxs-lookup"><span data-stu-id="5498d-121">-Context</span></span>
<span data-ttu-id="5498d-122">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5498d-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5498d-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5498d-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5498d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5498d-124">-DefaultProfile</span></span>
<span data-ttu-id="5498d-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5498d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5498d-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5498d-126">-Description</span></span>
<span data-ttu-id="5498d-127">Cachebeschreibung.</span><span class="sxs-lookup"><span data-stu-id="5498d-127">Cache Description.</span></span>
<span data-ttu-id="5498d-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="5498d-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="5498d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5498d-129">-Confirm</span></span>
<span data-ttu-id="5498d-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5498d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5498d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5498d-131">-WhatIf</span></span>
<span data-ttu-id="5498d-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5498d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5498d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5498d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5498d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5498d-134">CommonParameters</span></span>
<span data-ttu-id="5498d-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5498d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5498d-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5498d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5498d-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5498d-137">INPUTS</span></span>

### <span data-ttu-id="5498d-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5498d-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5498d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5498d-139">System.String</span></span>

## <span data-ttu-id="5498d-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5498d-140">OUTPUTS</span></span>

### <span data-ttu-id="5498d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="5498d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="5498d-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5498d-142">NOTES</span></span>

## <span data-ttu-id="5498d-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5498d-143">RELATED LINKS</span></span>

[<span data-ttu-id="5498d-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="5498d-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="5498d-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="5498d-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="5498d-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="5498d-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
