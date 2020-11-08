---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008747"
---
# <span data-ttu-id="95273-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="95273-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="95273-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95273-102">SYNOPSIS</span></span>
<span data-ttu-id="95273-103">Entfernt eine API-Verwaltung mit dem Namen "Wert".</span><span class="sxs-lookup"><span data-stu-id="95273-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="95273-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95273-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95273-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95273-105">DESCRIPTION</span></span>
<span data-ttu-id="95273-106">Das Cmdlet **Remove-AzApiManagementNamedValue** entfernt eine Azure API-Verwaltung **mit dem Namen Value**.</span><span class="sxs-lookup"><span data-stu-id="95273-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="95273-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95273-107">EXAMPLES</span></span>

### <span data-ttu-id="95273-108">Beispiel 1: Entfernen des benannten Werts</span><span class="sxs-lookup"><span data-stu-id="95273-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="95273-109">Mit diesem Befehl wird der benannte Wert entfernt, der die ID Property11.</span><span class="sxs-lookup"><span data-stu-id="95273-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="95273-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="95273-110">PARAMETERS</span></span>

### <span data-ttu-id="95273-111">-Context</span><span class="sxs-lookup"><span data-stu-id="95273-111">-Context</span></span>
<span data-ttu-id="95273-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="95273-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="95273-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="95273-113">This parameter is required.</span></span>

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

### <span data-ttu-id="95273-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95273-114">-DefaultProfile</span></span>
<span data-ttu-id="95273-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95273-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95273-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="95273-116">-NamedValueId</span></span>
<span data-ttu-id="95273-117">Bezeichner des vorhandenen benannten Werts.</span><span class="sxs-lookup"><span data-stu-id="95273-117">Identifier of existing named value.</span></span>
<span data-ttu-id="95273-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="95273-118">This parameter is required.</span></span>

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

### <span data-ttu-id="95273-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95273-119">-PassThru</span></span>
<span data-ttu-id="95273-120">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="95273-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="95273-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="95273-121">This parameter is optional.</span></span>
<span data-ttu-id="95273-122">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="95273-122">Default value is false.</span></span>

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

### <span data-ttu-id="95273-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95273-123">-Confirm</span></span>
<span data-ttu-id="95273-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95273-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95273-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95273-125">-WhatIf</span></span>
<span data-ttu-id="95273-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95273-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95273-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95273-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95273-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95273-128">CommonParameters</span></span>
<span data-ttu-id="95273-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95273-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95273-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95273-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95273-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95273-131">INPUTS</span></span>

### <span data-ttu-id="95273-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="95273-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="95273-133">System. String</span><span class="sxs-lookup"><span data-stu-id="95273-133">System.String</span></span>

### <span data-ttu-id="95273-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="95273-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="95273-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95273-135">OUTPUTS</span></span>

### <span data-ttu-id="95273-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95273-136">System.Boolean</span></span>

## <span data-ttu-id="95273-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="95273-137">NOTES</span></span>

## <span data-ttu-id="95273-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95273-138">RELATED LINKS</span></span>
