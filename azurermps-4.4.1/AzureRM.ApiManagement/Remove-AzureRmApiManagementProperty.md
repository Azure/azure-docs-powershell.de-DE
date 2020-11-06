---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: 333ed1cb778a5a366a7ad26d426559399658db1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477422"
---
# <span data-ttu-id="cf193-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="cf193-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="cf193-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf193-102">SYNOPSIS</span></span>
<span data-ttu-id="cf193-103">Entfernt eine API-Verwaltungseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cf193-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf193-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf193-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf193-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf193-105">DESCRIPTION</span></span>
<span data-ttu-id="cf193-106">Das Cmdlet **Remove-AzureRmApiManagementProperty** entfernt eine Azure API-Verwaltungs **Eigenschaft**.</span><span class="sxs-lookup"><span data-stu-id="cf193-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="cf193-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf193-107">EXAMPLES</span></span>

### <span data-ttu-id="cf193-108">Beispiel 1: Entfernen einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cf193-108">Example 1: Remove a property</span></span>
```
PS C:\>Remove-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="cf193-109">Dieser Befehl entfernt die Eigenschaft mit der ID Property11.</span><span class="sxs-lookup"><span data-stu-id="cf193-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="cf193-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf193-110">PARAMETERS</span></span>

### <span data-ttu-id="cf193-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cf193-111">-Context</span></span>
<span data-ttu-id="cf193-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cf193-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cf193-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf193-113">-PassThru</span></span>
<span data-ttu-id="cf193-114">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="cf193-114">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="cf193-115">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="cf193-115">-PropertyId</span></span>
<span data-ttu-id="cf193-116">Gibt eine ID der Eigenschaft an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf193-116">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cf193-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf193-117">-Confirm</span></span>
<span data-ttu-id="cf193-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf193-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf193-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf193-119">-WhatIf</span></span>
<span data-ttu-id="cf193-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf193-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf193-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf193-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf193-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf193-122">-DefaultProfile</span></span>
<span data-ttu-id="cf193-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf193-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf193-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf193-124">CommonParameters</span></span>
<span data-ttu-id="cf193-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf193-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf193-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf193-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf193-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf193-127">INPUTS</span></span>

## <span data-ttu-id="cf193-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf193-128">OUTPUTS</span></span>

### <span data-ttu-id="cf193-129">bool</span><span class="sxs-lookup"><span data-stu-id="cf193-129">bool</span></span>

## <span data-ttu-id="cf193-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf193-130">NOTES</span></span>

## <span data-ttu-id="cf193-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf193-131">RELATED LINKS</span></span>

[<span data-ttu-id="cf193-132">Neu – AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="cf193-132">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="cf193-133">Satz-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="cf193-133">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


