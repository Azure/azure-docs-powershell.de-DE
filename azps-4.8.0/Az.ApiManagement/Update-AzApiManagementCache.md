---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173948"
---
# <span data-ttu-id="0dc71-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0dc71-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="0dc71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0dc71-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc71-103">Aktualisiert einen Cache im API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="0dc71-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="0dc71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dc71-104">SYNTAX</span></span>

### <span data-ttu-id="0dc71-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="0dc71-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc71-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0dc71-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc71-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0dc71-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0dc71-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0dc71-108">DESCRIPTION</span></span>
<span data-ttu-id="0dc71-109">Das Cmdlet **Update-AzApiManagementCache** aktualisiert einen Cache im ApiManagement-Dienst.</span><span class="sxs-lookup"><span data-stu-id="0dc71-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="0dc71-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0dc71-110">EXAMPLES</span></span>

### <span data-ttu-id="0dc71-111">Beispiel 1: aktualisiert die Beschreibung des Caches in centralus</span><span class="sxs-lookup"><span data-stu-id="0dc71-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="0dc71-112">Aktualisiert die Beschreibung des Caches in Central US.</span><span class="sxs-lookup"><span data-stu-id="0dc71-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="0dc71-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dc71-113">PARAMETERS</span></span>

### <span data-ttu-id="0dc71-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="0dc71-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="0dc71-115">Arm-wiederherkunfts-Nr der Azure-Cache-Instanz.</span><span class="sxs-lookup"><span data-stu-id="0dc71-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="0dc71-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0dc71-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="0dc71-117">-Cache-Nr</span><span class="sxs-lookup"><span data-stu-id="0dc71-117">-CacheId</span></span>
<span data-ttu-id="0dc71-118">Bezeichner des neuen Caches.</span><span class="sxs-lookup"><span data-stu-id="0dc71-118">Identifier of new cache.</span></span>
<span data-ttu-id="0dc71-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0dc71-119">This parameter is required.</span></span>

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

### <span data-ttu-id="0dc71-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="0dc71-120">-ConnectionString</span></span>
<span data-ttu-id="0dc71-121">Verbindungszeichenfolge für die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0dc71-121">Redis Connection String.</span></span>
<span data-ttu-id="0dc71-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0dc71-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="0dc71-123">-Context</span><span class="sxs-lookup"><span data-stu-id="0dc71-123">-Context</span></span>
<span data-ttu-id="0dc71-124">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0dc71-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0dc71-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0dc71-125">This parameter is required.</span></span>

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

### <span data-ttu-id="0dc71-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc71-126">-DefaultProfile</span></span>
<span data-ttu-id="0dc71-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0dc71-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dc71-128">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0dc71-128">-Description</span></span>
<span data-ttu-id="0dc71-129">Cache Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="0dc71-129">Cache Description.</span></span>
<span data-ttu-id="0dc71-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0dc71-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="0dc71-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0dc71-131">-InputObject</span></span>
<span data-ttu-id="0dc71-132">Instanz von PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="0dc71-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="0dc71-133">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0dc71-133">This parameter is required.</span></span>

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

### <span data-ttu-id="0dc71-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dc71-134">-PassThru</span></span>
<span data-ttu-id="0dc71-135">Wenn angegeben, wird Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCache-Typs, der den geänderten Cache darstellt, in die Ausgabe geschrieben.</span><span class="sxs-lookup"><span data-stu-id="0dc71-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="0dc71-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0dc71-136">-ResourceId</span></span>
<span data-ttu-id="0dc71-137">Arm-Cache-Speicher.</span><span class="sxs-lookup"><span data-stu-id="0dc71-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="0dc71-138">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0dc71-138">This parameter is required.</span></span>

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

### <span data-ttu-id="0dc71-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0dc71-139">-Confirm</span></span>
<span data-ttu-id="0dc71-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dc71-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dc71-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dc71-141">-WhatIf</span></span>
<span data-ttu-id="0dc71-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0dc71-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dc71-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dc71-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dc71-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc71-144">CommonParameters</span></span>
<span data-ttu-id="0dc71-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc71-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc71-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0dc71-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc71-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0dc71-147">INPUTS</span></span>

### <span data-ttu-id="0dc71-148">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0dc71-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0dc71-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0dc71-149">System.String</span></span>

### <span data-ttu-id="0dc71-150">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0dc71-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="0dc71-151">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="0dc71-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0dc71-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0dc71-152">OUTPUTS</span></span>

### <span data-ttu-id="0dc71-153">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0dc71-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="0dc71-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="0dc71-154">NOTES</span></span>

## <span data-ttu-id="0dc71-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0dc71-155">RELATED LINKS</span></span>

[<span data-ttu-id="0dc71-156">Neu – AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0dc71-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="0dc71-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0dc71-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="0dc71-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="0dc71-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
