---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178073"
---
# <span data-ttu-id="cb798-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb798-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="cb798-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb798-102">SYNOPSIS</span></span>
<span data-ttu-id="cb798-103">Entfernt einen bestimmten API-Versions Satz</span><span class="sxs-lookup"><span data-stu-id="cb798-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="cb798-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb798-104">SYNTAX</span></span>

### <span data-ttu-id="cb798-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb798-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb798-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb798-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb798-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb798-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb798-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb798-108">DESCRIPTION</span></span>

<span data-ttu-id="cb798-109">Das Cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** entfernt eine vorhandene API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="cb798-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="cb798-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb798-110">EXAMPLES</span></span>

### <span data-ttu-id="cb798-111">Beispiel 1: Entfernen einer API-Versionsgruppe</span><span class="sxs-lookup"><span data-stu-id="cb798-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="cb798-112">Dieser Befehl entfernt die API-Versionsgruppe mit dem angegebenen ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="cb798-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="cb798-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb798-113">PARAMETERS</span></span>

### <span data-ttu-id="cb798-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="cb798-114">-ApiVersionSetId</span></span>
<span data-ttu-id="cb798-115">Bezeichner der API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="cb798-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="cb798-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb798-116">This parameter is required.</span></span>

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

### <span data-ttu-id="cb798-117">-Context</span><span class="sxs-lookup"><span data-stu-id="cb798-117">-Context</span></span>
<span data-ttu-id="cb798-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cb798-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cb798-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb798-119">This parameter is required.</span></span>

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

### <span data-ttu-id="cb798-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb798-120">-DefaultProfile</span></span>
<span data-ttu-id="cb798-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb798-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb798-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cb798-122">-InputObject</span></span>
<span data-ttu-id="cb798-123">Instanz von PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cb798-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="cb798-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb798-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb798-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb798-125">-PassThru</span></span>
<span data-ttu-id="cb798-126">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cb798-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="cb798-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="cb798-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="cb798-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cb798-128">-ResourceId</span></span>
<span data-ttu-id="cb798-129">Arm-ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cb798-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="cb798-130">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb798-130">This parameter is required.</span></span>

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

### <span data-ttu-id="cb798-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cb798-131">-Confirm</span></span>
<span data-ttu-id="cb798-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb798-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb798-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb798-133">-WhatIf</span></span>
<span data-ttu-id="cb798-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb798-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb798-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb798-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb798-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb798-136">CommonParameters</span></span>
<span data-ttu-id="cb798-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb798-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb798-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb798-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb798-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb798-139">INPUTS</span></span>

### <span data-ttu-id="cb798-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cb798-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cb798-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb798-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="cb798-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cb798-142">System.String</span></span>

## <span data-ttu-id="cb798-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb798-143">OUTPUTS</span></span>

### <span data-ttu-id="cb798-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb798-144">System.Boolean</span></span>

## <span data-ttu-id="cb798-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb798-145">NOTES</span></span>

## <span data-ttu-id="cb798-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb798-146">RELATED LINKS</span></span>

[<span data-ttu-id="cb798-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb798-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="cb798-148">Neu – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb798-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="cb798-149">Satz-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="cb798-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)