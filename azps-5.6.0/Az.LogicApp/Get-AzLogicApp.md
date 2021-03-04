---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: 98232807cc5f7624242cd44c7d27579ef0f92d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921963"
---
# <span data-ttu-id="b2dd7-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b2dd7-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="b2dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="b2dd7-103">Ruft eine Logik-App aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="b2dd7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2dd7-104">SYNTAX</span></span>

### <span data-ttu-id="b2dd7-105">ListWorkflows (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2dd7-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2dd7-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="b2dd7-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2dd7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2dd7-107">DESCRIPTION</span></span>
<span data-ttu-id="b2dd7-108">Das **Get-AzLogicApp-Cmdlet** ruft eine Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="b2dd7-109">Dieses Cmdlet gibt ein **Workflowobjekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="b2dd7-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b2dd7-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b2dd7-112">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b2dd7-113">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b2dd7-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2dd7-114">EXAMPLES</span></span>

### <span data-ttu-id="b2dd7-115">Beispiel 1: Herunterladen einer Logik-App aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b2dd7-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="b2dd7-116">Dieser Befehl ruft eine Logik-App aus der Ressourcengruppe "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="b2dd7-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b2dd7-117">PARAMETERS</span></span>

### <span data-ttu-id="b2dd7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2dd7-118">-DefaultProfile</span></span>
<span data-ttu-id="b2dd7-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b2dd7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2dd7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b2dd7-120">-Name</span></span>
<span data-ttu-id="b2dd7-121">Gibt den Namen der Logik-App an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2dd7-122">-ResourceGroupName</span></span>
<span data-ttu-id="b2dd7-123">Gibt den Namen für eine Ressourcengruppe an, in der dieses Cmdlet eine Logik-App erhält.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-124">-Version</span><span class="sxs-lookup"><span data-stu-id="b2dd7-124">-Version</span></span>
<span data-ttu-id="b2dd7-125">Gibt die Version einer Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2dd7-126">CommonParameters</span></span>
<span data-ttu-id="b2dd7-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2dd7-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2dd7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2dd7-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2dd7-129">INPUTS</span></span>

### <span data-ttu-id="b2dd7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b2dd7-130">System.String</span></span>

## <span data-ttu-id="b2dd7-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2dd7-131">OUTPUTS</span></span>

### <span data-ttu-id="b2dd7-132">Microsoft.Azure.Management.Logic.Models.Workflow</span><span class="sxs-lookup"><span data-stu-id="b2dd7-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="b2dd7-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="b2dd7-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="b2dd7-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b2dd7-134">NOTES</span></span>

## <span data-ttu-id="b2dd7-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b2dd7-135">RELATED LINKS</span></span>

[<span data-ttu-id="b2dd7-136">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b2dd7-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="b2dd7-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b2dd7-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="b2dd7-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b2dd7-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="b2dd7-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b2dd7-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


