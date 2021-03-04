---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: 3101f58720130a6e5f7c91fb4489d96915d8c4e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921528"
---
# <span data-ttu-id="a7480-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="a7480-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="a7480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7480-102">SYNOPSIS</span></span>
<span data-ttu-id="a7480-103">Entfernt einen benannten WERT für die API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="a7480-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="a7480-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7480-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7480-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7480-105">DESCRIPTION</span></span>
<span data-ttu-id="a7480-106">Das **Cmdlet Remove-AzApiManagementNamedValue** entfernt ein Azure API Management **Named Value**.</span><span class="sxs-lookup"><span data-stu-id="a7480-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="a7480-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7480-107">EXAMPLES</span></span>

### <span data-ttu-id="a7480-108">Beispiel 1: Entfernen des benannten Werts</span><span class="sxs-lookup"><span data-stu-id="a7480-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="a7480-109">Mit diesem Befehl wird der benannte Wert entfernt, der die ID-Eigenschaft11 hat.</span><span class="sxs-lookup"><span data-stu-id="a7480-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="a7480-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7480-110">PARAMETERS</span></span>

### <span data-ttu-id="a7480-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a7480-111">-Context</span></span>
<span data-ttu-id="a7480-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a7480-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a7480-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7480-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a7480-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7480-114">-DefaultProfile</span></span>
<span data-ttu-id="a7480-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7480-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7480-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="a7480-116">-NamedValueId</span></span>
<span data-ttu-id="a7480-117">Bezeichner des vorhandenen benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="a7480-117">Identifier of existing named value.</span></span>
<span data-ttu-id="a7480-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7480-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a7480-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7480-119">-PassThru</span></span>
<span data-ttu-id="a7480-120">Wenn angegeben wird, wird "true" geschrieben, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a7480-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a7480-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a7480-121">This parameter is optional.</span></span>
<span data-ttu-id="a7480-122">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="a7480-122">Default value is false.</span></span>

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

### <span data-ttu-id="a7480-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7480-123">-Confirm</span></span>
<span data-ttu-id="a7480-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7480-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7480-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7480-125">-WhatIf</span></span>
<span data-ttu-id="a7480-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7480-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7480-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7480-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7480-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7480-128">CommonParameters</span></span>
<span data-ttu-id="a7480-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7480-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7480-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7480-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7480-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7480-131">INPUTS</span></span>

### <span data-ttu-id="a7480-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a7480-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a7480-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a7480-133">System.String</span></span>

### <span data-ttu-id="a7480-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a7480-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a7480-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7480-135">OUTPUTS</span></span>

### <span data-ttu-id="a7480-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7480-136">System.Boolean</span></span>

## <span data-ttu-id="a7480-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7480-137">NOTES</span></span>

## <span data-ttu-id="a7480-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7480-138">RELATED LINKS</span></span>
