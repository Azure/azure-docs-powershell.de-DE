---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469467"
---
# <span data-ttu-id="302a0-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="302a0-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="302a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="302a0-102">SYNOPSIS</span></span>
<span data-ttu-id="302a0-103">Entfernt einen Integrationskontopartner.</span><span class="sxs-lookup"><span data-stu-id="302a0-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="302a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="302a0-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="302a0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="302a0-105">DESCRIPTION</span></span>
<span data-ttu-id="302a0-106">Das **Cmdlet "Remove-AzIntegrationAccountPartner"** entfernt einen Integrationskontopartner aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="302a0-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="302a0-107">Geben Sie den Namen des Integrationskontos, den Namen der Ressourcengruppe und den Namen des Partners an.</span><span class="sxs-lookup"><span data-stu-id="302a0-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="302a0-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="302a0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="302a0-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="302a0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="302a0-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="302a0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="302a0-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="302a0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="302a0-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="302a0-112">EXAMPLES</span></span>

### <span data-ttu-id="302a0-113">Beispiel 1: Entfernen eines Integrationskontopartners</span><span class="sxs-lookup"><span data-stu-id="302a0-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="302a0-114">Mit diesem Befehl wird der Integrationskontopartner "IntegrationAccountPartner1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="302a0-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="302a0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="302a0-115">PARAMETERS</span></span>

### <span data-ttu-id="302a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302a0-116">-DefaultProfile</span></span>
<span data-ttu-id="302a0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="302a0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="302a0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="302a0-118">-Force</span></span>
<span data-ttu-id="302a0-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="302a0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="302a0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="302a0-120">-Name</span></span>
<span data-ttu-id="302a0-121">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="302a0-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="302a0-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="302a0-122">-PartnerName</span></span>
<span data-ttu-id="302a0-123">Gibt den Namen des Integrationskontopartners an.</span><span class="sxs-lookup"><span data-stu-id="302a0-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="302a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="302a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="302a0-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="302a0-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="302a0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="302a0-126">-Confirm</span></span>
<span data-ttu-id="302a0-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="302a0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="302a0-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="302a0-128">-WhatIf</span></span>
<span data-ttu-id="302a0-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="302a0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="302a0-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="302a0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="302a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302a0-131">CommonParameters</span></span>
<span data-ttu-id="302a0-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302a0-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="302a0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302a0-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="302a0-134">INPUTS</span></span>

### <span data-ttu-id="302a0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="302a0-135">System.String</span></span>

## <span data-ttu-id="302a0-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="302a0-136">OUTPUTS</span></span>

### <span data-ttu-id="302a0-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="302a0-137">System.Void</span></span>

## <span data-ttu-id="302a0-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="302a0-138">NOTES</span></span>

## <span data-ttu-id="302a0-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="302a0-139">RELATED LINKS</span></span>

[<span data-ttu-id="302a0-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="302a0-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="302a0-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="302a0-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="302a0-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="302a0-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


