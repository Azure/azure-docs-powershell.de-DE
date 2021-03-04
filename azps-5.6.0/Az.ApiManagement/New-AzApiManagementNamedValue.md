---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 43a8d9969668abd96783fd766d4f99edb4b89e19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940648"
---
# <span data-ttu-id="a93ab-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="a93ab-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="a93ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a93ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a93ab-103">Erstellt einen neuen benannten Wert.</span><span class="sxs-lookup"><span data-stu-id="a93ab-103">Creates new Named Value.</span></span>

## <span data-ttu-id="a93ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a93ab-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a93ab-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a93ab-105">DESCRIPTION</span></span>
<span data-ttu-id="a93ab-106">Das **Cmdlet New-AzApiManagementNamedValue** erstellt ein Azure API Management **Named Value**.</span><span class="sxs-lookup"><span data-stu-id="a93ab-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="a93ab-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a93ab-107">EXAMPLES</span></span>

### <span data-ttu-id="a93ab-108">Beispiel 1: Erstellen eines benannten Werts, der Tags enthält</span><span class="sxs-lookup"><span data-stu-id="a93ab-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="a93ab-109">Der erste Befehl weist der Variablen $Tags zu.</span><span class="sxs-lookup"><span data-stu-id="a93ab-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="a93ab-110">Der zweite Befehl erstellt einen benannten Wert und weist die Zeichenfolgen in $Tags als Tags für die -Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="a93ab-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="a93ab-111">Beispiel 2: Erstellen eines benannten Werts mit einem geheimen Wert</span><span class="sxs-lookup"><span data-stu-id="a93ab-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="a93ab-112">Mit diesem Befehl wird ein **benannter Wert erstellt,** der einen verschlüsselten Wert hat.</span><span class="sxs-lookup"><span data-stu-id="a93ab-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="a93ab-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a93ab-113">PARAMETERS</span></span>

### <span data-ttu-id="a93ab-114">-Context</span><span class="sxs-lookup"><span data-stu-id="a93ab-114">-Context</span></span>
<span data-ttu-id="a93ab-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a93ab-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a93ab-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a93ab-116">This parameter is required.</span></span>

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

### <span data-ttu-id="a93ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93ab-117">-DefaultProfile</span></span>
<span data-ttu-id="a93ab-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a93ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a93ab-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a93ab-119">-Name</span></span>
<span data-ttu-id="a93ab-120">Name des benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="a93ab-120">Name of the named value.</span></span>
<span data-ttu-id="a93ab-121">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a93ab-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="a93ab-122">Sie darf nur Buchstaben, Ziffern, Perioden, Gedankenstriche und Unterstriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="a93ab-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="a93ab-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a93ab-123">This parameter is required.</span></span>

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

### <span data-ttu-id="a93ab-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="a93ab-124">-NamedValueId</span></span>
<span data-ttu-id="a93ab-125">Bezeichner des neuen benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="a93ab-125">Identifier of new named value.</span></span>
<span data-ttu-id="a93ab-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a93ab-126">This parameter is optional.</span></span>
<span data-ttu-id="a93ab-127">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="a93ab-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="a93ab-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="a93ab-128">-Secret</span></span>
<span data-ttu-id="a93ab-129">Bestimmt, ob es sich bei dem Wert um einen geheimen Wert handelt, der verschlüsselt werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="a93ab-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="a93ab-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a93ab-130">This parameter is optional.</span></span>
<span data-ttu-id="a93ab-131">Standardwert ist false.</span><span class="sxs-lookup"><span data-stu-id="a93ab-131">Default Value is false.</span></span>

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

### <span data-ttu-id="a93ab-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="a93ab-132">-Tag</span></span>
<span data-ttu-id="a93ab-133">Tags, die dem benannten Wert zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a93ab-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="a93ab-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a93ab-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93ab-135">-Wert</span><span class="sxs-lookup"><span data-stu-id="a93ab-135">-Value</span></span>
<span data-ttu-id="a93ab-136">Wert des benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="a93ab-136">Value of the named value.</span></span>
<span data-ttu-id="a93ab-137">Kann Richtlinienausdrücke enthalten.</span><span class="sxs-lookup"><span data-stu-id="a93ab-137">Can contain policy expressions.</span></span>
<span data-ttu-id="a93ab-138">Die maximale Länge beträgt 1.000 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a93ab-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="a93ab-139">Sie darf nicht leer sein oder nur aus Leerzeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="a93ab-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="a93ab-140">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a93ab-140">This parameter is required.</span></span>

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

### <span data-ttu-id="a93ab-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a93ab-141">-Confirm</span></span>
<span data-ttu-id="a93ab-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a93ab-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a93ab-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a93ab-143">-WhatIf</span></span>
<span data-ttu-id="a93ab-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a93ab-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a93ab-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a93ab-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a93ab-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93ab-146">CommonParameters</span></span>
<span data-ttu-id="a93ab-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93ab-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93ab-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a93ab-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93ab-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a93ab-149">INPUTS</span></span>

### <span data-ttu-id="a93ab-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a93ab-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a93ab-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a93ab-151">System.String</span></span>

### <span data-ttu-id="a93ab-152">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a93ab-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a93ab-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a93ab-153">System.String[]</span></span>

## <span data-ttu-id="a93ab-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a93ab-154">OUTPUTS</span></span>

### <span data-ttu-id="a93ab-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="a93ab-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="a93ab-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a93ab-156">NOTES</span></span>

## <span data-ttu-id="a93ab-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a93ab-157">RELATED LINKS</span></span>
