---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: c243cd47300d2b361e37766ab7e2e5bc906cb2ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925323"
---
# <span data-ttu-id="c4a41-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c4a41-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="c4a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a41-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a41-103">Konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c4a41-103">Configures an API management group.</span></span>

## <span data-ttu-id="c4a41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4a41-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4a41-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4a41-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a41-106">Das **Cmdlet Set-AzApiManagementGroup** konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c4a41-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="c4a41-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4a41-107">EXAMPLES</span></span>

### <span data-ttu-id="c4a41-108">Beispiel 1: Konfigurieren einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="c4a41-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="c4a41-109">Mit diesem Befehl wird eine Verwaltungsgruppe namens "Group0001" konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c4a41-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="c4a41-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c4a41-110">PARAMETERS</span></span>

### <span data-ttu-id="c4a41-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c4a41-111">-Context</span></span>
<span data-ttu-id="c4a41-112">Gibt eine Instanz eines **PsApiManagementContext-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="c4a41-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c4a41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a41-113">-DefaultProfile</span></span>
<span data-ttu-id="c4a41-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4a41-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4a41-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4a41-115">-Description</span></span>
<span data-ttu-id="c4a41-116">Gibt die Beschreibung der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="c4a41-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="c4a41-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c4a41-117">-GroupId</span></span>
<span data-ttu-id="c4a41-118">Gibt den Bezeichner der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="c4a41-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="c4a41-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c4a41-119">-Name</span></span>
<span data-ttu-id="c4a41-120">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="c4a41-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="c4a41-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4a41-121">-PassThru</span></span>
<span data-ttu-id="c4a41-122">passthru</span><span class="sxs-lookup"><span data-stu-id="c4a41-122">passthru</span></span>

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

### <span data-ttu-id="c4a41-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4a41-123">-Confirm</span></span>
<span data-ttu-id="c4a41-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4a41-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a41-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a41-125">-WhatIf</span></span>
<span data-ttu-id="c4a41-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4a41-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4a41-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4a41-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a41-128">CommonParameters</span></span>
<span data-ttu-id="c4a41-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a41-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4a41-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a41-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4a41-131">INPUTS</span></span>

### <span data-ttu-id="c4a41-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c4a41-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c4a41-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c4a41-133">System.String</span></span>

### <span data-ttu-id="c4a41-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c4a41-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c4a41-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4a41-135">OUTPUTS</span></span>

### <span data-ttu-id="c4a41-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c4a41-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="c4a41-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c4a41-137">NOTES</span></span>

## <span data-ttu-id="c4a41-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c4a41-138">RELATED LINKS</span></span>

[<span data-ttu-id="c4a41-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c4a41-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="c4a41-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c4a41-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="c4a41-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c4a41-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


