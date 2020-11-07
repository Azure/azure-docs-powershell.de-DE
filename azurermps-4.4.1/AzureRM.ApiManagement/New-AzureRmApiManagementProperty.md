---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: cb50ea5735a9f63f5f35b8f1cb0648c566e6108d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664491"
---
# <span data-ttu-id="08588-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="08588-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="08588-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08588-102">SYNOPSIS</span></span>
<span data-ttu-id="08588-103">Erstellt eine neue Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="08588-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08588-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08588-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tags <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08588-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08588-105">DESCRIPTION</span></span>
<span data-ttu-id="08588-106">Das Cmdlet **New-AzureRmApiManagementProperty** erstellt eine Azure API-Verwaltungs **Eigenschaft**.</span><span class="sxs-lookup"><span data-stu-id="08588-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="08588-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08588-107">EXAMPLES</span></span>

### <span data-ttu-id="08588-108">Beispiel 1: Erstellen einer Eigenschaft, die Tags enthält</span><span class="sxs-lookup"><span data-stu-id="08588-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="08588-109">Der erste Befehl weist der $Tags Variablen zwei Werte zu.</span><span class="sxs-lookup"><span data-stu-id="08588-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="08588-110">Der zweite Befehl erstellt eine Eigenschaft und weist die Zeichenfolgen in $Tags als Tags für die Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="08588-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="08588-111">Beispiel 2: Erstellen einer Eigenschaft mit einem geheimen Wert</span><span class="sxs-lookup"><span data-stu-id="08588-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="08588-112">Mit diesem Befehl wird eine **Eigenschaft** erstellt, die über einen verschlüsselten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="08588-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="08588-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="08588-113">PARAMETERS</span></span>

### <span data-ttu-id="08588-114">-Context</span><span class="sxs-lookup"><span data-stu-id="08588-114">-Context</span></span>
<span data-ttu-id="08588-115">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="08588-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="08588-116">-Name</span><span class="sxs-lookup"><span data-stu-id="08588-116">-Name</span></span>
<span data-ttu-id="08588-117">Gibt den Namen der vom Cmdlet erstellten Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="08588-117">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="08588-118">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="08588-118">Maximum length is 100 characters.</span></span>
<span data-ttu-id="08588-119">Namen enthalten nur Buchstaben, Ziffern, Punkt Zeichen, Striche und Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="08588-119">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="08588-120">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="08588-120">-PropertyId</span></span>
<span data-ttu-id="08588-121">Gibt eine ID für die Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="08588-121">Specifies an ID for the property.</span></span>
<span data-ttu-id="08588-122">Die maximale Länge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="08588-122">Maximum length is 256 characters.</span></span>
<span data-ttu-id="08588-123">Wenn Sie keine ID angeben, generiert dieses Cmdlet eine.</span><span class="sxs-lookup"><span data-stu-id="08588-123">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="08588-124">-Secret</span><span class="sxs-lookup"><span data-stu-id="08588-124">-Secret</span></span>
<span data-ttu-id="08588-125">Gibt an, dass der Eigenschaftswert ein Schlüssel ist und verschlüsselt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="08588-125">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="08588-126">-Tags</span><span class="sxs-lookup"><span data-stu-id="08588-126">-Tags</span></span>
<span data-ttu-id="08588-127">Gibt ein Array von Tags an, die dieses Cmdlet der Eigenschaft zuordnet.</span><span class="sxs-lookup"><span data-stu-id="08588-127">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="08588-128">Sie können Kategorien verwenden, um die Eigenschaftenliste zu filtern.</span><span class="sxs-lookup"><span data-stu-id="08588-128">You can use tags to filter the property list.</span></span>

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

### <span data-ttu-id="08588-129">-Wert</span><span class="sxs-lookup"><span data-stu-id="08588-129">-Value</span></span>
<span data-ttu-id="08588-130">Gibt einen Wert für die Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="08588-130">Specifies a value for the property.</span></span>
<span data-ttu-id="08588-131">Dieser Wert kann Richtlinienausdrücke enthalten.</span><span class="sxs-lookup"><span data-stu-id="08588-131">This value can contain policy expressions.</span></span>
<span data-ttu-id="08588-132">Die maximale Länge beträgt 1000 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="08588-132">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="08588-133">Der Wert darf nicht leer sein oder nur aus Leerzeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="08588-133">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="08588-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08588-134">-DefaultProfile</span></span>
<span data-ttu-id="08588-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08588-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08588-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08588-136">CommonParameters</span></span>
<span data-ttu-id="08588-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08588-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08588-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08588-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08588-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08588-139">INPUTS</span></span>

## <span data-ttu-id="08588-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08588-140">OUTPUTS</span></span>

### <span data-ttu-id="08588-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="08588-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="08588-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="08588-142">NOTES</span></span>

## <span data-ttu-id="08588-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08588-143">RELATED LINKS</span></span>

[<span data-ttu-id="08588-144">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="08588-144">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="08588-145">Satz-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="08588-145">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


