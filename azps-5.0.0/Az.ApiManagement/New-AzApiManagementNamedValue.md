---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177135"
---
# <span data-ttu-id="04554-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="04554-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="04554-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04554-102">SYNOPSIS</span></span>
<span data-ttu-id="04554-103">Erstellt einen neuen benannten Wert.</span><span class="sxs-lookup"><span data-stu-id="04554-103">Creates new Named Value.</span></span>

## <span data-ttu-id="04554-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04554-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04554-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04554-105">DESCRIPTION</span></span>
<span data-ttu-id="04554-106">Das Cmdlet **New-AzApiManagementNamedValue** erstellt eine Azure API-Verwaltung **mit dem Namen Value**.</span><span class="sxs-lookup"><span data-stu-id="04554-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="04554-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04554-107">EXAMPLES</span></span>

### <span data-ttu-id="04554-108">Beispiel 1: Erstellen eines benannten Werts, der Tags enthält</span><span class="sxs-lookup"><span data-stu-id="04554-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="04554-109">Der erste Befehl weist der $Tags Variablen zwei Werte zu.</span><span class="sxs-lookup"><span data-stu-id="04554-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="04554-110">Der zweite Befehl erstellt einen benannten Wert und weist die Zeichenfolgen in $Tags als Tags für die Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="04554-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="04554-111">Beispiel 2: Erstellen eines benannten Werts, der einen geheimen Wert aufweist</span><span class="sxs-lookup"><span data-stu-id="04554-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="04554-112">Mit diesem Befehl wird ein **benannter Wert** erstellt, der über einen verschlüsselten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="04554-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="04554-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="04554-113">PARAMETERS</span></span>

### <span data-ttu-id="04554-114">-Context</span><span class="sxs-lookup"><span data-stu-id="04554-114">-Context</span></span>
<span data-ttu-id="04554-115">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="04554-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="04554-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="04554-116">This parameter is required.</span></span>

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

### <span data-ttu-id="04554-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04554-117">-DefaultProfile</span></span>
<span data-ttu-id="04554-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="04554-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04554-119">-Name</span><span class="sxs-lookup"><span data-stu-id="04554-119">-Name</span></span>
<span data-ttu-id="04554-120">Der Name des benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="04554-120">Name of the named value.</span></span>
<span data-ttu-id="04554-121">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="04554-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="04554-122">Sie kann nur Buchstaben, Ziffern, Punkt, Strich und Unterstriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="04554-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="04554-123">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="04554-123">This parameter is required.</span></span>

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

### <span data-ttu-id="04554-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="04554-124">-NamedValueId</span></span>
<span data-ttu-id="04554-125">Bezeichner des neuen benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="04554-125">Identifier of new named value.</span></span>
<span data-ttu-id="04554-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="04554-126">This parameter is optional.</span></span>
<span data-ttu-id="04554-127">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="04554-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="04554-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="04554-128">-Secret</span></span>
<span data-ttu-id="04554-129">Bestimmt, ob es sich um einen geheimen Wert handelt, der verschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="04554-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="04554-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="04554-130">This parameter is optional.</span></span>
<span data-ttu-id="04554-131">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="04554-131">Default Value is false.</span></span>

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

### <span data-ttu-id="04554-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="04554-132">-Tag</span></span>
<span data-ttu-id="04554-133">Tags, die mit dem benannten Wert verknüpft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="04554-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="04554-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="04554-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="04554-135">-Wert</span><span class="sxs-lookup"><span data-stu-id="04554-135">-Value</span></span>
<span data-ttu-id="04554-136">Der Wert des benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="04554-136">Value of the named value.</span></span>
<span data-ttu-id="04554-137">Kann Richtlinienausdrücke enthalten.</span><span class="sxs-lookup"><span data-stu-id="04554-137">Can contain policy expressions.</span></span>
<span data-ttu-id="04554-138">Die maximale Länge beträgt 1000 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="04554-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="04554-139">Sie darf nicht leer sein oder nur aus Leerzeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="04554-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="04554-140">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="04554-140">This parameter is required.</span></span>

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

### <span data-ttu-id="04554-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="04554-141">-Confirm</span></span>
<span data-ttu-id="04554-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04554-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04554-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04554-143">-WhatIf</span></span>
<span data-ttu-id="04554-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04554-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04554-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04554-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04554-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04554-146">CommonParameters</span></span>
<span data-ttu-id="04554-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04554-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04554-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04554-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04554-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04554-149">INPUTS</span></span>

### <span data-ttu-id="04554-150">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="04554-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="04554-151">System. String</span><span class="sxs-lookup"><span data-stu-id="04554-151">System.String</span></span>

### <span data-ttu-id="04554-152">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="04554-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="04554-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="04554-153">System.String[]</span></span>

## <span data-ttu-id="04554-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04554-154">OUTPUTS</span></span>

### <span data-ttu-id="04554-155">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="04554-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="04554-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="04554-156">NOTES</span></span>

## <span data-ttu-id="04554-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04554-157">RELATED LINKS</span></span>
