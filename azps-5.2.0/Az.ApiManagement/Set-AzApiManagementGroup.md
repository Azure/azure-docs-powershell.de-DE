---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365782"
---
# <span data-ttu-id="68eea-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="68eea-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="68eea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68eea-102">SYNOPSIS</span></span>
<span data-ttu-id="68eea-103">Konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="68eea-103">Configures an API management group.</span></span>

## <span data-ttu-id="68eea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68eea-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68eea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68eea-105">DESCRIPTION</span></span>
<span data-ttu-id="68eea-106">Das **Cmdlet "Set-AzApiManagementGroup"** konfiguriert eine API-Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="68eea-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="68eea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="68eea-107">EXAMPLES</span></span>

### <span data-ttu-id="68eea-108">Beispiel 1: Konfigurieren einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="68eea-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="68eea-109">Mit diesem Befehl wird eine Verwaltungsgruppe namens "Group0001" konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="68eea-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="68eea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68eea-110">PARAMETERS</span></span>

### <span data-ttu-id="68eea-111">-Context</span><span class="sxs-lookup"><span data-stu-id="68eea-111">-Context</span></span>
<span data-ttu-id="68eea-112">Gibt eine Instanz eines **PsApiManagementContext-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="68eea-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="68eea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68eea-113">-DefaultProfile</span></span>
<span data-ttu-id="68eea-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68eea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68eea-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68eea-115">-Description</span></span>
<span data-ttu-id="68eea-116">Gibt die Beschreibung der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="68eea-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="68eea-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="68eea-117">-GroupId</span></span>
<span data-ttu-id="68eea-118">Gibt den Bezeichner der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="68eea-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="68eea-119">-Name</span><span class="sxs-lookup"><span data-stu-id="68eea-119">-Name</span></span>
<span data-ttu-id="68eea-120">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="68eea-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="68eea-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68eea-121">-PassThru</span></span>
<span data-ttu-id="68eea-122">passthru</span><span class="sxs-lookup"><span data-stu-id="68eea-122">passthru</span></span>

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

### <span data-ttu-id="68eea-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68eea-123">-Confirm</span></span>
<span data-ttu-id="68eea-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68eea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68eea-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="68eea-125">-WhatIf</span></span>
<span data-ttu-id="68eea-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68eea-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68eea-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68eea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68eea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68eea-128">CommonParameters</span></span>
<span data-ttu-id="68eea-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68eea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68eea-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68eea-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68eea-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="68eea-131">INPUTS</span></span>

### <span data-ttu-id="68eea-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68eea-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68eea-133">System.String</span><span class="sxs-lookup"><span data-stu-id="68eea-133">System.String</span></span>

### <span data-ttu-id="68eea-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="68eea-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68eea-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="68eea-135">OUTPUTS</span></span>

### <span data-ttu-id="68eea-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="68eea-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="68eea-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="68eea-137">NOTES</span></span>

## <span data-ttu-id="68eea-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="68eea-138">RELATED LINKS</span></span>

[<span data-ttu-id="68eea-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="68eea-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="68eea-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="68eea-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="68eea-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="68eea-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


