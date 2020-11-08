---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: 38c937de07d4a19a6c2632356c2b9ac58b2b416a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004376"
---
# <span data-ttu-id="2c53c-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2c53c-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="2c53c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c53c-102">SYNOPSIS</span></span>
<span data-ttu-id="2c53c-103">Ändert eine API-Verwaltungseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2c53c-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="2c53c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c53c-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c53c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c53c-105">DESCRIPTION</span></span>
<span data-ttu-id="2c53c-106">Das Cmdlet " **festlegen-AzApiManagementProperty** " ändert eine Azure API-Verwaltungseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2c53c-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="2c53c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c53c-107">EXAMPLES</span></span>

### <span data-ttu-id="2c53c-108">Beispiel 1: Ändern der Tags für eine Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2c53c-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="2c53c-109">Der erste Befehl weist der $Tags Variablen zwei Werte zu.</span><span class="sxs-lookup"><span data-stu-id="2c53c-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="2c53c-110">Der zweite Befehl ändert die Eigenschaft mit der ID Property11.</span><span class="sxs-lookup"><span data-stu-id="2c53c-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="2c53c-111">Der Befehl weist die Zeichenfolgen in $Tags als Tags für die Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="2c53c-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="2c53c-112">Beispiel 2: Ändern einer Eigenschaft, um einen geheimen Wert zu haben</span><span class="sxs-lookup"><span data-stu-id="2c53c-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="2c53c-113">Mit diesem Befehl wird die zu verschlüsselnde Eigenschaft geändert.</span><span class="sxs-lookup"><span data-stu-id="2c53c-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="2c53c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c53c-114">PARAMETERS</span></span>

### <span data-ttu-id="2c53c-115">-Context</span><span class="sxs-lookup"><span data-stu-id="2c53c-115">-Context</span></span>
<span data-ttu-id="2c53c-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2c53c-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2c53c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c53c-117">-DefaultProfile</span></span>
<span data-ttu-id="2c53c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c53c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c53c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2c53c-119">-Name</span></span>
<span data-ttu-id="2c53c-120">Gibt den Namen der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="2c53c-120">Specifies the name of the property.</span></span>
<span data-ttu-id="2c53c-121">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2c53c-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="2c53c-122">Namen enthalten nur Buchstaben, Ziffern, Punkt Zeichen, Striche und Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="2c53c-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="2c53c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c53c-123">-PassThru</span></span>
<span data-ttu-id="2c53c-124">Gibt an, dass dieses Cmdlet die **PsApiManagementProperty** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2c53c-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2c53c-125">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="2c53c-125">-PropertyId</span></span>
<span data-ttu-id="2c53c-126">Gibt eine ID der Eigenschaft an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2c53c-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2c53c-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="2c53c-127">-Secret</span></span>
<span data-ttu-id="2c53c-128">Gibt an, dass der Eigenschaftswert ein Schlüssel ist und verschlüsselt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="2c53c-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c53c-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="2c53c-129">-Tag</span></span>
<span data-ttu-id="2c53c-130">Einer Eigenschaft zugeordnete Kategorien.</span><span class="sxs-lookup"><span data-stu-id="2c53c-130">Tags associated with a property.</span></span> <span data-ttu-id="2c53c-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="2c53c-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c53c-132">-Wert</span><span class="sxs-lookup"><span data-stu-id="2c53c-132">-Value</span></span>
<span data-ttu-id="2c53c-133">Gibt einen Wert für die Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="2c53c-133">Specifies a value for the property.</span></span>
<span data-ttu-id="2c53c-134">Dieser Wert kann Richtlinienausdrücke enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c53c-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="2c53c-135">Die maximale Länge beträgt 1000 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2c53c-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="2c53c-136">Der Wert darf nicht leer sein oder nur aus Leerzeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="2c53c-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="2c53c-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2c53c-137">-Confirm</span></span>
<span data-ttu-id="2c53c-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c53c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c53c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c53c-139">-WhatIf</span></span>
<span data-ttu-id="2c53c-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c53c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c53c-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c53c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c53c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c53c-142">CommonParameters</span></span>
<span data-ttu-id="2c53c-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c53c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c53c-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c53c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c53c-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c53c-145">INPUTS</span></span>

### <span data-ttu-id="2c53c-146">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2c53c-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2c53c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2c53c-147">System.String</span></span>

### <span data-ttu-id="2c53c-148">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2c53c-148">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2c53c-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="2c53c-149">System.String[]</span></span>

### <span data-ttu-id="2c53c-150">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="2c53c-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2c53c-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c53c-151">OUTPUTS</span></span>

### <span data-ttu-id="2c53c-152">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2c53c-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="2c53c-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c53c-153">NOTES</span></span>

## <span data-ttu-id="2c53c-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c53c-154">RELATED LINKS</span></span>

[<span data-ttu-id="2c53c-155">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2c53c-155">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="2c53c-156">Neu – AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2c53c-156">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="2c53c-157">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2c53c-157">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


