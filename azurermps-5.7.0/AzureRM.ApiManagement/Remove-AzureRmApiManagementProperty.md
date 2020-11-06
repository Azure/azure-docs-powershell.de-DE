---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: d8c47cb6aaf1f135cd08110f4ab1d616cb105f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477045"
---
# <span data-ttu-id="346aa-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="346aa-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="346aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="346aa-102">SYNOPSIS</span></span>
<span data-ttu-id="346aa-103">Entfernt eine API-Verwaltungseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="346aa-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="346aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="346aa-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="346aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="346aa-105">DESCRIPTION</span></span>
<span data-ttu-id="346aa-106">Das Cmdlet **Remove-AzureRmApiManagementProperty** entfernt eine Azure API-Verwaltungs **Eigenschaft**.</span><span class="sxs-lookup"><span data-stu-id="346aa-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="346aa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="346aa-107">EXAMPLES</span></span>

### <span data-ttu-id="346aa-108">Beispiel 1: Entfernen einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="346aa-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="346aa-109">Dieser Befehl entfernt die Eigenschaft mit der ID Property11.</span><span class="sxs-lookup"><span data-stu-id="346aa-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="346aa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="346aa-110">PARAMETERS</span></span>

### <span data-ttu-id="346aa-111">-Context</span><span class="sxs-lookup"><span data-stu-id="346aa-111">-Context</span></span>
<span data-ttu-id="346aa-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="346aa-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="346aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="346aa-113">-DefaultProfile</span></span>
<span data-ttu-id="346aa-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="346aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="346aa-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="346aa-115">-PassThru</span></span>
<span data-ttu-id="346aa-116">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="346aa-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="346aa-117">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="346aa-117">-PropertyId</span></span>
<span data-ttu-id="346aa-118">Gibt eine ID der Eigenschaft an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="346aa-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="346aa-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="346aa-119">-Confirm</span></span>
<span data-ttu-id="346aa-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="346aa-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="346aa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="346aa-121">-WhatIf</span></span>
<span data-ttu-id="346aa-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="346aa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="346aa-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="346aa-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="346aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="346aa-124">CommonParameters</span></span>
<span data-ttu-id="346aa-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="346aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="346aa-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="346aa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="346aa-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="346aa-127">INPUTS</span></span>

### <span data-ttu-id="346aa-128">Keine</span><span class="sxs-lookup"><span data-stu-id="346aa-128">None</span></span>
<span data-ttu-id="346aa-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="346aa-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="346aa-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="346aa-130">OUTPUTS</span></span>

### <span data-ttu-id="346aa-131">bool</span><span class="sxs-lookup"><span data-stu-id="346aa-131">bool</span></span>

## <span data-ttu-id="346aa-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="346aa-132">NOTES</span></span>

## <span data-ttu-id="346aa-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="346aa-133">RELATED LINKS</span></span>

[<span data-ttu-id="346aa-134">Neu – AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="346aa-134">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="346aa-135">Satz-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="346aa-135">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


