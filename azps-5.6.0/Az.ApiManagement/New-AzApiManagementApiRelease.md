---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 317d6dd822b1ef465abf4e6315fa39a480248c42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935416"
---
# <span data-ttu-id="a9e1a-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a9e1a-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="a9e1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e1a-103">Erstellt eine API-Version einer API-Überarbeitung</span><span class="sxs-lookup"><span data-stu-id="a9e1a-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="a9e1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9e1a-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9e1a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9e1a-105">DESCRIPTION</span></span>

<span data-ttu-id="a9e1a-106">Das **Cmdlet New-AzApiManagementApiRelease** erstellt eine API-Version für eine API-Überarbeitung im KONTEXT FÜR DIE API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="a9e1a-107">Eine Version wird verwendet, um die Apirevision als aktuelle Revision zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="a9e1a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9e1a-108">EXAMPLES</span></span>

### <span data-ttu-id="a9e1a-109">Beispiel 1: Erstellen einer API-Version für eine API-Überarbeitung</span><span class="sxs-lookup"><span data-stu-id="a9e1a-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="a9e1a-110">Mit diesem Befehl wird eine API Release of Revision `2` von `echo-api` erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="a9e1a-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a9e1a-111">PARAMETERS</span></span>

### <span data-ttu-id="a9e1a-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a9e1a-112">-ApiId</span></span>
<span data-ttu-id="a9e1a-113">Bezeichner für neue API.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="a9e1a-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a9e1a-114">-ApiRevision</span></span>
<span data-ttu-id="a9e1a-115">Bezeichner für die Api-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="a9e1a-116">-Context</span><span class="sxs-lookup"><span data-stu-id="a9e1a-116">-Context</span></span>
<span data-ttu-id="a9e1a-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a9e1a-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a9e1a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e1a-119">-DefaultProfile</span></span>
<span data-ttu-id="a9e1a-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9e1a-121">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="a9e1a-121">-Note</span></span>
<span data-ttu-id="a9e1a-122">Api-Versionshinweise.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-122">Api Release Notes.</span></span> <span data-ttu-id="a9e1a-123">Dieser Parameter ist optional</span><span class="sxs-lookup"><span data-stu-id="a9e1a-123">This parameter is optional</span></span>

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

### <span data-ttu-id="a9e1a-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="a9e1a-124">-ReleaseId</span></span>
<span data-ttu-id="a9e1a-125">Bezeichner für die Api Release.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="a9e1a-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-126">This parameter is optional.</span></span>
<span data-ttu-id="a9e1a-127">Wenn kein bezeichner angegeben wird, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="a9e1a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9e1a-128">-Confirm</span></span>
<span data-ttu-id="a9e1a-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e1a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e1a-130">-WhatIf</span></span>
<span data-ttu-id="a9e1a-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9e1a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e1a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e1a-133">CommonParameters</span></span>
<span data-ttu-id="a9e1a-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e1a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e1a-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9e1a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e1a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9e1a-136">INPUTS</span></span>

### <span data-ttu-id="a9e1a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a9e1a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a9e1a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a9e1a-138">System.String</span></span>

## <span data-ttu-id="a9e1a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9e1a-139">OUTPUTS</span></span>

### <span data-ttu-id="a9e1a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a9e1a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="a9e1a-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a9e1a-141">NOTES</span></span>

## <span data-ttu-id="a9e1a-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a9e1a-142">RELATED LINKS</span></span>

[<span data-ttu-id="a9e1a-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a9e1a-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="a9e1a-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a9e1a-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="a9e1a-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a9e1a-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)