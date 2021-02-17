---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 263e54adc39103a704dc4ea0bd30f396b5d00fc9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413607"
---
# <span data-ttu-id="92b00-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="92b00-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="92b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92b00-102">SYNOPSIS</span></span>
<span data-ttu-id="92b00-103">Erstellt eine API-Version einer API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="92b00-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="92b00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92b00-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92b00-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92b00-105">DESCRIPTION</span></span>

<span data-ttu-id="92b00-106">Das **Cmdlet "New-AzApiManagementApiRelease"** erstellt eine API-Version für eine API-Revision im API-Verwaltungskontext.</span><span class="sxs-lookup"><span data-stu-id="92b00-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="92b00-107">Eine Version wird verwendet, um die Api-Überarbeitung als aktuelle Revision an vorn zu stellen.</span><span class="sxs-lookup"><span data-stu-id="92b00-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="92b00-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92b00-108">EXAMPLES</span></span>

### <span data-ttu-id="92b00-109">Beispiel 1: Erstellen einer API-Version für eine API-Überarbeitung</span><span class="sxs-lookup"><span data-stu-id="92b00-109">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


ReleaseId         : 7e4d3fbb43c146c4bf406499ef9411f4
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 1:16:29 AM
UpdatedDateTime   : 5/17/2018 1:16:29 AM
Notes             : Releasing version 6
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/7e4d3fbb43c146c4bf40649
                    9ef9411f4
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="92b00-110">Mit diesem Befehl wird eine API Release of Revision `2` der `echo-api` erstellt.</span><span class="sxs-lookup"><span data-stu-id="92b00-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="92b00-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92b00-111">PARAMETERS</span></span>

### <span data-ttu-id="92b00-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="92b00-112">-ApiId</span></span>
<span data-ttu-id="92b00-113">Id für neue API.</span><span class="sxs-lookup"><span data-stu-id="92b00-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="92b00-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="92b00-114">-ApiRevision</span></span>
<span data-ttu-id="92b00-115">Bezeichner für die Api-Revision.</span><span class="sxs-lookup"><span data-stu-id="92b00-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="92b00-116">-Context</span><span class="sxs-lookup"><span data-stu-id="92b00-116">-Context</span></span>
<span data-ttu-id="92b00-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="92b00-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="92b00-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="92b00-118">This parameter is required.</span></span>

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

### <span data-ttu-id="92b00-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b00-119">-DefaultProfile</span></span>
<span data-ttu-id="92b00-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92b00-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92b00-121">-Note</span><span class="sxs-lookup"><span data-stu-id="92b00-121">-Note</span></span>
<span data-ttu-id="92b00-122">Api-Versionshinweise.</span><span class="sxs-lookup"><span data-stu-id="92b00-122">Api Release Notes.</span></span> <span data-ttu-id="92b00-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="92b00-123">This parameter is optional</span></span>

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

### <span data-ttu-id="92b00-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="92b00-124">-ReleaseId</span></span>
<span data-ttu-id="92b00-125">Bezeichner für die API-Version.</span><span class="sxs-lookup"><span data-stu-id="92b00-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="92b00-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="92b00-126">This parameter is optional.</span></span>
<span data-ttu-id="92b00-127">Wenn kein Bezeichner angegeben ist, wird ein Bezeichner generiert.</span><span class="sxs-lookup"><span data-stu-id="92b00-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="92b00-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92b00-128">-Confirm</span></span>
<span data-ttu-id="92b00-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92b00-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b00-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="92b00-130">-WhatIf</span></span>
<span data-ttu-id="92b00-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92b00-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92b00-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92b00-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b00-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b00-133">CommonParameters</span></span>
<span data-ttu-id="92b00-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b00-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b00-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92b00-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b00-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92b00-136">INPUTS</span></span>

### <span data-ttu-id="92b00-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="92b00-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="92b00-138">System.String</span><span class="sxs-lookup"><span data-stu-id="92b00-138">System.String</span></span>

## <span data-ttu-id="92b00-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92b00-139">OUTPUTS</span></span>

### <span data-ttu-id="92b00-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="92b00-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="92b00-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="92b00-141">NOTES</span></span>

## <span data-ttu-id="92b00-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="92b00-142">RELATED LINKS</span></span>

[<span data-ttu-id="92b00-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="92b00-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="92b00-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="92b00-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="92b00-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="92b00-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)