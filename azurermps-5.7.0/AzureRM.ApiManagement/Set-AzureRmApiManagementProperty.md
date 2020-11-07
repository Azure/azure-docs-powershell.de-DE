---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 89612136023173d2f725c8c4b286a270400f8c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664399"
---
# <span data-ttu-id="2abdf-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2abdf-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="2abdf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2abdf-102">SYNOPSIS</span></span>
<span data-ttu-id="2abdf-103">Ändert eine API-Verwaltungseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2abdf-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2abdf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2abdf-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2abdf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2abdf-105">DESCRIPTION</span></span>
<span data-ttu-id="2abdf-106">Das Cmdlet " **festlegen-AzureRmApiManagementProperty** " ändert eine Azure API-Verwaltungseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2abdf-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="2abdf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2abdf-107">EXAMPLES</span></span>

### <span data-ttu-id="2abdf-108">Beispiel 1: Ändern der Tags für eine Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2abdf-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="2abdf-109">Der erste Befehl weist der $Tags Variablen zwei Werte zu.</span><span class="sxs-lookup"><span data-stu-id="2abdf-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="2abdf-110">Der zweite Befehl ändert die Eigenschaft mit der ID Property11.</span><span class="sxs-lookup"><span data-stu-id="2abdf-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="2abdf-111">Der Befehl weist die Zeichenfolgen in $Tags als Tags für die Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="2abdf-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="2abdf-112">Beispiel 2: Ändern einer Eigenschaft, um einen geheimen Wert zu haben</span><span class="sxs-lookup"><span data-stu-id="2abdf-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="2abdf-113">Mit diesem Befehl wird die zu verschlüsselnde Eigenschaft geändert.</span><span class="sxs-lookup"><span data-stu-id="2abdf-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="2abdf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2abdf-114">PARAMETERS</span></span>

### <span data-ttu-id="2abdf-115">-Context</span><span class="sxs-lookup"><span data-stu-id="2abdf-115">-Context</span></span>
<span data-ttu-id="2abdf-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2abdf-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2abdf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2abdf-117">-DefaultProfile</span></span>
<span data-ttu-id="2abdf-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2abdf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abdf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2abdf-119">-Name</span></span>
<span data-ttu-id="2abdf-120">Gibt den Namen der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="2abdf-120">Specifies the name of the property.</span></span>
<span data-ttu-id="2abdf-121">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2abdf-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="2abdf-122">Namen enthalten nur Buchstaben, Ziffern, Punkt Zeichen, Striche und Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="2abdf-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2abdf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2abdf-123">-PassThru</span></span>
<span data-ttu-id="2abdf-124">Gibt an, dass dieses Cmdlet die **PsApiManagementProperty** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2abdf-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2abdf-125">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="2abdf-125">-PropertyId</span></span>
<span data-ttu-id="2abdf-126">Gibt eine ID der Eigenschaft an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2abdf-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2abdf-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="2abdf-127">-Secret</span></span>
<span data-ttu-id="2abdf-128">Gibt an, dass der Eigenschaftswert ein Schlüssel ist und verschlüsselt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="2abdf-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2abdf-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="2abdf-129">-Tag</span></span>
<span data-ttu-id="2abdf-130">Einer Eigenschaft zugeordnete Kategorien.</span><span class="sxs-lookup"><span data-stu-id="2abdf-130">Tags associated with a property.</span></span> <span data-ttu-id="2abdf-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="2abdf-131">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2abdf-132">-Wert</span><span class="sxs-lookup"><span data-stu-id="2abdf-132">-Value</span></span>
<span data-ttu-id="2abdf-133">Gibt einen Wert für die Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="2abdf-133">Specifies a value for the property.</span></span>
<span data-ttu-id="2abdf-134">Dieser Wert kann Richtlinienausdrücke enthalten.</span><span class="sxs-lookup"><span data-stu-id="2abdf-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="2abdf-135">Die maximale Länge beträgt 1000 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2abdf-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="2abdf-136">Der Wert darf nicht leer sein oder nur aus Leerzeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="2abdf-136">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2abdf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2abdf-137">CommonParameters</span></span>
<span data-ttu-id="2abdf-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2abdf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2abdf-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2abdf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2abdf-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2abdf-140">INPUTS</span></span>

### <span data-ttu-id="2abdf-141">Keine</span><span class="sxs-lookup"><span data-stu-id="2abdf-141">None</span></span>
<span data-ttu-id="2abdf-142">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2abdf-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2abdf-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2abdf-143">OUTPUTS</span></span>

### <span data-ttu-id="2abdf-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2abdf-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="2abdf-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2abdf-145">NOTES</span></span>

## <span data-ttu-id="2abdf-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2abdf-146">RELATED LINKS</span></span>

[<span data-ttu-id="2abdf-147">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2abdf-147">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="2abdf-148">Neu – AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2abdf-148">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="2abdf-149">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2abdf-149">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


