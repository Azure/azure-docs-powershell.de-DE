---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: bb0fb41409407d6e522c8371042e94501b0e1f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663394"
---
# <span data-ttu-id="15c6f-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="15c6f-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="15c6f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="15c6f-103">Erstellt eine neue Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="15c6f-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15c6f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15c6f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15c6f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15c6f-105">DESCRIPTION</span></span>
<span data-ttu-id="15c6f-106">Das Cmdlet **New-AzureRmApiManagementProperty** erstellt eine Azure API-Verwaltungs **Eigenschaft**.</span><span class="sxs-lookup"><span data-stu-id="15c6f-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="15c6f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15c6f-107">EXAMPLES</span></span>

### <span data-ttu-id="15c6f-108">Beispiel 1: Erstellen einer Eigenschaft, die Tags enthält</span><span class="sxs-lookup"><span data-stu-id="15c6f-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="15c6f-109">Der erste Befehl weist der $Tags Variablen zwei Werte zu.</span><span class="sxs-lookup"><span data-stu-id="15c6f-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="15c6f-110">Der zweite Befehl erstellt eine Eigenschaft und weist die Zeichenfolgen in $Tags als Tags für die Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="15c6f-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="15c6f-111">Beispiel 2: Erstellen einer Eigenschaft mit einem geheimen Wert</span><span class="sxs-lookup"><span data-stu-id="15c6f-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="15c6f-112">Mit diesem Befehl wird eine **Eigenschaft** erstellt, die über einen verschlüsselten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="15c6f-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="15c6f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="15c6f-113">PARAMETERS</span></span>

### <span data-ttu-id="15c6f-114">-Context</span><span class="sxs-lookup"><span data-stu-id="15c6f-114">-Context</span></span>
<span data-ttu-id="15c6f-115">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="15c6f-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="15c6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c6f-116">-DefaultProfile</span></span>
<span data-ttu-id="15c6f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15c6f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15c6f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="15c6f-118">-Name</span></span>
<span data-ttu-id="15c6f-119">Gibt den Namen der vom Cmdlet erstellten Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="15c6f-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="15c6f-120">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="15c6f-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="15c6f-121">Namen enthalten nur Buchstaben, Ziffern, Punkt Zeichen, Striche und Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="15c6f-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="15c6f-122">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="15c6f-122">-PropertyId</span></span>
<span data-ttu-id="15c6f-123">Gibt eine ID für die Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="15c6f-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="15c6f-124">Die maximale Länge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="15c6f-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="15c6f-125">Wenn Sie keine ID angeben, generiert dieses Cmdlet eine.</span><span class="sxs-lookup"><span data-stu-id="15c6f-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="15c6f-126">-Secret</span><span class="sxs-lookup"><span data-stu-id="15c6f-126">-Secret</span></span>
<span data-ttu-id="15c6f-127">Gibt an, dass der Eigenschaftswert ein Schlüssel ist und verschlüsselt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="15c6f-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="15c6f-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="15c6f-128">-Tag</span></span>
<span data-ttu-id="15c6f-129">Tags, die mit der Eigenschaft verknüpft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15c6f-129">Tags to be associated with Property.</span></span> <span data-ttu-id="15c6f-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="15c6f-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="15c6f-131">-Wert</span><span class="sxs-lookup"><span data-stu-id="15c6f-131">-Value</span></span>
<span data-ttu-id="15c6f-132">Gibt einen Wert für die Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="15c6f-132">Specifies a value for the property.</span></span>
<span data-ttu-id="15c6f-133">Dieser Wert kann Richtlinienausdrücke enthalten.</span><span class="sxs-lookup"><span data-stu-id="15c6f-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="15c6f-134">Die maximale Länge beträgt 1000 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="15c6f-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="15c6f-135">Der Wert darf nicht leer sein oder nur aus Leerzeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="15c6f-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="15c6f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c6f-136">CommonParameters</span></span>
<span data-ttu-id="15c6f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c6f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c6f-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15c6f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c6f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15c6f-139">INPUTS</span></span>

### <span data-ttu-id="15c6f-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="15c6f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="15c6f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="15c6f-141">System.String</span></span>

### <span data-ttu-id="15c6f-142">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="15c6f-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="15c6f-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="15c6f-143">System.String[]</span></span>

## <span data-ttu-id="15c6f-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15c6f-144">OUTPUTS</span></span>

### <span data-ttu-id="15c6f-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="15c6f-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="15c6f-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="15c6f-146">NOTES</span></span>

## <span data-ttu-id="15c6f-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15c6f-147">RELATED LINKS</span></span>

[<span data-ttu-id="15c6f-148">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="15c6f-148">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="15c6f-149">Satz-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="15c6f-149">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


