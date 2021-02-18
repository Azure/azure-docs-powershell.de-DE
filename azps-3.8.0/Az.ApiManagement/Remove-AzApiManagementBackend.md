---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 073b32936be1e1614e495ca680a250498742ba66
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414593"
---
# <span data-ttu-id="347f2-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="347f2-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="347f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="347f2-102">SYNOPSIS</span></span>
<span data-ttu-id="347f2-103">Entfernt ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="347f2-103">Removes a Backend.</span></span>

## <span data-ttu-id="347f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="347f2-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="347f2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="347f2-105">DESCRIPTION</span></span>
<span data-ttu-id="347f2-106">Entfernt ein Back-End, das durch den Bezeichner aus der Api-Verwaltung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="347f2-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="347f2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="347f2-107">EXAMPLES</span></span>

### <span data-ttu-id="347f2-108">Beispiel 1: Entfernen des Backends 123</span><span class="sxs-lookup"><span data-stu-id="347f2-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="347f2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="347f2-109">PARAMETERS</span></span>

### <span data-ttu-id="347f2-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="347f2-110">-BackendId</span></span>
<span data-ttu-id="347f2-111">Bezeichner des vorhandenen Backends.</span><span class="sxs-lookup"><span data-stu-id="347f2-111">Identifier of existing backend.</span></span>
<span data-ttu-id="347f2-112">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="347f2-112">This parameter is required.</span></span>

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

### <span data-ttu-id="347f2-113">-Context</span><span class="sxs-lookup"><span data-stu-id="347f2-113">-Context</span></span>
<span data-ttu-id="347f2-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="347f2-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="347f2-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="347f2-115">This parameter is required.</span></span>

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

### <span data-ttu-id="347f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="347f2-116">-DefaultProfile</span></span>
<span data-ttu-id="347f2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="347f2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="347f2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="347f2-118">-PassThru</span></span>
<span data-ttu-id="347f2-119">Wenn angegeben, wird "true" für den Fall geschrieben, dass der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="347f2-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="347f2-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="347f2-120">This parameter is optional.</span></span>
<span data-ttu-id="347f2-121">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="347f2-121">Default value is false.</span></span>

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

### <span data-ttu-id="347f2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="347f2-122">-Confirm</span></span>
<span data-ttu-id="347f2-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="347f2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="347f2-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="347f2-124">-WhatIf</span></span>
<span data-ttu-id="347f2-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="347f2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="347f2-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="347f2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="347f2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="347f2-127">CommonParameters</span></span>
<span data-ttu-id="347f2-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="347f2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="347f2-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="347f2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="347f2-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="347f2-130">INPUTS</span></span>

### <span data-ttu-id="347f2-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="347f2-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="347f2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="347f2-132">System.String</span></span>

### <span data-ttu-id="347f2-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="347f2-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="347f2-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="347f2-134">OUTPUTS</span></span>

### <span data-ttu-id="347f2-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="347f2-135">System.Boolean</span></span>

## <span data-ttu-id="347f2-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="347f2-136">NOTES</span></span>

## <span data-ttu-id="347f2-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="347f2-137">RELATED LINKS</span></span>

[<span data-ttu-id="347f2-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="347f2-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="347f2-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="347f2-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="347f2-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="347f2-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="347f2-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="347f2-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="347f2-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="347f2-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
