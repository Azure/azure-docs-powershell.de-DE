---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: ea063de747f69d10660fe8117d34647156694b5b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821055"
---
# <span data-ttu-id="553a1-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="553a1-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="553a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="553a1-102">SYNOPSIS</span></span>
<span data-ttu-id="553a1-103">Entfernt eine API-Verwaltungseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="553a1-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="553a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="553a1-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="553a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="553a1-105">DESCRIPTION</span></span>
<span data-ttu-id="553a1-106">Das Cmdlet **Remove-AzApiManagementProperty** entfernt eine Azure API-Verwaltungs **Eigenschaft**.</span><span class="sxs-lookup"><span data-stu-id="553a1-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="553a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="553a1-107">EXAMPLES</span></span>

### <span data-ttu-id="553a1-108">Beispiel 1: Entfernen einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="553a1-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="553a1-109">Dieser Befehl entfernt die Eigenschaft mit der ID Property11.</span><span class="sxs-lookup"><span data-stu-id="553a1-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="553a1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="553a1-110">PARAMETERS</span></span>

### <span data-ttu-id="553a1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="553a1-111">-Context</span></span>
<span data-ttu-id="553a1-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="553a1-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="553a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553a1-113">-DefaultProfile</span></span>
<span data-ttu-id="553a1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="553a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="553a1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="553a1-115">-PassThru</span></span>
<span data-ttu-id="553a1-116">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="553a1-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="553a1-117">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="553a1-117">-PropertyId</span></span>
<span data-ttu-id="553a1-118">Gibt eine ID der Eigenschaft an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="553a1-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="553a1-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="553a1-119">-Confirm</span></span>
<span data-ttu-id="553a1-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="553a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="553a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="553a1-121">-WhatIf</span></span>
<span data-ttu-id="553a1-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="553a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="553a1-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="553a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="553a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553a1-124">CommonParameters</span></span>
<span data-ttu-id="553a1-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="553a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553a1-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="553a1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553a1-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="553a1-127">INPUTS</span></span>

### <span data-ttu-id="553a1-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="553a1-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="553a1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="553a1-129">System.String</span></span>

### <span data-ttu-id="553a1-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="553a1-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="553a1-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="553a1-131">OUTPUTS</span></span>

### <span data-ttu-id="553a1-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="553a1-132">System.Boolean</span></span>

## <span data-ttu-id="553a1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="553a1-133">NOTES</span></span>

## <span data-ttu-id="553a1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="553a1-134">RELATED LINKS</span></span>

[<span data-ttu-id="553a1-135">Neu – AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="553a1-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="553a1-136">Satz-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="553a1-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


