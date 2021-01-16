---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 37e6fcbaf1347d9aec48f680de749bf0b967551a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291538"
---
# <span data-ttu-id="39043-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="39043-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="39043-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39043-102">SYNOPSIS</span></span>
<span data-ttu-id="39043-103">Entfernt eine Integrationskontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="39043-103">Removes an integration account map.</span></span>

## <span data-ttu-id="39043-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39043-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39043-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39043-105">DESCRIPTION</span></span>
<span data-ttu-id="39043-106">Das **Cmdlet "Remove-AzIntegrationAccountMap"** entfernt eine Integrationskontozuordnung aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="39043-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="39043-107">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen und den Zuordnungsnamen an.</span><span class="sxs-lookup"><span data-stu-id="39043-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="39043-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="39043-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="39043-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="39043-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="39043-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="39043-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="39043-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="39043-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="39043-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39043-112">EXAMPLES</span></span>

### <span data-ttu-id="39043-113">Beispiel 1: Entfernen einer Zuordnung eines Integrationskontos</span><span class="sxs-lookup"><span data-stu-id="39043-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="39043-114">Mit diesem Befehl wird die Integrationskontozuordnung namens "IntegrationAccountMap47" entfernt.</span><span class="sxs-lookup"><span data-stu-id="39043-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="39043-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39043-115">PARAMETERS</span></span>

### <span data-ttu-id="39043-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39043-116">-DefaultProfile</span></span>
<span data-ttu-id="39043-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="39043-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39043-118">-Force</span><span class="sxs-lookup"><span data-stu-id="39043-118">-Force</span></span>
<span data-ttu-id="39043-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="39043-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="39043-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="39043-120">-MapName</span></span>
<span data-ttu-id="39043-121">Gibt den Namen der Integrationskontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="39043-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39043-122">-Name</span><span class="sxs-lookup"><span data-stu-id="39043-122">-Name</span></span>
<span data-ttu-id="39043-123">Gibt den Namen des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="39043-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39043-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39043-124">-ResourceGroupName</span></span>
<span data-ttu-id="39043-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="39043-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="39043-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39043-126">-Confirm</span></span>
<span data-ttu-id="39043-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39043-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39043-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="39043-128">-WhatIf</span></span>
<span data-ttu-id="39043-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39043-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39043-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39043-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39043-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39043-131">CommonParameters</span></span>
<span data-ttu-id="39043-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39043-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39043-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39043-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39043-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39043-134">INPUTS</span></span>

### <span data-ttu-id="39043-135">System.String</span><span class="sxs-lookup"><span data-stu-id="39043-135">System.String</span></span>

## <span data-ttu-id="39043-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39043-136">OUTPUTS</span></span>

### <span data-ttu-id="39043-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="39043-137">System.Void</span></span>

## <span data-ttu-id="39043-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39043-138">NOTES</span></span>

## <span data-ttu-id="39043-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39043-139">RELATED LINKS</span></span>

[<span data-ttu-id="39043-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="39043-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="39043-141">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="39043-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="39043-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="39043-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


