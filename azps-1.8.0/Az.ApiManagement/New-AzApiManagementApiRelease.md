---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 5e536d3174a9a71cf4f648172f3d06e6fc5ae79f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400997"
---
# <span data-ttu-id="cb7ce-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cb7ce-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="cb7ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb7ce-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7ce-103">Erstellt eine API-Version einer API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="cb7ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb7ce-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb7ce-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb7ce-105">DESCRIPTION</span></span>

<span data-ttu-id="cb7ce-106">Das **Cmdlet "New-AzApiManagementApiRelease"** erstellt eine API-Version für eine API-Revision im API-Verwaltungskontext.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="cb7ce-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb7ce-107">EXAMPLES</span></span>

### <span data-ttu-id="cb7ce-108">Beispiel 1: Erstellen einer API-Version für eine API-Überarbeitung</span><span class="sxs-lookup"><span data-stu-id="cb7ce-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="cb7ce-109">Mit diesem Befehl wird eine API Release of Revision `2` der `echo-api` erstellt.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="cb7ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb7ce-110">PARAMETERS</span></span>

### <span data-ttu-id="cb7ce-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cb7ce-111">-ApiId</span></span>
<span data-ttu-id="cb7ce-112">Id für neue API.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="cb7ce-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="cb7ce-113">-ApiRevision</span></span>
<span data-ttu-id="cb7ce-114">Bezeichner für die Api-Revision.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="cb7ce-115">-Context</span><span class="sxs-lookup"><span data-stu-id="cb7ce-115">-Context</span></span>
<span data-ttu-id="cb7ce-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cb7ce-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-117">This parameter is required.</span></span>

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

### <span data-ttu-id="cb7ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7ce-118">-DefaultProfile</span></span>
<span data-ttu-id="cb7ce-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb7ce-120">-Note</span><span class="sxs-lookup"><span data-stu-id="cb7ce-120">-Note</span></span>
<span data-ttu-id="cb7ce-121">Api-Versionshinweise.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-121">Api Release Notes.</span></span> <span data-ttu-id="cb7ce-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-122">This parameter is optional</span></span>

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

### <span data-ttu-id="cb7ce-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="cb7ce-123">-ReleaseId</span></span>
<span data-ttu-id="cb7ce-124">Bezeichner für die API-Version.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="cb7ce-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-125">This parameter is optional.</span></span>
<span data-ttu-id="cb7ce-126">Wenn kein Bezeichner angegeben ist, wird ein Bezeichner generiert.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="cb7ce-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb7ce-127">-Confirm</span></span>
<span data-ttu-id="cb7ce-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb7ce-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cb7ce-129">-WhatIf</span></span>
<span data-ttu-id="cb7ce-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb7ce-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb7ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7ce-132">CommonParameters</span></span>
<span data-ttu-id="cb7ce-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb7ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7ce-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb7ce-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7ce-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb7ce-135">INPUTS</span></span>

### <span data-ttu-id="cb7ce-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cb7ce-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cb7ce-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cb7ce-137">System.String</span></span>

## <span data-ttu-id="cb7ce-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb7ce-138">OUTPUTS</span></span>

### <span data-ttu-id="cb7ce-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cb7ce-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="cb7ce-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cb7ce-140">NOTES</span></span>

## <span data-ttu-id="cb7ce-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cb7ce-141">RELATED LINKS</span></span>

[<span data-ttu-id="cb7ce-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cb7ce-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="cb7ce-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cb7ce-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="cb7ce-144">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cb7ce-144">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)