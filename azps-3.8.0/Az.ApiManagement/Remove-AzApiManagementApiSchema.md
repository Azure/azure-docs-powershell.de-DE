---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: fb144bfa228b07501c374f054970d1e3e0337ec1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005275"
---
# <span data-ttu-id="a82a4-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a82a4-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="a82a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a82a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a82a4-103">Entfernt das API-Schema aus der API.</span><span class="sxs-lookup"><span data-stu-id="a82a4-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="a82a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a82a4-104">SYNTAX</span></span>

### <span data-ttu-id="a82a4-105">ByApiSchemaId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a82a4-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a82a4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a82a4-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a82a4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a82a4-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a82a4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a82a4-108">DESCRIPTION</span></span>
<span data-ttu-id="a82a4-109">Das Cmdlet **Remove-AzApiManagementSchema** aus der API.</span><span class="sxs-lookup"><span data-stu-id="a82a4-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="a82a4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a82a4-110">EXAMPLES</span></span>

### <span data-ttu-id="a82a4-111">Beispiel 1: entfernt das API-Schema aus der API</span><span class="sxs-lookup"><span data-stu-id="a82a4-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="a82a4-112">Das Skript entfernt das Schema `2` aus der API `echo-api` , wenn nicht darauf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a82a4-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="a82a4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a82a4-113">PARAMETERS</span></span>

### <span data-ttu-id="a82a4-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a82a4-114">-ApiId</span></span>
<span data-ttu-id="a82a4-115">Bezeichner der API.</span><span class="sxs-lookup"><span data-stu-id="a82a4-115">Identifier of the API.</span></span>
<span data-ttu-id="a82a4-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a82a4-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82a4-117">-Context</span><span class="sxs-lookup"><span data-stu-id="a82a4-117">-Context</span></span>
<span data-ttu-id="a82a4-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a82a4-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a82a4-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a82a4-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a82a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a82a4-120">-DefaultProfile</span></span>
<span data-ttu-id="a82a4-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a82a4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a82a4-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a82a4-122">-InputObject</span></span>
<span data-ttu-id="a82a4-123">Instanz von PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="a82a4-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="a82a4-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a82a4-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a82a4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a82a4-125">-PassThru</span></span>
<span data-ttu-id="a82a4-126">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a82a4-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="a82a4-127">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a82a4-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="a82a4-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a82a4-128">-ResourceId</span></span>
<span data-ttu-id="a82a4-129">Arm-ApiSchema.</span><span class="sxs-lookup"><span data-stu-id="a82a4-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="a82a4-130">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a82a4-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82a4-131">-Schema-Nr</span><span class="sxs-lookup"><span data-stu-id="a82a4-131">-SchemaId</span></span>
<span data-ttu-id="a82a4-132">Bezeichner des API-Schemas.</span><span class="sxs-lookup"><span data-stu-id="a82a4-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="a82a4-133">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a82a4-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82a4-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a82a4-134">-Confirm</span></span>
<span data-ttu-id="a82a4-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a82a4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a82a4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a82a4-136">-WhatIf</span></span>
<span data-ttu-id="a82a4-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a82a4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a82a4-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a82a4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a82a4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a82a4-139">CommonParameters</span></span>
<span data-ttu-id="a82a4-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a82a4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a82a4-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a82a4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a82a4-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a82a4-142">INPUTS</span></span>

### <span data-ttu-id="a82a4-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a82a4-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a82a4-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a82a4-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="a82a4-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a82a4-145">System.String</span></span>

## <span data-ttu-id="a82a4-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a82a4-146">OUTPUTS</span></span>

### <span data-ttu-id="a82a4-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a82a4-147">System.Boolean</span></span>

## <span data-ttu-id="a82a4-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="a82a4-148">NOTES</span></span>

## <span data-ttu-id="a82a4-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a82a4-149">RELATED LINKS</span></span>

[<span data-ttu-id="a82a4-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a82a4-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="a82a4-151">Neu – AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a82a4-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="a82a4-152">Satz-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="a82a4-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
