---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 3bb20e0314e95f2586c0bd8585c7937c4d6ca5b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301283"
---
# <span data-ttu-id="da043-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="da043-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="da043-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da043-102">SYNOPSIS</span></span>
<span data-ttu-id="da043-103">Ändert ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="da043-103">Modifies an integration account.</span></span>

## <span data-ttu-id="da043-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da043-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da043-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da043-105">DESCRIPTION</span></span>
<span data-ttu-id="da043-106">Das **Cmdlet "Set-AzIntegrationAccount"** ändert ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="da043-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="da043-107">Dieses Cmdlet gibt ein Objekt zurück, das das Integrationskonto darstellt.</span><span class="sxs-lookup"><span data-stu-id="da043-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="da043-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="da043-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="da043-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="da043-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="da043-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="da043-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="da043-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="da043-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="da043-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da043-112">EXAMPLES</span></span>

### <span data-ttu-id="da043-113">Beispiel 1: Ändern eines Integrationskontos</span><span class="sxs-lookup"><span data-stu-id="da043-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="da043-114">Mit diesem Befehl wird ein Integrationskonto namens "IntegrationAccount31" in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="da043-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="da043-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da043-115">PARAMETERS</span></span>

### <span data-ttu-id="da043-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da043-116">-DefaultProfile</span></span>
<span data-ttu-id="da043-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="da043-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da043-118">-Force</span><span class="sxs-lookup"><span data-stu-id="da043-118">-Force</span></span>
<span data-ttu-id="da043-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="da043-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da043-120">-Location</span><span class="sxs-lookup"><span data-stu-id="da043-120">-Location</span></span>
<span data-ttu-id="da043-121">Gibt einen Speicherort für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="da043-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="da043-122">-Name</span><span class="sxs-lookup"><span data-stu-id="da043-122">-Name</span></span>
<span data-ttu-id="da043-123">Gibt den Namen des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="da043-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da043-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da043-124">-ResourceGroupName</span></span>
<span data-ttu-id="da043-125">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="da043-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="da043-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="da043-126">-Sku</span></span>
<span data-ttu-id="da043-127">Gibt einen Namen der SKU für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="da043-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da043-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da043-128">-Confirm</span></span>
<span data-ttu-id="da043-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da043-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da043-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="da043-130">-WhatIf</span></span>
<span data-ttu-id="da043-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da043-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da043-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da043-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da043-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da043-133">CommonParameters</span></span>
<span data-ttu-id="da043-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da043-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da043-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da043-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da043-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da043-136">INPUTS</span></span>

### <span data-ttu-id="da043-137">System.String</span><span class="sxs-lookup"><span data-stu-id="da043-137">System.String</span></span>

## <span data-ttu-id="da043-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da043-138">OUTPUTS</span></span>

### <span data-ttu-id="da043-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="da043-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="da043-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="da043-140">NOTES</span></span>

## <span data-ttu-id="da043-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="da043-141">RELATED LINKS</span></span>

[<span data-ttu-id="da043-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="da043-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="da043-143">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="da043-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="da043-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="da043-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


