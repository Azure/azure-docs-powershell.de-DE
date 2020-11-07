---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 4ff48709b02cdd0270c559ea8be2f4e269dbce2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662200"
---
# <span data-ttu-id="eca73-101">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="eca73-101">Remove-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="eca73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eca73-102">SYNOPSIS</span></span>
<span data-ttu-id="eca73-103">Entfernt einen bestimmten API-Versions Satz</span><span class="sxs-lookup"><span data-stu-id="eca73-103">Removes a particular Api Version Set</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eca73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eca73-104">SYNTAX</span></span>

### <span data-ttu-id="eca73-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="eca73-105">ExpandedParameter (Default)</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca73-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eca73-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eca73-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eca73-107">DESCRIPTION</span></span>

<span data-ttu-id="eca73-108">Das Cmdlet **Remove-AzureRmApiManagementApiVersionSet** entfernt eine vorhandene API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="eca73-108">The **Remove-AzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="eca73-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eca73-109">EXAMPLES</span></span>

### <span data-ttu-id="eca73-110">Beispiel 1: Entfernen einer API-Versionsgruppe</span><span class="sxs-lookup"><span data-stu-id="eca73-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="eca73-111">Dieser Befehl entfernt die API-Versionsgruppe mit dem angegebenen ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="eca73-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="eca73-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eca73-112">PARAMETERS</span></span>

### <span data-ttu-id="eca73-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="eca73-113">-ApiVersionSetId</span></span>
<span data-ttu-id="eca73-114">Bezeichner der API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="eca73-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="eca73-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eca73-115">This parameter is required.</span></span>

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

### <span data-ttu-id="eca73-116">-Context</span><span class="sxs-lookup"><span data-stu-id="eca73-116">-Context</span></span>
<span data-ttu-id="eca73-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="eca73-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="eca73-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eca73-118">This parameter is required.</span></span>

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

### <span data-ttu-id="eca73-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca73-119">-DefaultProfile</span></span>
<span data-ttu-id="eca73-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eca73-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eca73-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eca73-121">-InputObject</span></span>
<span data-ttu-id="eca73-122">Instanz von PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="eca73-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="eca73-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eca73-123">This parameter is required.</span></span>

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

### <span data-ttu-id="eca73-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eca73-124">-PassThru</span></span>
<span data-ttu-id="eca73-125">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="eca73-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="eca73-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="eca73-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="eca73-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eca73-127">-Confirm</span></span>
<span data-ttu-id="eca73-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eca73-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca73-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca73-129">-WhatIf</span></span>
<span data-ttu-id="eca73-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eca73-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eca73-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eca73-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca73-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca73-132">CommonParameters</span></span>
<span data-ttu-id="eca73-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca73-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca73-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eca73-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca73-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eca73-135">INPUTS</span></span>

### <span data-ttu-id="eca73-136">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eca73-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="eca73-137">Parameter: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eca73-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="eca73-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="eca73-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="eca73-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eca73-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="eca73-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eca73-140">System.String</span></span>

## <span data-ttu-id="eca73-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eca73-141">OUTPUTS</span></span>

### <span data-ttu-id="eca73-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eca73-142">System.Boolean</span></span>

## <span data-ttu-id="eca73-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="eca73-143">NOTES</span></span>

## <span data-ttu-id="eca73-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eca73-144">RELATED LINKS</span></span>

[<span data-ttu-id="eca73-145">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="eca73-145">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="eca73-146">Neu – AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="eca73-146">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="eca73-147">Satz-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="eca73-147">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
