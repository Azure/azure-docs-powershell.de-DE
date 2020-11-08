---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: e68fec8bf38dc990737f11d5dc3ed079d71fd6ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008748"
---
# <span data-ttu-id="e2ded-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e2ded-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="e2ded-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2ded-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ded-103">Entfernt eine API-verwaltungsprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="e2ded-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="e2ded-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2ded-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2ded-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2ded-105">DESCRIPTION</span></span>
<span data-ttu-id="e2ded-106">Das Cmdlet **Remove-AzApiManagementLogger** entfernt eine Azure API-Verwaltungs **Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="e2ded-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="e2ded-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2ded-107">EXAMPLES</span></span>

### <span data-ttu-id="e2ded-108">Beispiel 1: Entfernen einer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="e2ded-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="e2ded-109">Dieser Befehl entfernt eine Protokollierung mit der ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="e2ded-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="e2ded-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2ded-110">PARAMETERS</span></span>

### <span data-ttu-id="e2ded-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e2ded-111">-Context</span></span>
<span data-ttu-id="e2ded-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e2ded-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e2ded-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ded-113">-DefaultProfile</span></span>
<span data-ttu-id="e2ded-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e2ded-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2ded-115">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="e2ded-115">-LoggerId</span></span>
<span data-ttu-id="e2ded-116">Gibt die ID der zu entfernenden Protokollierung an.</span><span class="sxs-lookup"><span data-stu-id="e2ded-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="e2ded-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2ded-117">-PassThru</span></span>
<span data-ttu-id="e2ded-118">Gibt an, dass dieses Cmdlet den Wert $true zurückgibt, wenn der Vorgang erfolgreich ausgeführt wird oder $false andernfalls.</span><span class="sxs-lookup"><span data-stu-id="e2ded-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="e2ded-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e2ded-119">-Confirm</span></span>
<span data-ttu-id="e2ded-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2ded-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2ded-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ded-121">-WhatIf</span></span>
<span data-ttu-id="e2ded-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2ded-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ded-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2ded-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2ded-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ded-124">CommonParameters</span></span>
<span data-ttu-id="e2ded-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ded-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ded-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2ded-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ded-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2ded-127">INPUTS</span></span>

### <span data-ttu-id="e2ded-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e2ded-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e2ded-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e2ded-129">System.String</span></span>

### <span data-ttu-id="e2ded-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="e2ded-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e2ded-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2ded-131">OUTPUTS</span></span>

### <span data-ttu-id="e2ded-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2ded-132">System.Boolean</span></span>

## <span data-ttu-id="e2ded-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2ded-133">NOTES</span></span>

## <span data-ttu-id="e2ded-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2ded-134">RELATED LINKS</span></span>

[<span data-ttu-id="e2ded-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e2ded-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="e2ded-136">Neu – AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e2ded-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="e2ded-137">Satz-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e2ded-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


