---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472455"
---
# <span data-ttu-id="cc072-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cc072-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="cc072-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc072-102">SYNOPSIS</span></span>
<span data-ttu-id="cc072-103">Entfernt einen Vertrag für ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="cc072-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="cc072-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc072-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc072-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc072-105">DESCRIPTION</span></span>
<span data-ttu-id="cc072-106">Das **Cmdlet "Remove-AzIntegrationAccountAgreement"** entfernt einen Integrationskontovertrag aus einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc072-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="cc072-107">Geben Sie den Namen des Integrationskontos, den Namen der Ressourcengruppe und den Vertragsnamen an.</span><span class="sxs-lookup"><span data-stu-id="cc072-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="cc072-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="cc072-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cc072-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="cc072-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cc072-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="cc072-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cc072-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="cc072-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cc072-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc072-112">EXAMPLES</span></span>

### <span data-ttu-id="cc072-113">Beispiel 1: Entfernen eines Vertrags für ein Integrationskonto nach Name</span><span class="sxs-lookup"><span data-stu-id="cc072-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="cc072-114">Mit diesem Befehl wird der Vertrag für das Integrationskonto namens "IntegrationAccountAgreement06" entfernt.</span><span class="sxs-lookup"><span data-stu-id="cc072-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="cc072-115">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="cc072-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cc072-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc072-116">PARAMETERS</span></span>

### <span data-ttu-id="cc072-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="cc072-117">-AgreementName</span></span>
<span data-ttu-id="cc072-118">Gibt den Namen des Vertrags für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="cc072-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="cc072-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc072-119">-DefaultProfile</span></span>
<span data-ttu-id="cc072-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cc072-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc072-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cc072-121">-Force</span></span>
<span data-ttu-id="cc072-122">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="cc072-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc072-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cc072-123">-Name</span></span>
<span data-ttu-id="cc072-124">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="cc072-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="cc072-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc072-125">-ResourceGroupName</span></span>
<span data-ttu-id="cc072-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cc072-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cc072-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc072-127">-Confirm</span></span>
<span data-ttu-id="cc072-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc072-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc072-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cc072-129">-WhatIf</span></span>
<span data-ttu-id="cc072-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc072-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc072-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc072-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc072-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc072-132">CommonParameters</span></span>
<span data-ttu-id="cc072-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc072-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc072-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc072-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc072-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc072-135">INPUTS</span></span>

### <span data-ttu-id="cc072-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cc072-136">System.String</span></span>

## <span data-ttu-id="cc072-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc072-137">OUTPUTS</span></span>

### <span data-ttu-id="cc072-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="cc072-138">System.Void</span></span>

## <span data-ttu-id="cc072-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cc072-139">NOTES</span></span>

## <span data-ttu-id="cc072-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cc072-140">RELATED LINKS</span></span>

[<span data-ttu-id="cc072-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cc072-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="cc072-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cc072-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="cc072-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cc072-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


