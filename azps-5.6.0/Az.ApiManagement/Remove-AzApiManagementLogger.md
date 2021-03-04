---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: 7bdf37996fb5d407d3961ddacee4701acce2baaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919083"
---
# <span data-ttu-id="2a799-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2a799-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="2a799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a799-102">SYNOPSIS</span></span>
<span data-ttu-id="2a799-103">Entfernt einen API-Verwaltungsprotokollger.</span><span class="sxs-lookup"><span data-stu-id="2a799-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="2a799-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a799-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a799-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a799-105">DESCRIPTION</span></span>
<span data-ttu-id="2a799-106">Das **Cmdlet Remove-AzApiManagementLogger** entfernt einen Azure API **Management Logger**.</span><span class="sxs-lookup"><span data-stu-id="2a799-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="2a799-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a799-107">EXAMPLES</span></span>

### <span data-ttu-id="2a799-108">Beispiel 1: Entfernen eines Loggers</span><span class="sxs-lookup"><span data-stu-id="2a799-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="2a799-109">Mit diesem Befehl wird ein Logger entfernt, der über die ID Logger123 verfügt.</span><span class="sxs-lookup"><span data-stu-id="2a799-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="2a799-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2a799-110">PARAMETERS</span></span>

### <span data-ttu-id="2a799-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2a799-111">-Context</span></span>
<span data-ttu-id="2a799-112">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="2a799-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2a799-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a799-113">-DefaultProfile</span></span>
<span data-ttu-id="2a799-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a799-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a799-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="2a799-115">-LoggerId</span></span>
<span data-ttu-id="2a799-116">Gibt die ID des zu entfernenden Loggers an.</span><span class="sxs-lookup"><span data-stu-id="2a799-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="2a799-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a799-117">-PassThru</span></span>
<span data-ttu-id="2a799-118">Gibt an, dass dieses Cmdlet den Wert $True, wenn der Vorgang erfolgreich ist oder $False wird.</span><span class="sxs-lookup"><span data-stu-id="2a799-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="2a799-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2a799-119">-Confirm</span></span>
<span data-ttu-id="2a799-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a799-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a799-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a799-121">-WhatIf</span></span>
<span data-ttu-id="2a799-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a799-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a799-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a799-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a799-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a799-124">CommonParameters</span></span>
<span data-ttu-id="2a799-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a799-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a799-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a799-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a799-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a799-127">INPUTS</span></span>

### <span data-ttu-id="2a799-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a799-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a799-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2a799-129">System.String</span></span>

### <span data-ttu-id="2a799-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a799-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a799-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a799-131">OUTPUTS</span></span>

### <span data-ttu-id="2a799-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a799-132">System.Boolean</span></span>

## <span data-ttu-id="2a799-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2a799-133">NOTES</span></span>

## <span data-ttu-id="2a799-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2a799-134">RELATED LINKS</span></span>

[<span data-ttu-id="2a799-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2a799-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="2a799-136">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2a799-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="2a799-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2a799-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


