---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: ca0871dae696425c7f19ac1924aa0b725d0dac6c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845967"
---
# <span data-ttu-id="df055-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="df055-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="df055-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df055-102">SYNOPSIS</span></span>
<span data-ttu-id="df055-103">Ruft eine Logik-App aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="df055-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="df055-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df055-104">SYNTAX</span></span>

### <span data-ttu-id="df055-105">ListWorkflows (Standard)</span><span class="sxs-lookup"><span data-stu-id="df055-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df055-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="df055-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df055-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df055-107">DESCRIPTION</span></span>
<span data-ttu-id="df055-108">Das Cmdlet " **Get-AzLogicApp** " Ruft eine Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="df055-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="df055-109">Dieses Cmdlet gibt ein **Workflow** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="df055-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="df055-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="df055-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="df055-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="df055-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="df055-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="df055-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="df055-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="df055-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="df055-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df055-114">EXAMPLES</span></span>

### <span data-ttu-id="df055-115">Beispiel 1: Abrufen einer Logik-App aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="df055-115">Example 1: Get a logic app from a resource group</span></span>
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

<span data-ttu-id="df055-116">Dieser Befehl ruft eine Logik-App aus der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="df055-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="df055-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="df055-117">PARAMETERS</span></span>

### <span data-ttu-id="df055-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df055-118">-DefaultProfile</span></span>
<span data-ttu-id="df055-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="df055-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df055-120">-Name</span><span class="sxs-lookup"><span data-stu-id="df055-120">-Name</span></span>
<span data-ttu-id="df055-121">Gibt den Namen der Logik-APP an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="df055-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

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

### <span data-ttu-id="df055-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df055-122">-ResourceGroupName</span></span>
<span data-ttu-id="df055-123">Gibt den Namen für eine Ressourcengruppe an, in der dieses Cmdlet eine Logik-APP erhält.</span><span class="sxs-lookup"><span data-stu-id="df055-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="df055-124">-Version</span><span class="sxs-lookup"><span data-stu-id="df055-124">-Version</span></span>
<span data-ttu-id="df055-125">Gibt die Version einer Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="df055-125">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="df055-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df055-126">CommonParameters</span></span>
<span data-ttu-id="df055-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df055-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df055-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df055-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df055-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df055-129">INPUTS</span></span>

### <span data-ttu-id="df055-130">System. String</span><span class="sxs-lookup"><span data-stu-id="df055-130">System.String</span></span>

## <span data-ttu-id="df055-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df055-131">OUTPUTS</span></span>

### <span data-ttu-id="df055-132">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="df055-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="df055-133">Microsoft. Azure. Management. Logic. Models. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="df055-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="df055-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="df055-134">NOTES</span></span>

## <span data-ttu-id="df055-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df055-135">RELATED LINKS</span></span>

[<span data-ttu-id="df055-136">Neu – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="df055-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="df055-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="df055-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="df055-138">Satz-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="df055-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="df055-139">Anfang-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="df055-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


