---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: cb7fbfe4ba4fdf09b9012ddc5be8028af0bd80c1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93506045"
---
# <span data-ttu-id="f2f51-101">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f2f51-101">New-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="f2f51-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2f51-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f51-103">Erstellt eine API-Version einer API-Revision</span><span class="sxs-lookup"><span data-stu-id="f2f51-103">Creates an API Release of an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2f51-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2f51-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2f51-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2f51-105">DESCRIPTION</span></span>

<span data-ttu-id="f2f51-106">Das Cmdlet **New-AzureRmApiManagementApiRelease** erstellt eine API-Version für eine API-Revision im API-Verwaltungskontext.</span><span class="sxs-lookup"><span data-stu-id="f2f51-106">The **New-AzureRmApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="f2f51-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2f51-107">EXAMPLES</span></span>

### <span data-ttu-id="f2f51-108">Beispiel 1: Erstellen einer API-Version für eine API-Revision</span><span class="sxs-lookup"><span data-stu-id="f2f51-108">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


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

<span data-ttu-id="f2f51-109">Dieser Befehl erstellt eine API-Version der Revision `2` von `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="f2f51-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="f2f51-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2f51-110">PARAMETERS</span></span>

### <span data-ttu-id="f2f51-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f2f51-111">-ApiId</span></span>
<span data-ttu-id="f2f51-112">Bezeichner für neue API.</span><span class="sxs-lookup"><span data-stu-id="f2f51-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="f2f51-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f2f51-113">-ApiRevision</span></span>
<span data-ttu-id="f2f51-114">Bezeichner für die API-Revision.</span><span class="sxs-lookup"><span data-stu-id="f2f51-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="f2f51-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f2f51-115">-Context</span></span>
<span data-ttu-id="f2f51-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f2f51-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f2f51-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2f51-117">This parameter is required.</span></span>

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

### <span data-ttu-id="f2f51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f51-118">-DefaultProfile</span></span>
<span data-ttu-id="f2f51-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2f51-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f51-120">-Hinweis</span><span class="sxs-lookup"><span data-stu-id="f2f51-120">-Note</span></span>
<span data-ttu-id="f2f51-121">Anmerkungen zur API-Version.</span><span class="sxs-lookup"><span data-stu-id="f2f51-121">Api Release Notes.</span></span> <span data-ttu-id="f2f51-122">Dieser Parameter ist optional</span><span class="sxs-lookup"><span data-stu-id="f2f51-122">This parameter is optional</span></span>

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

### <span data-ttu-id="f2f51-123">-Veröffentlichungs-Nr</span><span class="sxs-lookup"><span data-stu-id="f2f51-123">-ReleaseId</span></span>
<span data-ttu-id="f2f51-124">Bezeichner für die API-Version.</span><span class="sxs-lookup"><span data-stu-id="f2f51-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="f2f51-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="f2f51-125">This parameter is optional.</span></span>
<span data-ttu-id="f2f51-126">Wenn kein angegebener Bezeichner generiert wird.</span><span class="sxs-lookup"><span data-stu-id="f2f51-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="f2f51-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2f51-127">-Confirm</span></span>
<span data-ttu-id="f2f51-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2f51-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2f51-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2f51-129">-WhatIf</span></span>
<span data-ttu-id="f2f51-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2f51-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2f51-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2f51-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2f51-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f51-132">CommonParameters</span></span>
<span data-ttu-id="f2f51-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f51-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f51-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2f51-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f51-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2f51-135">INPUTS</span></span>

### <span data-ttu-id="f2f51-136">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f2f51-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="f2f51-137">Parameter: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2f51-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="f2f51-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f2f51-138">System.String</span></span>

## <span data-ttu-id="f2f51-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2f51-139">OUTPUTS</span></span>

### <span data-ttu-id="f2f51-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f2f51-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="f2f51-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2f51-141">NOTES</span></span>

## <span data-ttu-id="f2f51-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2f51-142">RELATED LINKS</span></span>

[<span data-ttu-id="f2f51-143">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f2f51-143">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="f2f51-144">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f2f51-144">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="f2f51-145">Satz-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f2f51-145">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
