---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 31e2151e5c41a4e4c9d053174f9d598cd16680f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658209"
---
# <span data-ttu-id="a9ca5-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a9ca5-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="a9ca5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ca5-103">Entfernt eine bestimmte API-Version</span><span class="sxs-lookup"><span data-stu-id="a9ca5-103">Removes a particular API Release</span></span>

## <span data-ttu-id="a9ca5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9ca5-104">SYNTAX</span></span>

### <span data-ttu-id="a9ca5-105">ByApiReleaseId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9ca5-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9ca5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a9ca5-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9ca5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9ca5-107">DESCRIPTION</span></span>

<span data-ttu-id="a9ca5-108">Das Cmdlet **Remove-AzAzureRmApiManagementApiRelease** entfernt eine vorhandene API-Version.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="a9ca5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9ca5-109">EXAMPLES</span></span>

### <span data-ttu-id="a9ca5-110">Beispiel 1: Entfernen einer API-Version</span><span class="sxs-lookup"><span data-stu-id="a9ca5-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="a9ca5-111">Mit diesem Befehl wird die API-Version mit dem angegebenen ApiId und der angegebenen Veröffentlichungs-Nr entfernt.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="a9ca5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9ca5-112">PARAMETERS</span></span>

### <span data-ttu-id="a9ca5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a9ca5-113">-ApiId</span></span>
<span data-ttu-id="a9ca5-114">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-114">Identifier of the API.</span></span>
<span data-ttu-id="a9ca5-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ca5-116">-Context</span><span class="sxs-lookup"><span data-stu-id="a9ca5-116">-Context</span></span>
<span data-ttu-id="a9ca5-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a9ca5-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ca5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ca5-119">-DefaultProfile</span></span>
<span data-ttu-id="a9ca5-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9ca5-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9ca5-121">-InputObject</span></span>
<span data-ttu-id="a9ca5-122">Instanz von PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="a9ca5-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ca5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9ca5-124">-PassThru</span></span>
<span data-ttu-id="a9ca5-125">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a9ca5-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9ca5-127">-Veröffentlichungs-Nr</span><span class="sxs-lookup"><span data-stu-id="a9ca5-127">-ReleaseId</span></span>
<span data-ttu-id="a9ca5-128">Bezeichner der API-Version.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-128">Identifier of the API Release.</span></span>
<span data-ttu-id="a9ca5-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ca5-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9ca5-130">-Confirm</span></span>
<span data-ttu-id="a9ca5-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ca5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ca5-132">-WhatIf</span></span>
<span data-ttu-id="a9ca5-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9ca5-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9ca5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ca5-135">CommonParameters</span></span>
<span data-ttu-id="a9ca5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ca5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ca5-137">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9ca5-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ca5-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9ca5-138">INPUTS</span></span>

### <span data-ttu-id="a9ca5-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a9ca5-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a9ca5-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a9ca5-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="a9ca5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a9ca5-141">System.String</span></span>

## <span data-ttu-id="a9ca5-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9ca5-142">OUTPUTS</span></span>

### <span data-ttu-id="a9ca5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9ca5-143">System.Boolean</span></span>

## <span data-ttu-id="a9ca5-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9ca5-144">NOTES</span></span>

## <span data-ttu-id="a9ca5-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9ca5-145">RELATED LINKS</span></span>

[<span data-ttu-id="a9ca5-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a9ca5-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="a9ca5-147">Neu – AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a9ca5-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="a9ca5-148">Satz-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a9ca5-148">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)