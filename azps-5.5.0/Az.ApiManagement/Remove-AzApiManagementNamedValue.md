---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166961"
---
# <span data-ttu-id="15db9-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="15db9-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="15db9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15db9-102">SYNOPSIS</span></span>
<span data-ttu-id="15db9-103">Entfernt einen benannten API-Verwaltungswert.</span><span class="sxs-lookup"><span data-stu-id="15db9-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="15db9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15db9-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15db9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15db9-105">DESCRIPTION</span></span>
<span data-ttu-id="15db9-106">Das **Cmdlet "Remove-AzApiManagementNamedValue"** entfernt einen azure API Management **Named Value.**</span><span class="sxs-lookup"><span data-stu-id="15db9-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="15db9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15db9-107">EXAMPLES</span></span>

### <span data-ttu-id="15db9-108">Beispiel 1: Entfernen des benannten Werts</span><span class="sxs-lookup"><span data-stu-id="15db9-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="15db9-109">Mit diesem Befehl wird der benannte Wert entfernt, der die ID Property11 hat.</span><span class="sxs-lookup"><span data-stu-id="15db9-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="15db9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15db9-110">PARAMETERS</span></span>

### <span data-ttu-id="15db9-111">-Context</span><span class="sxs-lookup"><span data-stu-id="15db9-111">-Context</span></span>
<span data-ttu-id="15db9-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="15db9-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="15db9-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="15db9-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15db9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15db9-114">-DefaultProfile</span></span>
<span data-ttu-id="15db9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15db9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15db9-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="15db9-116">-NamedValueId</span></span>
<span data-ttu-id="15db9-117">Bezeichner eines vorhandenen benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="15db9-117">Identifier of existing named value.</span></span>
<span data-ttu-id="15db9-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="15db9-118">This parameter is required.</span></span>

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

### <span data-ttu-id="15db9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15db9-119">-PassThru</span></span>
<span data-ttu-id="15db9-120">Wenn angegeben, wird "true" für den Fall geschrieben, dass der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="15db9-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="15db9-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="15db9-121">This parameter is optional.</span></span>
<span data-ttu-id="15db9-122">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="15db9-122">Default value is false.</span></span>

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

### <span data-ttu-id="15db9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15db9-123">-Confirm</span></span>
<span data-ttu-id="15db9-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15db9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15db9-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="15db9-125">-WhatIf</span></span>
<span data-ttu-id="15db9-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15db9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15db9-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15db9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15db9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15db9-128">CommonParameters</span></span>
<span data-ttu-id="15db9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15db9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15db9-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15db9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15db9-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15db9-131">INPUTS</span></span>

### <span data-ttu-id="15db9-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="15db9-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="15db9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="15db9-133">System.String</span></span>

### <span data-ttu-id="15db9-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="15db9-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15db9-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15db9-135">OUTPUTS</span></span>

### <span data-ttu-id="15db9-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="15db9-136">System.Boolean</span></span>

## <span data-ttu-id="15db9-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="15db9-137">NOTES</span></span>

## <span data-ttu-id="15db9-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="15db9-138">RELATED LINKS</span></span>
