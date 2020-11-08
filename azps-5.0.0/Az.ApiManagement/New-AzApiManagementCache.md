---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179946"
---
# <span data-ttu-id="b51c1-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b51c1-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="b51c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b51c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b51c1-103">Erstellt eine neue Cache Entität</span><span class="sxs-lookup"><span data-stu-id="b51c1-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="b51c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b51c1-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b51c1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b51c1-105">DESCRIPTION</span></span>
<span data-ttu-id="b51c1-106">Das Cmdlet **New-AzApiManagementCache** erstellt im API-Verwaltungsdienst eine neue Cache Entität.</span><span class="sxs-lookup"><span data-stu-id="b51c1-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="b51c1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b51c1-107">EXAMPLES</span></span>

### <span data-ttu-id="b51c1-108">Beispiel 1: Erstellen einer neuen Cache Entität</span><span class="sxs-lookup"><span data-stu-id="b51c1-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="b51c1-109">Die Cmdlets erstellen eine neue Cache Entität am Master Speicherort des API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="b51c1-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="b51c1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b51c1-110">PARAMETERS</span></span>

### <span data-ttu-id="b51c1-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="b51c1-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="b51c1-112">Arm-wiederherkunfts-Nr der Azure-Cache-Instanz.</span><span class="sxs-lookup"><span data-stu-id="b51c1-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="b51c1-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b51c1-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="b51c1-114">-Cache-Nr</span><span class="sxs-lookup"><span data-stu-id="b51c1-114">-CacheId</span></span>
<span data-ttu-id="b51c1-115">Bezeichner des neuen Caches.</span><span class="sxs-lookup"><span data-stu-id="b51c1-115">Identifier of new cache.</span></span>
<span data-ttu-id="b51c1-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b51c1-116">This parameter is optional.</span></span>
<span data-ttu-id="b51c1-117">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="b51c1-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="b51c1-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b51c1-118">-ConnectionString</span></span>
<span data-ttu-id="b51c1-119">Verbindungszeichenfolge für die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b51c1-119">Redis Connection String.</span></span>
<span data-ttu-id="b51c1-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b51c1-120">This parameter is required.</span></span>

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

### <span data-ttu-id="b51c1-121">-Context</span><span class="sxs-lookup"><span data-stu-id="b51c1-121">-Context</span></span>
<span data-ttu-id="b51c1-122">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b51c1-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b51c1-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b51c1-123">This parameter is required.</span></span>

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

### <span data-ttu-id="b51c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b51c1-124">-DefaultProfile</span></span>
<span data-ttu-id="b51c1-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b51c1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b51c1-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b51c1-126">-Description</span></span>
<span data-ttu-id="b51c1-127">Cache Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="b51c1-127">Cache Description.</span></span>
<span data-ttu-id="b51c1-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b51c1-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="b51c1-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b51c1-129">-Confirm</span></span>
<span data-ttu-id="b51c1-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b51c1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b51c1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b51c1-131">-WhatIf</span></span>
<span data-ttu-id="b51c1-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b51c1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b51c1-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b51c1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b51c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b51c1-134">CommonParameters</span></span>
<span data-ttu-id="b51c1-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b51c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b51c1-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b51c1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b51c1-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b51c1-137">INPUTS</span></span>

### <span data-ttu-id="b51c1-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b51c1-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b51c1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b51c1-139">System.String</span></span>

## <span data-ttu-id="b51c1-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b51c1-140">OUTPUTS</span></span>

### <span data-ttu-id="b51c1-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b51c1-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="b51c1-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="b51c1-142">NOTES</span></span>

## <span data-ttu-id="b51c1-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b51c1-143">RELATED LINKS</span></span>

[<span data-ttu-id="b51c1-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b51c1-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="b51c1-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b51c1-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="b51c1-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="b51c1-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
