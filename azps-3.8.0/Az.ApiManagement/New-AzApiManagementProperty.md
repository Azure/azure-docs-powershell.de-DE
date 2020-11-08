---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: bed6126dbd1ea57a29d041daf10a3deb05f2dc92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996923"
---
# <span data-ttu-id="91ca6-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="91ca6-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="91ca6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="91ca6-103">Erstellt eine neue Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="91ca6-103">Creates a new Property.</span></span>

## <span data-ttu-id="91ca6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91ca6-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91ca6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91ca6-105">DESCRIPTION</span></span>
<span data-ttu-id="91ca6-106">Das Cmdlet **New-AzApiManagementProperty** erstellt eine Azure API-Verwaltungs **Eigenschaft**.</span><span class="sxs-lookup"><span data-stu-id="91ca6-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="91ca6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91ca6-107">EXAMPLES</span></span>

### <span data-ttu-id="91ca6-108">Beispiel 1: Erstellen einer Eigenschaft, die Tags enthält</span><span class="sxs-lookup"><span data-stu-id="91ca6-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="91ca6-109">Der erste Befehl weist der $Tags Variablen zwei Werte zu.</span><span class="sxs-lookup"><span data-stu-id="91ca6-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="91ca6-110">Der zweite Befehl erstellt eine Eigenschaft und weist die Zeichenfolgen in $Tags als Tags für die Eigenschaft zu.</span><span class="sxs-lookup"><span data-stu-id="91ca6-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="91ca6-111">Beispiel 2: Erstellen einer Eigenschaft mit einem geheimen Wert</span><span class="sxs-lookup"><span data-stu-id="91ca6-111">Example 2: Create a property that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="91ca6-112">Mit diesem Befehl wird eine **Eigenschaft** erstellt, die über einen verschlüsselten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="91ca6-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="91ca6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="91ca6-113">PARAMETERS</span></span>

### <span data-ttu-id="91ca6-114">-Context</span><span class="sxs-lookup"><span data-stu-id="91ca6-114">-Context</span></span>
<span data-ttu-id="91ca6-115">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="91ca6-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="91ca6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ca6-116">-DefaultProfile</span></span>
<span data-ttu-id="91ca6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91ca6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91ca6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="91ca6-118">-Name</span></span>
<span data-ttu-id="91ca6-119">Gibt den Namen der vom Cmdlet erstellten Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="91ca6-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="91ca6-120">Die maximale Länge beträgt 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="91ca6-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="91ca6-121">Namen enthalten nur Buchstaben, Ziffern, Punkt Zeichen, Striche und Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="91ca6-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="91ca6-122">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="91ca6-122">-PropertyId</span></span>
<span data-ttu-id="91ca6-123">Gibt eine ID für die Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="91ca6-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="91ca6-124">Die maximale Länge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="91ca6-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="91ca6-125">Wenn Sie keine ID angeben, generiert dieses Cmdlet eine.</span><span class="sxs-lookup"><span data-stu-id="91ca6-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="91ca6-126">-Secret</span><span class="sxs-lookup"><span data-stu-id="91ca6-126">-Secret</span></span>
<span data-ttu-id="91ca6-127">Gibt an, dass der Eigenschaftswert ein Schlüssel ist und verschlüsselt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="91ca6-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="91ca6-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="91ca6-128">-Tag</span></span>
<span data-ttu-id="91ca6-129">Tags, die mit der Eigenschaft verknüpft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="91ca6-129">Tags to be associated with Property.</span></span> <span data-ttu-id="91ca6-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="91ca6-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="91ca6-131">-Wert</span><span class="sxs-lookup"><span data-stu-id="91ca6-131">-Value</span></span>
<span data-ttu-id="91ca6-132">Gibt einen Wert für die Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="91ca6-132">Specifies a value for the property.</span></span>
<span data-ttu-id="91ca6-133">Dieser Wert kann Richtlinienausdrücke enthalten.</span><span class="sxs-lookup"><span data-stu-id="91ca6-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="91ca6-134">Die maximale Länge beträgt 1000 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="91ca6-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="91ca6-135">Der Wert darf nicht leer sein oder nur aus Leerzeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="91ca6-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="91ca6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ca6-136">CommonParameters</span></span>
<span data-ttu-id="91ca6-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ca6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ca6-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91ca6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ca6-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91ca6-139">INPUTS</span></span>

### <span data-ttu-id="91ca6-140">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="91ca6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="91ca6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="91ca6-141">System.String</span></span>

### <span data-ttu-id="91ca6-142">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="91ca6-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="91ca6-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="91ca6-143">System.String[]</span></span>

## <span data-ttu-id="91ca6-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91ca6-144">OUTPUTS</span></span>

### <span data-ttu-id="91ca6-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="91ca6-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="91ca6-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="91ca6-146">NOTES</span></span>

## <span data-ttu-id="91ca6-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91ca6-147">RELATED LINKS</span></span>

[<span data-ttu-id="91ca6-148">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="91ca6-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="91ca6-149">Satz-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="91ca6-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


