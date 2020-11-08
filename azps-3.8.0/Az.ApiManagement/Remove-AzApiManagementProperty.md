---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: 41ce5ae67bbc3b21b29740cde1503e474ebe9f8a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996841"
---
# <span data-ttu-id="b7315-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b7315-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="b7315-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7315-102">SYNOPSIS</span></span>
<span data-ttu-id="b7315-103">Entfernt eine API-Verwaltungseigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7315-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="b7315-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7315-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7315-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7315-105">DESCRIPTION</span></span>
<span data-ttu-id="b7315-106">Das Cmdlet **Remove-AzApiManagementProperty** entfernt eine Azure API-Verwaltungs **Eigenschaft**.</span><span class="sxs-lookup"><span data-stu-id="b7315-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="b7315-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7315-107">EXAMPLES</span></span>

### <span data-ttu-id="b7315-108">Beispiel 1: Entfernen einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7315-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="b7315-109">Dieser Befehl entfernt die Eigenschaft mit der ID Property11.</span><span class="sxs-lookup"><span data-stu-id="b7315-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="b7315-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7315-110">PARAMETERS</span></span>

### <span data-ttu-id="b7315-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b7315-111">-Context</span></span>
<span data-ttu-id="b7315-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b7315-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b7315-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7315-113">-DefaultProfile</span></span>
<span data-ttu-id="b7315-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7315-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7315-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7315-115">-PassThru</span></span>
<span data-ttu-id="b7315-116">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="b7315-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="b7315-117">-Eigenschafts-Nr</span><span class="sxs-lookup"><span data-stu-id="b7315-117">-PropertyId</span></span>
<span data-ttu-id="b7315-118">Gibt eine ID der Eigenschaft an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="b7315-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b7315-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7315-119">-Confirm</span></span>
<span data-ttu-id="b7315-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7315-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7315-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7315-121">-WhatIf</span></span>
<span data-ttu-id="b7315-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7315-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7315-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7315-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7315-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7315-124">CommonParameters</span></span>
<span data-ttu-id="b7315-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7315-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7315-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7315-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7315-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7315-127">INPUTS</span></span>

### <span data-ttu-id="b7315-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b7315-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b7315-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b7315-129">System.String</span></span>

### <span data-ttu-id="b7315-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="b7315-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b7315-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7315-131">OUTPUTS</span></span>

### <span data-ttu-id="b7315-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7315-132">System.Boolean</span></span>

## <span data-ttu-id="b7315-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7315-133">NOTES</span></span>

## <span data-ttu-id="b7315-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7315-134">RELATED LINKS</span></span>

[<span data-ttu-id="b7315-135">Neu – AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b7315-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="b7315-136">Satz-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b7315-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


