---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398103"
---
# <span data-ttu-id="4c357-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4c357-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="4c357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c357-102">SYNOPSIS</span></span>
<span data-ttu-id="4c357-103">Erstellt eine neue Cacheentität</span><span class="sxs-lookup"><span data-stu-id="4c357-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="4c357-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c357-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c357-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c357-105">DESCRIPTION</span></span>
<span data-ttu-id="4c357-106">Das Cmdlet **"New-AzApiManagementCache"** erstellt eine neue Cacheentität im Api-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="4c357-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="4c357-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4c357-107">EXAMPLES</span></span>

### <span data-ttu-id="4c357-108">Beispiel 1: Erstellen einer neuen Cacheentität</span><span class="sxs-lookup"><span data-stu-id="4c357-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="4c357-109">Die Cmdlets erstellen eine neue Cacheentität am Hauptspeicherort des API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="4c357-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="4c357-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c357-110">PARAMETERS</span></span>

### <span data-ttu-id="4c357-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="4c357-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="4c357-112">Arm ResourceId der Azure Redis Cache-Instanz.</span><span class="sxs-lookup"><span data-stu-id="4c357-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="4c357-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4c357-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="4c357-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="4c357-114">-CacheId</span></span>
<span data-ttu-id="4c357-115">Id des neuen Caches.</span><span class="sxs-lookup"><span data-stu-id="4c357-115">Identifier of new cache.</span></span>
<span data-ttu-id="4c357-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4c357-116">This parameter is optional.</span></span>
<span data-ttu-id="4c357-117">Wenn keine Angabe angegeben wird, wird ein Code generiert.</span><span class="sxs-lookup"><span data-stu-id="4c357-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="4c357-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="4c357-118">-ConnectionString</span></span>
<span data-ttu-id="4c357-119">Redis-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4c357-119">Redis Connection String.</span></span>
<span data-ttu-id="4c357-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4c357-120">This parameter is required.</span></span>

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

### <span data-ttu-id="4c357-121">-Context</span><span class="sxs-lookup"><span data-stu-id="4c357-121">-Context</span></span>
<span data-ttu-id="4c357-122">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4c357-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4c357-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4c357-123">This parameter is required.</span></span>

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

### <span data-ttu-id="4c357-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c357-124">-DefaultProfile</span></span>
<span data-ttu-id="4c357-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c357-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c357-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c357-126">-Description</span></span>
<span data-ttu-id="4c357-127">Cachebeschreibung.</span><span class="sxs-lookup"><span data-stu-id="4c357-127">Cache Description.</span></span>
<span data-ttu-id="4c357-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4c357-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="4c357-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c357-129">-Confirm</span></span>
<span data-ttu-id="4c357-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c357-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c357-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4c357-131">-WhatIf</span></span>
<span data-ttu-id="4c357-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c357-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c357-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c357-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c357-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c357-134">CommonParameters</span></span>
<span data-ttu-id="4c357-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c357-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c357-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c357-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c357-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4c357-137">INPUTS</span></span>

### <span data-ttu-id="4c357-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4c357-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4c357-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4c357-139">System.String</span></span>

## <span data-ttu-id="4c357-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4c357-140">OUTPUTS</span></span>

### <span data-ttu-id="4c357-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4c357-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="4c357-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4c357-142">NOTES</span></span>

## <span data-ttu-id="4c357-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4c357-143">RELATED LINKS</span></span>

[<span data-ttu-id="4c357-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4c357-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="4c357-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4c357-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="4c357-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="4c357-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
