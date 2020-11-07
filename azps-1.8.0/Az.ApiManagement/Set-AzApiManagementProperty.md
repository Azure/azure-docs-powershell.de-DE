---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: b12a904be944b4a6338ad0bf34a4c906382cb910
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820975"
---
# <span data-ttu-id="b565b-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b565b-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="b565b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b565b-102">SYNOPSIS</span></span>
<span data-ttu-id="b565b-103">Ändert eine API-Verwaltungseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b565b-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="b565b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b565b-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b565b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b565b-105">DESCRIPTION</span></span>
<span data-ttu-id="b565b-106">Das Cmdlet " **festlegen-AzApiManagementProperty** " ändert eine Azure API-Verwaltungseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b565b-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="b565b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b565b-107">EXAMPLES</span></span>

### <span data-ttu-id="b565b-108">Beispiel 1: Ändern der Tags für eine Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b565b-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="b565b-109">Der erste Befehl weist der $Tags Variablen zwei Werte zu.</span><span class="sxs-lookup"><span data-stu-id="b565b-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="b565b-110">Der zweite Befehl ändert die Eigenschaft mit der ID Property11.</span><span class="sxs-lookup"><span data-stu-id="b565b-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="b565b-111">Der Befehl weist die Zeichenfolgen in $Tags als Tags für die Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="b565b-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="b565b-112">Beispiel 2: Ändern einer Eigenschaft, um einen geheimen Wert zu haben</span><span class="sxs-lookup"><span data-stu-id="b565b-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="b565b-113">Mit diesem Befehl wird die zu verschlüsselnde Eigenschaft geändert.</span><span class="sxs-lookup"><span data-stu-id="b565b-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="b565b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b565b-114">PARAMETERS</span></span>

### <span data-ttu-id="b565b-115">-Context</span><span class="sxs-lookup"><span data-stu-id="b565b-115">-Context</span></span>
<span data-ttu-id="b565b-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b565b-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b565b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b565b-117">-DefaultProfile</span></span>
<span data-ttu-id="b565b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b565b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b565b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b565b-119">-Name</span></span>
<span data-ttu-id="b565b-120">Gibt den Namen der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="b565b-120">Specifies the name of the property.</span></span>
<span data-ttu-id="b565b-121">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b565b-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="b565b-122">Namen enthalten nur Buchstaben, Ziffern, Punkt Zeichen, Striche und Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="b565b-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="b565b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b565b-123">-PassThru</span></span>
<span data-ttu-id="b565b-124">Gibt an, dass dieses Cmdlet die **PsApiManagementProperty** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b565b-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b565b-125">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="b565b-125">-PropertyId</span></span>
<span data-ttu-id="b565b-126">Gibt eine ID der Eigenschaft an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b565b-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b565b-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="b565b-127">-Secret</span></span>
<span data-ttu-id="b565b-128">Gibt an, dass der Eigenschaftswert ein Schlüssel ist und verschlüsselt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="b565b-128">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="b565b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="b565b-129">-Tag</span></span>
<span data-ttu-id="b565b-130">Einer Eigenschaft zugeordnete Kategorien.</span><span class="sxs-lookup"><span data-stu-id="b565b-130">Tags associated with a property.</span></span> <span data-ttu-id="b565b-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="b565b-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="b565b-132">-Wert</span><span class="sxs-lookup"><span data-stu-id="b565b-132">-Value</span></span>
<span data-ttu-id="b565b-133">Gibt einen Wert für die Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="b565b-133">Specifies a value for the property.</span></span>
<span data-ttu-id="b565b-134">Dieser Wert kann Richtlinienausdrücke enthalten.</span><span class="sxs-lookup"><span data-stu-id="b565b-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="b565b-135">Die maximale Länge beträgt 1000 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b565b-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="b565b-136">Der Wert darf nicht leer sein oder nur aus Leerzeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="b565b-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="b565b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b565b-137">CommonParameters</span></span>
<span data-ttu-id="b565b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b565b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b565b-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b565b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b565b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b565b-140">INPUTS</span></span>

### <span data-ttu-id="b565b-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b565b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b565b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b565b-142">System.String</span></span>

### <span data-ttu-id="b565b-143">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b565b-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b565b-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="b565b-144">System.String[]</span></span>

### <span data-ttu-id="b565b-145">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="b565b-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b565b-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b565b-146">OUTPUTS</span></span>

### <span data-ttu-id="b565b-147">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b565b-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="b565b-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="b565b-148">NOTES</span></span>

## <span data-ttu-id="b565b-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b565b-149">RELATED LINKS</span></span>

[<span data-ttu-id="b565b-150">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b565b-150">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="b565b-151">Neu – AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b565b-151">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="b565b-152">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b565b-152">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


