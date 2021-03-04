---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: d1f15544223a20113a40975780aa8ca899205f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923616"
---
# <span data-ttu-id="3ef75-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="3ef75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ef75-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef75-103">Entfernt ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="3ef75-103">Removes an integration account.</span></span>

## <span data-ttu-id="3ef75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ef75-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ef75-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ef75-105">DESCRIPTION</span></span>
<span data-ttu-id="3ef75-106">Das **Cmdlet Remove-AzIntegrationAccount** entfernt ein Integrationskonto aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3ef75-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="3ef75-107">Geben Sie den Namen des Integrationskontos und den Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="3ef75-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="3ef75-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="3ef75-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3ef75-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="3ef75-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3ef75-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="3ef75-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3ef75-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3ef75-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3ef75-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ef75-112">EXAMPLES</span></span>

### <span data-ttu-id="3ef75-113">Beispiel 1: Entfernen eines Integrationskontos</span><span class="sxs-lookup"><span data-stu-id="3ef75-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="3ef75-114">Mit diesem Befehl wird ein Integrationskonto mit dem Namen IntegrationAccount31 entfernt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="3ef75-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3ef75-115">PARAMETERS</span></span>

### <span data-ttu-id="3ef75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef75-116">-DefaultProfile</span></span>
<span data-ttu-id="3ef75-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3ef75-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ef75-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="3ef75-118">-Force</span></span>
<span data-ttu-id="3ef75-119">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="3ef75-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ef75-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3ef75-120">-Name</span></span>
<span data-ttu-id="3ef75-121">Gibt den Namen des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="3ef75-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="3ef75-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ef75-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ef75-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3ef75-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3ef75-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ef75-124">-Confirm</span></span>
<span data-ttu-id="3ef75-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ef75-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ef75-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ef75-126">-WhatIf</span></span>
<span data-ttu-id="3ef75-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ef75-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ef75-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ef75-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ef75-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef75-129">CommonParameters</span></span>
<span data-ttu-id="3ef75-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef75-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef75-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef75-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef75-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ef75-132">INPUTS</span></span>

### <span data-ttu-id="3ef75-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3ef75-133">System.String</span></span>

## <span data-ttu-id="3ef75-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ef75-134">OUTPUTS</span></span>

### <span data-ttu-id="3ef75-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="3ef75-135">System.Void</span></span>

## <span data-ttu-id="3ef75-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3ef75-136">NOTES</span></span>

## <span data-ttu-id="3ef75-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3ef75-137">RELATED LINKS</span></span>

[<span data-ttu-id="3ef75-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="3ef75-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="3ef75-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3ef75-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


