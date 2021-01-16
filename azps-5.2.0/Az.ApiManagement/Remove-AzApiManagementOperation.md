---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 153eb354ae8ba0f033a34010658b0d851572ddd6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293579"
---
# <span data-ttu-id="26fc2-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="26fc2-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="26fc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="26fc2-103">Entfernt einen vorhandenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="26fc2-103">Removes an existing operation.</span></span>

## <span data-ttu-id="26fc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26fc2-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26fc2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="26fc2-106">Das **Cmdlet "Remove-AzApiManagementOperation"** entfernt einen vorhandenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="26fc2-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="26fc2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26fc2-107">EXAMPLES</span></span>

### <span data-ttu-id="26fc2-108">Beispiel 1: Entfernen eines vorhandenen API-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="26fc2-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="26fc2-109">Mit diesem Befehl wird ein vorhandener API-Vorgang entfernt.</span><span class="sxs-lookup"><span data-stu-id="26fc2-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="26fc2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26fc2-110">PARAMETERS</span></span>

### <span data-ttu-id="26fc2-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="26fc2-111">-ApiId</span></span>
<span data-ttu-id="26fc2-112">Gibt den Bezeichner der API an.</span><span class="sxs-lookup"><span data-stu-id="26fc2-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="26fc2-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="26fc2-113">-ApiRevision</span></span>
<span data-ttu-id="26fc2-114">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="26fc2-114">Identifier of API Revision.</span></span> <span data-ttu-id="26fc2-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="26fc2-115">This parameter is optional.</span></span> <span data-ttu-id="26fc2-116">Wenn nichts angegeben wird, wird der Vorgang aus der derzeit aktiven API-Überarbeitung entfernt.</span><span class="sxs-lookup"><span data-stu-id="26fc2-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="26fc2-117">-Context</span><span class="sxs-lookup"><span data-stu-id="26fc2-117">-Context</span></span>
<span data-ttu-id="26fc2-118">Gibt eine Instanz von **PsApiManagementContext an.**</span><span class="sxs-lookup"><span data-stu-id="26fc2-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="26fc2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fc2-119">-DefaultProfile</span></span>
<span data-ttu-id="26fc2-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26fc2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26fc2-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="26fc2-121">-OperationId</span></span>
<span data-ttu-id="26fc2-122">Gibt den Bezeichner des API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="26fc2-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="26fc2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26fc2-123">-PassThru</span></span>
<span data-ttu-id="26fc2-124">Gibt an, dass dieses Cmdlet den Wert "$True, wenn es erfolgreich ist, oder den Wert "$False" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="26fc2-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="26fc2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26fc2-125">-Confirm</span></span>
<span data-ttu-id="26fc2-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26fc2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26fc2-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="26fc2-127">-WhatIf</span></span>
<span data-ttu-id="26fc2-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26fc2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26fc2-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26fc2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26fc2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fc2-130">CommonParameters</span></span>
<span data-ttu-id="26fc2-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26fc2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fc2-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26fc2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fc2-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26fc2-133">INPUTS</span></span>

### <span data-ttu-id="26fc2-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="26fc2-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26fc2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="26fc2-135">System.String</span></span>

### <span data-ttu-id="26fc2-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="26fc2-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26fc2-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26fc2-137">OUTPUTS</span></span>

### <span data-ttu-id="26fc2-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26fc2-138">System.Boolean</span></span>

## <span data-ttu-id="26fc2-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="26fc2-139">NOTES</span></span>

## <span data-ttu-id="26fc2-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="26fc2-140">RELATED LINKS</span></span>

[<span data-ttu-id="26fc2-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="26fc2-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="26fc2-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="26fc2-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="26fc2-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="26fc2-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


