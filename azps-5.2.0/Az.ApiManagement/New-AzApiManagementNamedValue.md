---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300712"
---
# <span data-ttu-id="9abf4-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="9abf4-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="9abf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9abf4-102">SYNOPSIS</span></span>
<span data-ttu-id="9abf4-103">Erstellt einen neuen benannten Wert.</span><span class="sxs-lookup"><span data-stu-id="9abf4-103">Creates new Named Value.</span></span>

## <span data-ttu-id="9abf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9abf4-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9abf4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9abf4-105">DESCRIPTION</span></span>
<span data-ttu-id="9abf4-106">Das **Cmdlet "New-AzApiManagementNamedValue"** erstellt ein Azure API Management **Named Value.**</span><span class="sxs-lookup"><span data-stu-id="9abf4-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="9abf4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9abf4-107">EXAMPLES</span></span>

### <span data-ttu-id="9abf4-108">Beispiel 1: Erstellen eines benannten Werts, der Tags enthält</span><span class="sxs-lookup"><span data-stu-id="9abf4-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="9abf4-109">Der erste Befehl weist der Variablen $Tags Werte zu.</span><span class="sxs-lookup"><span data-stu-id="9abf4-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="9abf4-110">Der zweite Befehl erstellt einen benannten Wert und weist die Zeichenfolgen in $Tags als Tags für die Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="9abf4-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="9abf4-111">Beispiel 2: Erstellen eines benannten Werts mit einem geheimen Wert</span><span class="sxs-lookup"><span data-stu-id="9abf4-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="9abf4-112">Mit diesem Befehl wird ein **benannter Wert erstellt,** der einen verschlüsselten Wert hat.</span><span class="sxs-lookup"><span data-stu-id="9abf4-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="9abf4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9abf4-113">PARAMETERS</span></span>

### <span data-ttu-id="9abf4-114">-Context</span><span class="sxs-lookup"><span data-stu-id="9abf4-114">-Context</span></span>
<span data-ttu-id="9abf4-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9abf4-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9abf4-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9abf4-116">This parameter is required.</span></span>

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

### <span data-ttu-id="9abf4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abf4-117">-DefaultProfile</span></span>
<span data-ttu-id="9abf4-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9abf4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9abf4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9abf4-119">-Name</span></span>
<span data-ttu-id="9abf4-120">Der Name des benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="9abf4-120">Name of the named value.</span></span>
<span data-ttu-id="9abf4-121">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9abf4-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="9abf4-122">Sie darf nur Buchstaben, Ziffern, Bindestriche und Unterstriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="9abf4-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="9abf4-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9abf4-123">This parameter is required.</span></span>

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

### <span data-ttu-id="9abf4-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="9abf4-124">-NamedValueId</span></span>
<span data-ttu-id="9abf4-125">Bezeichner eines neuen benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="9abf4-125">Identifier of new named value.</span></span>
<span data-ttu-id="9abf4-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="9abf4-126">This parameter is optional.</span></span>
<span data-ttu-id="9abf4-127">Wenn keine Angabe angegeben wird, wird ein Code generiert.</span><span class="sxs-lookup"><span data-stu-id="9abf4-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="9abf4-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="9abf4-128">-Secret</span></span>
<span data-ttu-id="9abf4-129">Bestimmt, ob der Wert ein geheimer Wert ist und verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9abf4-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="9abf4-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="9abf4-130">This parameter is optional.</span></span>
<span data-ttu-id="9abf4-131">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="9abf4-131">Default Value is false.</span></span>

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

### <span data-ttu-id="9abf4-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="9abf4-132">-Tag</span></span>
<span data-ttu-id="9abf4-133">Tags, die benannten Wert zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9abf4-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="9abf4-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="9abf4-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="9abf4-135">-Value</span><span class="sxs-lookup"><span data-stu-id="9abf4-135">-Value</span></span>
<span data-ttu-id="9abf4-136">Wert des benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="9abf4-136">Value of the named value.</span></span>
<span data-ttu-id="9abf4-137">Kann Richtlinienausdrücke enthalten.</span><span class="sxs-lookup"><span data-stu-id="9abf4-137">Can contain policy expressions.</span></span>
<span data-ttu-id="9abf4-138">Die maximale Länge beträgt 1.000 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9abf4-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="9abf4-139">Er darf nicht leer sein oder nur aus Leerzeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="9abf4-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="9abf4-140">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9abf4-140">This parameter is required.</span></span>

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

### <span data-ttu-id="9abf4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9abf4-141">-Confirm</span></span>
<span data-ttu-id="9abf4-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9abf4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9abf4-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9abf4-143">-WhatIf</span></span>
<span data-ttu-id="9abf4-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9abf4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9abf4-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9abf4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9abf4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abf4-146">CommonParameters</span></span>
<span data-ttu-id="9abf4-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9abf4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abf4-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9abf4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abf4-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9abf4-149">INPUTS</span></span>

### <span data-ttu-id="9abf4-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9abf4-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9abf4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9abf4-151">System.String</span></span>

### <span data-ttu-id="9abf4-152">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9abf4-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9abf4-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9abf4-153">System.String[]</span></span>

## <span data-ttu-id="9abf4-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9abf4-154">OUTPUTS</span></span>

### <span data-ttu-id="9abf4-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="9abf4-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="9abf4-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9abf4-156">NOTES</span></span>

## <span data-ttu-id="9abf4-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9abf4-157">RELATED LINKS</span></span>
