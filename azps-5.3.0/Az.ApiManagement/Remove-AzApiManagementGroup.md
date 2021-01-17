---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382051"
---
# <span data-ttu-id="335e6-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="335e6-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="335e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="335e6-102">SYNOPSIS</span></span>
<span data-ttu-id="335e6-103">Entfernt eine vorhandene API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="335e6-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="335e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="335e6-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="335e6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="335e6-105">DESCRIPTION</span></span>
<span data-ttu-id="335e6-106">Das **Cmdlet "Remove-AzApiManagementGroup"** entfernt eine vorhandene API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="335e6-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="335e6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="335e6-107">EXAMPLES</span></span>

### <span data-ttu-id="335e6-108">Beispiel 1: Entfernen einer vorhandenen Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="335e6-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="335e6-109">Mit diesem Befehl wird eine vorhandene Verwaltungsgruppe namens "Group0001" entfernt, und der Benutzer wird nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="335e6-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="335e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="335e6-110">PARAMETERS</span></span>

### <span data-ttu-id="335e6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="335e6-111">-Context</span></span>
<span data-ttu-id="335e6-112">Gibt die Instanz eines **PsApiManagementContext-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="335e6-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="335e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="335e6-113">-DefaultProfile</span></span>
<span data-ttu-id="335e6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="335e6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="335e6-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="335e6-115">-GroupId</span></span>
<span data-ttu-id="335e6-116">Gibt den Bezeichner einer Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="335e6-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="335e6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="335e6-117">-PassThru</span></span>
<span data-ttu-id="335e6-118">Gibt an, dass dieses Cmdlet den Wert "$True, wenn es erfolgreich ist, oder den Wert "$False" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="335e6-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="335e6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="335e6-119">-Confirm</span></span>
<span data-ttu-id="335e6-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="335e6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="335e6-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="335e6-121">-WhatIf</span></span>
<span data-ttu-id="335e6-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="335e6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="335e6-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="335e6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="335e6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="335e6-124">CommonParameters</span></span>
<span data-ttu-id="335e6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="335e6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="335e6-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="335e6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="335e6-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="335e6-127">INPUTS</span></span>

### <span data-ttu-id="335e6-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="335e6-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="335e6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="335e6-129">System.String</span></span>

### <span data-ttu-id="335e6-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="335e6-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="335e6-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="335e6-131">OUTPUTS</span></span>

### <span data-ttu-id="335e6-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="335e6-132">System.Boolean</span></span>

## <span data-ttu-id="335e6-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="335e6-133">NOTES</span></span>

## <span data-ttu-id="335e6-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="335e6-134">RELATED LINKS</span></span>

[<span data-ttu-id="335e6-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="335e6-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="335e6-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="335e6-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="335e6-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="335e6-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


