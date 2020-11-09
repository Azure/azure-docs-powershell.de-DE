---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302199"
---
# <span data-ttu-id="cdedd-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="cdedd-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="cdedd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cdedd-102">SYNOPSIS</span></span>
<span data-ttu-id="cdedd-103">Entfernt die Cache Entität.</span><span class="sxs-lookup"><span data-stu-id="cdedd-103">Removes the cache entity.</span></span>

## <span data-ttu-id="cdedd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdedd-104">SYNTAX</span></span>

### <span data-ttu-id="cdedd-105">ContextParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cdedd-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdedd-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdedd-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdedd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdedd-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdedd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdedd-108">DESCRIPTION</span></span>
<span data-ttu-id="cdedd-109">Das Cmdlet **Remove-AzApiManagementCache** entfernt die Cache Entität.</span><span class="sxs-lookup"><span data-stu-id="cdedd-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="cdedd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdedd-110">EXAMPLES</span></span>

### <span data-ttu-id="cdedd-111">Beispiel 1: Entfernen der Cache Entität</span><span class="sxs-lookup"><span data-stu-id="cdedd-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="cdedd-112">Mit diesem Cmdlet wird der Cache `centralus` vom API-Verwaltungsdienst entfernt.</span><span class="sxs-lookup"><span data-stu-id="cdedd-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="cdedd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdedd-113">PARAMETERS</span></span>

### <span data-ttu-id="cdedd-114">-Cache-Nr</span><span class="sxs-lookup"><span data-stu-id="cdedd-114">-CacheId</span></span>
<span data-ttu-id="cdedd-115">Bezeichner der vorhandenen Cache-ID.</span><span class="sxs-lookup"><span data-stu-id="cdedd-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="cdedd-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cdedd-116">This parameter is required.</span></span>

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

### <span data-ttu-id="cdedd-117">-Context</span><span class="sxs-lookup"><span data-stu-id="cdedd-117">-Context</span></span>
<span data-ttu-id="cdedd-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cdedd-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cdedd-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cdedd-119">This parameter is required.</span></span>

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

### <span data-ttu-id="cdedd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdedd-120">-DefaultProfile</span></span>
<span data-ttu-id="cdedd-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cdedd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdedd-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cdedd-122">-InputObject</span></span>
<span data-ttu-id="cdedd-123">Instanz von PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="cdedd-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="cdedd-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cdedd-124">This parameter is required.</span></span>

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

### <span data-ttu-id="cdedd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdedd-125">-PassThru</span></span>
<span data-ttu-id="cdedd-126">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cdedd-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="cdedd-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="cdedd-127">This parameter is optional.</span></span>
<span data-ttu-id="cdedd-128">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="cdedd-128">Default value is false.</span></span>

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

### <span data-ttu-id="cdedd-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cdedd-129">-ResourceId</span></span>
<span data-ttu-id="cdedd-130">Arm-Cache-Speicher.</span><span class="sxs-lookup"><span data-stu-id="cdedd-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="cdedd-131">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cdedd-131">This parameter is required.</span></span>

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

### <span data-ttu-id="cdedd-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cdedd-132">-Confirm</span></span>
<span data-ttu-id="cdedd-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cdedd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdedd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdedd-134">-WhatIf</span></span>
<span data-ttu-id="cdedd-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cdedd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdedd-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cdedd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdedd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdedd-137">CommonParameters</span></span>
<span data-ttu-id="cdedd-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdedd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdedd-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdedd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdedd-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cdedd-140">INPUTS</span></span>

### <span data-ttu-id="cdedd-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cdedd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cdedd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cdedd-142">System.String</span></span>

### <span data-ttu-id="cdedd-143">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="cdedd-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cdedd-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdedd-144">OUTPUTS</span></span>

### <span data-ttu-id="cdedd-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdedd-145">System.Boolean</span></span>

## <span data-ttu-id="cdedd-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="cdedd-146">NOTES</span></span>

## <span data-ttu-id="cdedd-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cdedd-147">RELATED LINKS</span></span>

[<span data-ttu-id="cdedd-148">Neu – AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="cdedd-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="cdedd-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="cdedd-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="cdedd-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="cdedd-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
