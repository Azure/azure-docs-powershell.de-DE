---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: cd15a6f132360bba973e9361cf2f6e98c9bf24f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927083"
---
# <span data-ttu-id="3a4b8-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3a4b8-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="3a4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4b8-103">Entfernt einen Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="3a4b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a4b8-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a4b8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="3a4b8-106">Das **Cmdlet Remove-AzIntegrationAccountAgreement** entfernt einen Integrationskontovertrag aus einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="3a4b8-107">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen und den Vertragsnamen an.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="3a4b8-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3a4b8-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3a4b8-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3a4b8-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3a4b8-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a4b8-112">EXAMPLES</span></span>

### <span data-ttu-id="3a4b8-113">Beispiel 1: Entfernen eines Integrationskontovertrags nach Name</span><span class="sxs-lookup"><span data-stu-id="3a4b8-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="3a4b8-114">Mit diesem Befehl wird der Integrationskontovertrag mit dem Namen IntegrationAccountAgreement06 entfernt.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="3a4b8-115">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3a4b8-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3a4b8-116">PARAMETERS</span></span>

### <span data-ttu-id="3a4b8-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="3a4b8-117">-AgreementName</span></span>
<span data-ttu-id="3a4b8-118">Gibt den Namen des Integrationskontovertrags an.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="3a4b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4b8-119">-DefaultProfile</span></span>
<span data-ttu-id="3a4b8-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3a4b8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a4b8-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="3a4b8-121">-Force</span></span>
<span data-ttu-id="3a4b8-122">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a4b8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3a4b8-123">-Name</span></span>
<span data-ttu-id="3a4b8-124">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3a4b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a4b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a4b8-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3a4b8-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a4b8-127">-Confirm</span></span>
<span data-ttu-id="3a4b8-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a4b8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a4b8-129">-WhatIf</span></span>
<span data-ttu-id="3a4b8-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a4b8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a4b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4b8-132">CommonParameters</span></span>
<span data-ttu-id="3a4b8-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a4b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4b8-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a4b8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4b8-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a4b8-135">INPUTS</span></span>

### <span data-ttu-id="3a4b8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3a4b8-136">System.String</span></span>

## <span data-ttu-id="3a4b8-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a4b8-137">OUTPUTS</span></span>

### <span data-ttu-id="3a4b8-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="3a4b8-138">System.Void</span></span>

## <span data-ttu-id="3a4b8-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3a4b8-139">NOTES</span></span>

## <span data-ttu-id="3a4b8-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3a4b8-140">RELATED LINKS</span></span>

[<span data-ttu-id="3a4b8-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3a4b8-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="3a4b8-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3a4b8-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="3a4b8-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3a4b8-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


