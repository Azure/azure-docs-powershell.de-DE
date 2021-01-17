---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: e68fec8bf38dc990737f11d5dc3ed079d71fd6ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382036"
---
# <span data-ttu-id="f8b2f-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f8b2f-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="f8b2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b2f-103">Entfernt einen API-Verwaltungsprotokollger.</span><span class="sxs-lookup"><span data-stu-id="f8b2f-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="f8b2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8b2f-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8b2f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b2f-106">Das **Cmdlet "Remove-AzApiManagementLogger"** entfernt einen Azure API Management **Logger.**</span><span class="sxs-lookup"><span data-stu-id="f8b2f-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="f8b2f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8b2f-107">EXAMPLES</span></span>

### <span data-ttu-id="f8b2f-108">Beispiel 1: Entfernen eines Protokollgers</span><span class="sxs-lookup"><span data-stu-id="f8b2f-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="f8b2f-109">Mit diesem Befehl wird ein Protokoller entfernt, der den ID Logger123 enthält.</span><span class="sxs-lookup"><span data-stu-id="f8b2f-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="f8b2f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8b2f-110">PARAMETERS</span></span>

### <span data-ttu-id="f8b2f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f8b2f-111">-Context</span></span>
<span data-ttu-id="f8b2f-112">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="f8b2f-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f8b2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b2f-113">-DefaultProfile</span></span>
<span data-ttu-id="f8b2f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8b2f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8b2f-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="f8b2f-115">-LoggerId</span></span>
<span data-ttu-id="f8b2f-116">Gibt die ID des zu entfernenden Loggers an.</span><span class="sxs-lookup"><span data-stu-id="f8b2f-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="f8b2f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8b2f-117">-PassThru</span></span>
<span data-ttu-id="f8b2f-118">Gibt an, dass dieses Cmdlet den Wert "$True, wenn der Vorgang erfolgreich war oder $False zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f8b2f-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="f8b2f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8b2f-119">-Confirm</span></span>
<span data-ttu-id="f8b2f-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8b2f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8b2f-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f8b2f-121">-WhatIf</span></span>
<span data-ttu-id="f8b2f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8b2f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8b2f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8b2f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8b2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b2f-124">CommonParameters</span></span>
<span data-ttu-id="f8b2f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b2f-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8b2f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b2f-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8b2f-127">INPUTS</span></span>

### <span data-ttu-id="f8b2f-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f8b2f-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f8b2f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f8b2f-129">System.String</span></span>

### <span data-ttu-id="f8b2f-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f8b2f-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f8b2f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8b2f-131">OUTPUTS</span></span>

### <span data-ttu-id="f8b2f-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f8b2f-132">System.Boolean</span></span>

## <span data-ttu-id="f8b2f-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f8b2f-133">NOTES</span></span>

## <span data-ttu-id="f8b2f-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f8b2f-134">RELATED LINKS</span></span>

[<span data-ttu-id="f8b2f-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f8b2f-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="f8b2f-136">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f8b2f-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="f8b2f-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f8b2f-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


