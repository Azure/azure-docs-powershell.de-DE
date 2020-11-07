---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 681ce525d1d00802cc226539fd9c3014c1786098
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821107"
---
# <span data-ttu-id="c3e7c-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c3e7c-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="c3e7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e7c-103">Entfernt einen bestimmten API-Versions Satz</span><span class="sxs-lookup"><span data-stu-id="c3e7c-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="c3e7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3e7c-104">SYNTAX</span></span>

### <span data-ttu-id="c3e7c-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3e7c-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3e7c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c3e7c-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e7c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3e7c-107">DESCRIPTION</span></span>

<span data-ttu-id="c3e7c-108">Das Cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** entfernt eine vorhandene API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-108">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="c3e7c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="c3e7c-110">Beispiel 1: Entfernen einer API-Versionsgruppe</span><span class="sxs-lookup"><span data-stu-id="c3e7c-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="c3e7c-111">Dieser Befehl entfernt die API-Versionsgruppe mit dem angegebenen ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="c3e7c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3e7c-112">PARAMETERS</span></span>

### <span data-ttu-id="c3e7c-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="c3e7c-113">-ApiVersionSetId</span></span>
<span data-ttu-id="c3e7c-114">Bezeichner der API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="c3e7c-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-115">This parameter is required.</span></span>

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

### <span data-ttu-id="c3e7c-116">-Context</span><span class="sxs-lookup"><span data-stu-id="c3e7c-116">-Context</span></span>
<span data-ttu-id="c3e7c-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c3e7c-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c3e7c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e7c-119">-DefaultProfile</span></span>
<span data-ttu-id="c3e7c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e7c-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3e7c-121">-InputObject</span></span>
<span data-ttu-id="c3e7c-122">Instanz von PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="c3e7c-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-123">This parameter is required.</span></span>

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

### <span data-ttu-id="c3e7c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3e7c-124">-PassThru</span></span>
<span data-ttu-id="c3e7c-125">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c3e7c-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="c3e7c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3e7c-127">-Confirm</span></span>
<span data-ttu-id="c3e7c-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e7c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e7c-129">-WhatIf</span></span>
<span data-ttu-id="c3e7c-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e7c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e7c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e7c-132">CommonParameters</span></span>
<span data-ttu-id="c3e7c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e7c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e7c-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e7c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e7c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3e7c-135">INPUTS</span></span>

### <span data-ttu-id="c3e7c-136">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c3e7c-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c3e7c-137">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c3e7c-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="c3e7c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c3e7c-138">System.String</span></span>

## <span data-ttu-id="c3e7c-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3e7c-139">OUTPUTS</span></span>

### <span data-ttu-id="c3e7c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3e7c-140">System.Boolean</span></span>

## <span data-ttu-id="c3e7c-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3e7c-141">NOTES</span></span>

## <span data-ttu-id="c3e7c-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3e7c-142">RELATED LINKS</span></span>

[<span data-ttu-id="c3e7c-143">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c3e7c-143">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c3e7c-144">Neu – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c3e7c-144">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c3e7c-145">Satz-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c3e7c-145">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)