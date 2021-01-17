---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365180"
---
# <span data-ttu-id="cb14b-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="cb14b-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="cb14b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb14b-102">SYNOPSIS</span></span>
<span data-ttu-id="cb14b-103">Löscht eine Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="cb14b-103">Deletes a action rule</span></span>

## <span data-ttu-id="cb14b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb14b-104">SYNTAX</span></span>

### <span data-ttu-id="cb14b-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb14b-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb14b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb14b-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb14b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb14b-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb14b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb14b-108">DESCRIPTION</span></span>
<span data-ttu-id="cb14b-109">**Das Cmdlet "Remove-AzActionRule"** löscht eine Aktionsregel.</span><span class="sxs-lookup"><span data-stu-id="cb14b-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="cb14b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb14b-110">EXAMPLES</span></span>

### <span data-ttu-id="cb14b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cb14b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="cb14b-112">Dieses Cmdlet löscht die Aktionsregel mit dem Namen "ActionRuleName" in "Test-rg" der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cb14b-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="cb14b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb14b-113">PARAMETERS</span></span>

### <span data-ttu-id="cb14b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb14b-114">-DefaultProfile</span></span>
<span data-ttu-id="cb14b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb14b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb14b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb14b-116">-InputObject</span></span>
<span data-ttu-id="cb14b-117">Die Aktionsregelressource</span><span class="sxs-lookup"><span data-stu-id="cb14b-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb14b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cb14b-118">-Name</span></span>
<span data-ttu-id="cb14b-119">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="cb14b-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb14b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb14b-120">-PassThru</span></span>
<span data-ttu-id="cb14b-121">PassThru gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cb14b-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="cb14b-122">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cb14b-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb14b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb14b-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb14b-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="cb14b-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb14b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb14b-125">-ResourceId</span></span>
<span data-ttu-id="cb14b-126">Aktionsregel nach Ressourcen-ID erhalten.</span><span class="sxs-lookup"><span data-stu-id="cb14b-126">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb14b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb14b-127">-Confirm</span></span>
<span data-ttu-id="cb14b-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb14b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb14b-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cb14b-129">-WhatIf</span></span>
<span data-ttu-id="cb14b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb14b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb14b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb14b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb14b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb14b-132">CommonParameters</span></span>
<span data-ttu-id="cb14b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb14b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb14b-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb14b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb14b-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb14b-135">INPUTS</span></span>

### <span data-ttu-id="cb14b-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="cb14b-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="cb14b-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb14b-137">OUTPUTS</span></span>

### <span data-ttu-id="cb14b-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb14b-138">System.Boolean</span></span>

## <span data-ttu-id="cb14b-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cb14b-139">NOTES</span></span>

## <span data-ttu-id="cb14b-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cb14b-140">RELATED LINKS</span></span>
